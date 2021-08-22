---
description: L’objet View représente un jeu de résultats obtenu lors du traitement d’une requête à l’aide de la méthode OpenView de l’objet Database.
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: Afficher l’objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f5025df952ce6e3c5ce43bf3dcb93748a241702b8c4e2f52cd9d0fd00103dc49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145272"
---
# <a name="view-object"></a>Afficher l’objet

L’objet **View** représente un jeu de résultats obtenu lors du traitement d’une requête à l’aide de la méthode [**OpenView**](database-openview.md) de l’objet [**Database**](database-object.md) . avant de pouvoir transférer des données, la requête doit être exécutée à l’aide de la méthode [**execute**](view-execute.md) , en lui transmettant tous les paramètres remplaçables désignés dans la chaîne de requête SQL. La requête peut être exécutée à nouveau, avec des paramètres différents, si nécessaire, mais uniquement après avoir libéré le jeu de résultats en extrayant tous les enregistrements ou en appelant la méthode [**Close**](view-close.md) .

## <a name="members"></a>Membres

L’objet de **vue** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet de **vue** possède ces méthodes.



| Méthode                            | Description                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Plus**](view-close.md)       | Met fin à l’exécution de la requête et libère les ressources de la base de données.<br/>                                                                                                          |
| [**Effectue**](view-execute.md)   | utilise le jeton de point d’interrogation pour représenter les paramètres dans une requête de SQL. Les valeurs de ces paramètres sont transmises en tant que champs correspondants d’un enregistrement de paramètre.<br/> |
| [**Collecté**](view-fetch.md)       | Retourne un objet [**Record**](record-object.md) contenant les données de la colonne demandée si davantage de lignes sont disponibles dans le jeu de résultats, sinon retourne la valeur null.<br/>      |
| [**GetError**](view-geterror.md) | Retourne l’erreur de validation et le nom de la colonne pour laquelle l’erreur s’est produite.<br/>                                                                                           |
| [**Modify**](view-modify.md)     | Modifie une ligne de base de données avec un objet [**enregistrement**](record-object.md) modifié obtenu à l’aide de la méthode [**Fetch**](view-fetch.md) .<br/>                                   |



 

### <a name="properties"></a>Propriétés

L’objet de **vue** possède ces propriétés.



| Propriété                                         | Description                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**ColumnInfo**](view-columninfo.md)<br/> | Retourne un objet [**Record**](record-object.md) contenant les informations demandées sur chaque colonne du jeu de résultats.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | L’IID \_ IView est défini en tant que 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Exemples de scripts d’installation](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




