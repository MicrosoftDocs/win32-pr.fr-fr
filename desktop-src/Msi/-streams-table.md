---
description: le \_ tableau Flux répertorie les flux de données OLE incorporés. il s’agit d’une table temporaire, créée uniquement lorsqu’elle est référencée par une instruction SQL.
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: Table _Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f3796a3abb402027dc9985991a6ba673f5381d8f35657e7d80b0714c40f1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013337"
---
# <a name="_streams-table"></a>\_Flux Tableau

le \_ tableau Flux répertorie les flux de données OLE incorporés. il s’agit d’une table temporaire, créée uniquement lorsqu’elle est référencée par une instruction SQL.



| Colonne | Type                 | Clé | Nullable |
|--------|----------------------|-----|----------|
| Nom   | [Text](text.md)     | O   | N        |
| Données   | [Binaire](binary.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Clé unique qui identifie le flux. La longueur maximale du nom est de 62 caractères.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Métadonnée
</dt> <dd>

Données binaires non mises en forme.

</dd> </dl>

## <a name="remarks"></a>Remarques

pour copier un flux de données OLE (par exemple, un objet du type de données [Binary](binary.md) ) d’un fichier dans une base de données, créez un enregistrement dans la \_ table Flux et entrez le nom du flux de données dans la colonne nom de cet enregistrement, puis copiez les données du fichier dans la colonne de données à l’aide de [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama). Utilisez [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pour insérer le nouvel enregistrement dans la table.

pour lire un flux de données binaires incorporé dans une base de données, utilisez une requête SQL pour rechercher et extraire l’enregistrement contenant les données binaires. Utilisez [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) pour lire les données binaires dans une mémoire tampon.

Pour déplacer un flux de données binaires d’une base de données vers une autre, exportez d’abord les données dans un fichier. utilisez une requête de SQL pour trouver le flux de données dans le fichier et utilisez [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) pour copier les données du fichier dans la colonne de données de \_ Flux table de la deuxième base de données. Cela garantit que chaque base de données possède sa propre copie des données binaires. Vous ne pouvez pas déplacer des données binaires d’une base de données vers une autre simplement en extrayant un enregistrement avec les données de la première base de données et en l’insérant dans la deuxième base de données.

Pour supprimer un flux de données, récupérez l’enregistrement et affectez la valeur null à la colonne de données avant de mettre à jour l’enregistrement. une autre méthode consiste à supprimer l’enregistrement de la table, en le supprimant à l’aide de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou d’une requête simple SQL. Un flux ne doit pas être extrait dans un enregistrement si le flux est supprimé de la table.

Pour renommer un flux de données OLE, mettez à jour la colonne « Name » de l’enregistrement.

si un blocage est placé sur cette table à l’aide de SQL (ALTER table <table> HOLD) ou une colonne est ajoutée avec HOLD, la table doit être libérée à l’aide de FREE. les Flux ne sont pas écrits tant que la table n’a pas été libérée ou validée.

 

 



