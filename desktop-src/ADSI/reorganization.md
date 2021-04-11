---
title: Réorganisation
description: L’Organisation des ventes a été déplacée vers une nouvelle organisation \ 8212 ; \ 0034 ; Ventes et support. \ 0034 ; Julie Bankert a été promue au vice-président et va mener la nouvelle organisation.
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- Réorganisation de l’ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587f3de34738814b34ad250bb00bb7b71121d65c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028555"
---
# <a name="reorganization"></a>Réorganisation

L’Organisation des ventes a été déplacée vers une nouvelle organisation (« ventes et support »). Julie Bankert a été promue au vice-président et va mener la nouvelle organisation. Joe worden, administrateur de l’entreprise, doit déplacer l’unité d’organisation Sales vers une nouvelle unité d’organisation, sales et support.


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



Avec cet exemple de code, tous les objets de l’unité d’organisation Sales, y compris les sous-unités d’organisation, sont déplacés vers la nouvelle unité d’organisation.

Joe peut à présent déplacer Julie vers l’unité d’organisation Sales and support.


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



N’oubliez pas que le lien Manager-direct Report entre Julie Bankert et Chris Gray est automatiquement mis à jour par Active Directory.

**Pour créer un rapport de Active Directory**

1.  Ouvrez Visual Basic version 6,0 et, lorsque vous êtes invité à entrer le type de projet, sélectionnez **projet de données**.
2.  Sur le **projet de données**, double-cliquez sur **données Environment1**.
3.  Dans la fenêtre **environnement de données** , cliquez avec le bouton droit sur l’objet de connexion **(Connection1)** et sélectionnez **Propriétés**.
4.  Sélectionnez **OLE DB fournisseur pour les services d’annuaire Microsoft**, puis cliquez sur **suivant**.
5.  Sélectionnez **utiliser la sécurité intégrée de Windows NT**, puis cliquez sur **OK**. Cela crée un objet de connexion.
6.  Cliquez à nouveau avec le bouton droit sur la fenêtre **environnement de données** pour sélectionner **Ajouter une commande**. Cliquez avec le bouton droit sur l’objet **Command1** et sélectionnez **Propriétés**. La boîte de dialogue **Propriétés de commande1** suivante s’affiche.

    ![boîte de dialogue Propriétés de commande1](images/adadsi3.png)

7.  Cliquez sur la case d’option **instruction SQL** et tapez la commande suivante :

    Sélectionnez nom, telephoneNumber à partir de « LDAP://DC = fabrikam, DC = com », où objectCategory = « Person » et objectClass = « user »

    L’objet **Command** est créé. Ajoutez l’objet de **commande** au rapport.

8.  Double-cliquez sur **données Report1** dans la fenêtre **projet** .
9.  Faites glisser l’objet **Command1** de la fenêtre **DataEnvironment1** vers la section **Détails** de la fenêtre **rapport de données** .
10. Dans **Propriétés de DataReport1**, pour **DataSource**, sélectionnez **DataEnvironment1** dans le menu déroulant, puis sélectionnez **Command1** dans le champ **DataMember** .
11. Dans la fenêtre projet, cliquez avec le bouton droit sur **projet de données**, puis sélectionnez **Propriétés de DataProject**.
12. Dans la fenêtre de boîte de dialogue **DataProject-propriétés du projet** , sous **objet de démarrage**, sélectionnez **DataReport1** dans le menu déroulant. Cliquez sur **OK** pour enregistrer.
13. Compilation. La boîte de dialogue **DataReport1** suivante s’affiche.

    ![boîte de dialogue datareport1](images/adadsi4.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Jointure de données hétérogènes](joining-heterogeneous-data.md)
</dt> </dl>

 

 




