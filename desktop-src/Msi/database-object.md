---
description: L’objet de base de données accède à une base de données du programme d’installation.
ms.assetid: 97765884-3e1c-486a-932c-6430b113fac8
title: Objet de base de données
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5b47e4678d9475abe90c4b55d6adb514314dcc0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537895"
---
# <a name="database-object"></a>Objet de base de données

L’objet **de base de données** accède à une base de données du programme d’installation.

L’objet **de base de données** est libéré lorsqu’il est retiré de l’étendue ou lorsque la variable objet associée est définie sur null. La méthode de [**validation**](database-commit.md) doit être appelée avant que l’objet **de base de données** ne soit libéré pour écrire toutes les modifications persistantes. Si la méthode de **validation** n’est pas appelée, le programme d’installation effectue une restauration implicite lors de la destruction de l’objet.

Le client peut utiliser la procédure suivante pour l’accès aux données.

**Pour interroger l’API de séquencement**

1.  Obtenez un objet **de base de données** en appelant l’objet [**OpenDatabase**](installer-opendatabase.md) ou le [**programme d’installation**](installer-object.md) .
2.  Lancez une requête à l’aide d’une chaîne SQL en appelant la méthode [**OpenView**](database-openview.md) de l’objet **de base de données** .
3.  Définissez les paramètres de requête dans un objet [**enregistrement**](record-object.md) et exécutez la requête de base de données en appelant la méthode [**Execute**](view-execute.md) de l’objet [**View**](view-object.md) . Cela génère un résultat qui peut être extrait ou mis à jour.
4.  Appelez la méthode [**Fetch**](view-fetch.md) de l’objet [**View**](view-object.md) à plusieurs reprises pour retourner des objets [**Record**](record-object.md) .
5.  Met à jour les lignes de base de données d’un objet [**Record**](record-object.md) obtenu par la méthode [**Fetch**](view-fetch.md) à l’aide de la méthode [**Modify**](view-modify.md) de l’objet [**View**](view-object.md) .
6.  Libérez la requête et tous les enregistrements non récupérés en appelant la méthode [**Close**](view-close.md) de l’objet [**View**](view-object.md) .
7.  Conservez toutes les mises à jour de base de données en appelant la méthode [**Commit**](database-commit.md) de l’objet **Database** .

## <a name="members"></a>Membres

L’objet **de base de données** a les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **de base de données** a ces méthodes.



| Méthode                                                                    | Description                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyTransform**](database-applytransform.md)                         | Applique la transformation à cette base de données.<br/>                                                                                                                        |
| [**Commit**](database-commit.md)                                         | Finalise la forme persistante de la base de données.<br/>                                                                                                                 |
| [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) | Crée et remplit le flux d’informations de synthèse d’un fichier de transformation existant.<br/>                                                                            |
| [**EnableUIPreview**](database-enableuipreview.md)                       | Facilite la création de boîtes de dialogue et de panneaux en fournissant la prise en charge nécessaire pour afficher les boîtes de dialogue de l’interface utilisateur stockées dans la base de données du programme d’installation.<br/> |
| [**Exporter**](database-export.md)                                         | Copie la structure et les données d’une table spécifiée dans un fichier d’archive de texte.<br/>                                                                                   |
| [**GenerateTransform**](database-generatetransform.md)                   | Crée une transformation.<br/>                                                                                                                                           |
| [**Importer**](database-import.md)                                         | Importe une table de base de données à partir d’un fichier d’archive de texte.<br/>                                                                                                             |
| [**Fusion**](database-merge.md)                                           | Fusionne la base de données de référence avec la base de données de base.<br/>                                                                                                          |
| [**OpenView**](database-openview.md)                                     | Retourne un objet de [**vue**](view-object.md) représentant la requête spécifiée par une chaîne SQL.<br/>                                                                 |



 

### <a name="properties"></a>Propriétés

L’objet **de base de données** a ces propriétés.



| Propriété                                                                               | Description                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DatabaseState**](database-databasestate.md)<br/>                             | Retourne l’état de persistance de la base de données.<br/>                                                                                                        |
| [**PrimaryKeys**](database-primarykeys.md)<br/>                                 | Retourne un objet [**Record**](record-object.md) contenant le nom de la table et les noms des colonnes (qui composent les clés primaires).<br/>                        |
| [**SummaryInformation (objet de base de données)**](database-summaryinformation.md)<br/> | Retourne un objet [**SummaryInfo**](summaryinfo-object.md) qui peut être utilisé pour examiner, mettre à jour et ajouter des propriétés au flux d’informations de synthèse.<br/> |
| [**TablePersistent**](database-tablepersistent.md)<br/>                         | Retourne l’état de persistance de la table.<br/>                                                                                                           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Exemples de scripts Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




