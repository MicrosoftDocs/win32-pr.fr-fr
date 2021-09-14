---
description: Le programme d’installation fournit des fonctions qui manipulent les enregistrements dans une base de données d’installation. Ces fonctions peuvent être utilisées conjointement avec les fonctions décrites dans utilisation de requêtes pour apporter des modifications réelles dans une base de données.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Utilisation des enregistrements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3252dc29bf755d08494dbdc2326bf45a4afb1c91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011805"
---
# <a name="working-with-records"></a>Utilisation des enregistrements

Le programme d’installation fournit des fonctions qui manipulent les enregistrements dans une base de données d’installation. Ces fonctions peuvent être utilisées conjointement avec les fonctions décrites dans [utilisation de requêtes](working-with-queries.md) pour apporter des modifications réelles dans une base de données.

Les fonctions suivantes créent ou suppriment des enregistrements :

-   Pour créer un nouvel enregistrement pour une base de données, appelez la fonction [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) .
-   Pour effacer les données d’un enregistrement, attribuez la valeur null à chaque champ en appelant la fonction [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) .

Les fonctions suivantes remplissent les champs d’enregistrements spécifiés :

-   Pour définir un enregistrement sur un entier, appelez la fonction [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) .
-   Pour définir un enregistrement sur une chaîne, appelez la fonction [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) .
-   Pour insérer un fichier entier dans un champ de flux, appelez la fonction [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) .

Les fonctions suivantes lisent des valeurs à partir de champs d’enregistrements spécifiés :

-   Pour lire une valeur entière à partir d’un champ, appelez la fonction [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) .
-   Pour récupérer une valeur de chaîne, appelez la fonction [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) .
-   Pour obtenir un flux, appelez la fonction [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) .
-   Pour déterminer si un champ particulier d’un enregistrement a la valeur null, appelez la fonction [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) .

Les fonctions suivantes sont des fonctions d’enregistrement d’informations :

-   Pour obtenir le nombre de champs qu’un enregistrement contient, appelez la fonction [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) .
-   Pour obtenir la taille d’un champ, appelez la fonction [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) . La valeur de retour de **MsiRecordDataSize** est sensible au type de champ.

 

 



