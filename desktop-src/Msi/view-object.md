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
ms.openlocfilehash: c26cfa3c4873913d70fca63537f1d25532648a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528560"
---
# <a name="view-object"></a>Afficher l’objet

L’objet **View** représente un jeu de résultats obtenu lors du traitement d’une requête à l’aide de la méthode [**OpenView**](database-openview.md) de l’objet [**Database**](database-object.md) . Avant de pouvoir transférer des données, la requête doit être exécutée à l’aide de la méthode [**Execute**](view-execute.md) , en lui transmettant tous les paramètres remplaçables désignés dans la chaîne de requête SQL. La requête peut être exécutée à nouveau, avec des paramètres différents, si nécessaire, mais uniquement après avoir libéré le jeu de résultats en extrayant tous les enregistrements ou en appelant la méthode [**Close**](view-close.md) .

## <a name="members"></a>Membres

L’objet de **vue** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet de **vue** possède ces méthodes.



| Méthode                            | Description                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Fermer**](view-close.md)       | Met fin à l’exécution de la requête et libère les ressources de la base de données.<br/>                                                                                                          |
| [**Execute**](view-execute.md)   | Utilise le jeton de point d’interrogation pour représenter les paramètres dans une requête SQL. Les valeurs de ces paramètres sont transmises en tant que champs correspondants d’un enregistrement de paramètre.<br/> |
| [**Collecté**](view-fetch.md)       | Retourne un objet [**Record**](record-object.md) contenant les données de la colonne demandée si davantage de lignes sont disponibles dans le jeu de résultats, sinon retourne la valeur null.<br/>      |
| [**GetError**](view-geterror.md) | Retourne l’erreur de validation et le nom de la colonne pour laquelle l’erreur s’est produite.<br/>                                                                                           |
| [**Modifier**](view-modify.md)     | Modifie une ligne de base de données avec un objet [**enregistrement**](record-object.md) modifié obtenu à l’aide de la méthode [**Fetch**](view-fetch.md) .<br/>                                   |



 

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

[Exemples de scripts Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




