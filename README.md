#CaptureBills

Une comptabilité rapide et intuitive à portée de main - suivez-vos dépenses en temps réel

##Product Vision:

Prise de photo de factures pour préremplir la note de frais (détection date, montant TTC, montant TVA, émetteur, lieu, choix compte bancaire perso et pro)
Gestionnaire de devis et espace de facturation
Frais kilometrique
Gestionnaire de stock
Mise en relation avec expert comptable

##Contributeurs:

Diana
Ali
Heloise

##Dev:

INSERTIONS SQL

INSERT INTO credentials (pseudo, password) VALUES ('tutu', 'nhgbmn1434nse');

INSERT INTO role (status) VALUES ('admin');

INSERT INTO user (credentials_id, email, firstname, lastname, adress, role_id) VALUES (5,'tutu@gmail.fr', 'tutu', 'dupont','18 impasse des lauriers', 2);

INSERT INTO userrole (user_id, role_id) VALUES (1,3);


REQUETES SQL
Affiche ceux qui ont 12 dans leur addresse:
SELECT * FROM user WHERE address LIKE "12%";

Double jointure sans union pour avoir info de user et role en passant par userrole:
SELECT * FROM userrole 
JOIN user ON user.id = userrole.user_id 
JOIN role ON role.id = userrole.role_id;

Outer join entre user et userrole:
SELECT * FROM user 
LEFT JOIN userrole ON user.id = userrole.user_id 
UNION SELECT * FROM user 
RIGHT JOIN userrole ON user.id = userrole.user_id;







