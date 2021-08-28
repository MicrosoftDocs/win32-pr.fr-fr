---
description: La propriété ColumnInfo de l’objet View retourne un objet record contenant les informations demandées sur chaque colonne du jeu de résultats.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: View. ColumnInfo, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.ColumnInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 08996c3e77212032eac8f65621c7f8ca9ee8489683295c63fb30092995ad41d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012699"
---
# <a name="viewcolumninfo-property"></a>View. ColumnInfo, propriété

La propriété **COLUMNINFO** de l’objet [**View**](view-object.md) retourne un objet [**Record**](record-object.md) contenant les informations demandées sur chaque colonne du jeu de résultats. Les noms de colonnes ou les définitions de colonne peuvent être demandés. Les constantes fournies dans la liste de sélection n’ont pas de noms.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a>Valeur de la propriété

Informations requises pour chaque colonne.



| Nom du paramètre                                                                                                                                                                                                                                                          | Signification                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <dt>**msiColumnInfoNames**</dt> <dt>0</dt> </dl> | Retourne les noms de toutes les colonnes non constantes dans le jeu de résultats.<br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <dt>**msiColumnInfoTypes**</dt> <dt>1</dt> </dl> | Retourne les types de toutes les colonnes non constantes dans le jeu de résultats.<br/> |



 

## <a name="remarks"></a>Remarques

Les descriptions de colonne retournées par la propriété **COLUMNINFO** sont au format décrit dans [format de définition de colonne](column-definition-format.md). Chaque colonne est décrite par une chaîne dans le champ d’enregistrement correspondant. La chaîne de définition se compose d’une seule lettre représentant le type de données suivi de la largeur de la colonne (en caractères, le cas échéant, ou d’octets). Une largeur de zéro désigne une largeur illimitée (champs de texte long et flux). Une lettre majuscule indique que les valeurs NULL sont autorisées dans la colonne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | L’IID \_ IView est défini en tant que 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




