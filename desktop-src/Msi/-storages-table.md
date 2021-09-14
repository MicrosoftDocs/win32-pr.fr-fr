---
description: Le \_ tableau stockages répertorie les stockages de données OLE incorporés. il s’agit d’une table temporaire, créée uniquement lorsqu’elle est référencée par une instruction SQL.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: Table _Storages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093025"
---
# <a name="_storages-table"></a>\_Table de stockage

Le \_ tableau stockages répertorie les stockages de données OLE incorporés. il s’agit d’une table temporaire, créée uniquement lorsqu’elle est référencée par une instruction SQL.



| Colonne | Type                 | Clé | Nullable |
|--------|----------------------|-----|----------|
| Nom   | [Text](text.md)     | O   | N        |
| Données   | [Binaire](binary.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Clé unique qui identifie le stockage. La longueur maximale du nom est de 31 caractères.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Métadonnée
</dt> <dd>

Données binaires non mises en forme.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour ajouter un stockage OLE à une base de données, créez un nouvel enregistrement dans la \_ table de stockage et entrez le nom du stockage dans la colonne nom. Utilisez [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) pour copier des données dans la colonne de données de cet enregistrement. Enfin, utilisez [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pour insérer l’enregistrement dans la \_ table storages.

Les données ne peuvent pas être lues à partir de la \_ table de stockage. Toutefois, la \_ table de stockage peut être interrogée pour vérifier l’existence d’un stockage spécifique. Cela signifie qu’il n’est pas possible de déplacer un stockage OLE d’une base de données vers une autre. Au lieu de cela, vous devez importer le fichier de stockage d’origine dans la nouvelle base de données. Pour supprimer un stockage OLE, récupérez l’enregistrement contenant les données binaires, affectez la valeur null à la colonne de données de la \_ table storages, puis mettez à jour l’enregistrement. une autre méthode consiste simplement à supprimer l’enregistrement à l’aide de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou d’une requête simple SQL.

Pour renommer un stockage OLE, mettez à jour la colonne Name de l’enregistrement.

si un blocage est placé sur cette table à l’aide de SQL (ALTER table <table> HOLD) ou une colonne est ajoutée avec HOLD, la table doit être libérée à l’aide de FREE. Les stockages ne sont pas écrits tant que la table n’a pas été libérée ou validée.

 

 



