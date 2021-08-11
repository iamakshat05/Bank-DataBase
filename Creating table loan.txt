CREATE TABLE loan
   (
   
    custid VARCHAR(6),
    bid VARCHAR(6),
    loan_amount INT(7),
    CONSTRAINT loan_customer_custid_bid_pk PRIMARY KEY(custid,bid),
    CONSTRAINT loan_custid_fk FOREIGN KEY(custid) REFERENCES  customer(custid),
    CONSTRAINT loan_bid_fk FOREIGN KEY(bid) REFERENCES  branch(bid)
   );