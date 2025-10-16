digraph ATM_Para_Cekme {
    rankdir=TB;
    node [shape=box, style=rounded];

    Start [label="Başla", shape=ellipse, style=filled, fillcolor=lightgreen];
    InsertCard [label="Kart takıldı mı?"];
    EnterPIN [label="PIN gir"];
    CheckPIN [label="PIN doğru mu?", shape=diamond];
    RetryPIN [label="PIN tekrar gir"];
    ExceedAttempts [label="3 Hatalı giriş - Kart iade", shape=box, style=filled, fillcolor=lightcoral];
    SelectAmount [label="Çekilecek miktarı gir"];
    CheckBalance [label="Yeterli bakiye var mı?", shape=diamond];
    DenyWithdrawal [label="Yetersiz bakiye", style=filled, fillcolor=lightcoral];
    DispenseCash [label="Parayı ver"];
    EjectCard [label="Kartı iade et"];
    End [label="Bitti", shape=ellipse, style=filled, fillcolor=lightgreen];

    Start -> InsertCard;
    InsertCard -> EnterPIN;
    EnterPIN -> CheckPIN;

    CheckPIN -> SelectAmount [label="Evet"];
    CheckPIN -> RetryPIN [label="Hayır"];

    RetryPIN -> CheckPIN;
    CheckPIN -> ExceedAttempts [label="3. Hatalı Giriş"];

    SelectAmount -> CheckBalance;
    CheckBalance -> DispenseCash [label="Evet"];
    CheckBalance -> DenyWithdrawal [label="Hayır"];

    DispenseCash -> EjectCard;
    DenyWithdrawal -> EjectCard;
    ExceedAttempts -> End;
    EjectCard -> End;
}
