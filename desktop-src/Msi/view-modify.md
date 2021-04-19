---
description: La méthode modify de l’objet View modifie une ligne de base de données avec un objet record modifié obtenu à l’aide de la méthode fetch.
ms.assetid: c3c500aa-070f-41d7-90f7-db979452d24f
title: View. Modify, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Modify
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b4dc97f2e3b5f85d472cfcbfad6017ce4e051e4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536038"
---
# <a name="viewmodify-method"></a>View. Modify, méthode

La méthode **Modify** de l’objet [**View**](view-object.md) modifie une ligne de base de données avec un objet [**Record**](record-object.md) modifié obtenu à l’aide de la méthode [**Fetch**](view-fetch.md) .

## <a name="syntax"></a>Syntaxe


```JScript
View.Modify(
  action,
  record
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*action* 
</dt> <dd>

Action requise à effectuer sur la ligne de la base de données. Cette action est l’une de celles répertoriées dans le tableau suivant.



| Nom de l'action                                                                                                                                                                                                                                                                                                     | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiViewModifySeek"></span><span id="msiviewmodifyseek"></span><span id="MSIVIEWMODIFYSEEK"></span><dl> <dt>**msiViewModifySeek**</dt> <dt>– 1</dt> </dl>                                            | Actualise les informations de l’enregistrement fourni sans modifier la position dans le jeu de résultats et sans affecter les opérations d’extraction ultérieures. L’enregistrement peut ensuite être utilisé pour la mise à jour, la suppression et l’actualisation ultérieures. Toutes les colonnes de clé primaire de la table doivent être dans la requête et l’enregistrement doit avoir au moins autant de champs que la requête. La recherche ne peut pas être utilisée avec des requêtes multitables. Consultez les notes. Ce mode ne peut pas être utilisé avec une vue contenant des jointures.<br/>                                                                             |
| <span id="msiViewModifyRefresh"></span><span id="msiviewmodifyrefresh"></span><span id="MSIVIEWMODIFYREFRESH"></span><dl> <dt>**msiViewModifyRefresh**</dt> <dt>0</dt> </dl>                                 | Actualise les informations de l’enregistrement. Vous devez d’abord appeler la méthode [**Fetch**](view-fetch.md) avec le même enregistrement. Échoue pour une ligne supprimée. Fonctionne avec les enregistrements en lecture-écriture et en lecture seule.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyInsert"></span><span id="msiviewmodifyinsert"></span><span id="MSIVIEWMODIFYINSERT"></span><dl> <dt>**msiViewModifyInsert**</dt> <dt>1</dt> </dl>                                     | Insère un enregistrement. Échoue s’il existe une ligne avec les mêmes clés primaires. Échoue avec une base de données en lecture seule. Ce mode ne peut pas être utilisé avec une vue contenant des jointures.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="msiViewModifyUpdate"></span><span id="msiviewmodifyupdate"></span><span id="MSIVIEWMODIFYUPDATE"></span><dl> <dt>**msiViewModifyUpdate**</dt> <dt>2</dt> </dl>                                     | Met à jour un enregistrement existant. Clés non primaires uniquement. Vous devez d’abord appeler la méthode [**Fetch**](view-fetch.md) avec le même enregistrement. Échoue avec un enregistrement supprimé. Fonctionne uniquement avec les enregistrements en lecture-écriture.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyAssign"></span><span id="msiviewmodifyassign"></span><span id="MSIVIEWMODIFYASSIGN"></span><dl> <dt>**msiViewModifyAssign**</dt> <dt>3</dt> </dl>                                     | Écrit les données actuelles du curseur dans une ligne de table. Met à jour l’enregistrement si les clés primaires correspondent à une ligne existante et s’insert si elles ne correspondent pas. Échoue avec une base de données en lecture seule. Ce mode ne peut pas être utilisé avec une vue contenant des jointures.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiViewModifyReplace"></span><span id="msiviewmodifyreplace"></span><span id="MSIVIEWMODIFYREPLACE"></span><dl> <dt>**msiViewModifyReplace**</dt> <dt>4</dt> </dl>                                 | Met à jour ou supprime et insère un enregistrement dans une table. Vous devez d’abord appeler la méthode [**Fetch**](view-fetch.md) avec le même enregistrement. Met à jour l’enregistrement si les clés primaires sont inchangées. Supprime l’ancienne ligne et insère New si les clés primaires ont été modifiées. Échoue avec une base de données en lecture seule. Ce mode ne peut pas être utilisé avec une vue contenant des jointures.<br/>                                                                                                                                                                                                           |
| <span id="msiViewModifyMerge"></span><span id="msiviewmodifymerge"></span><span id="MSIVIEWMODIFYMERGE"></span><dl> <dt>**msiViewModifyMerge**</dt> <dt>5</dt> </dl>                                         | Insère ou valide un enregistrement dans une table. Insère si les clés primaires ne correspondent à aucune ligne et vérifie s’il existe une correspondance. Échoue si l’enregistrement ne correspond pas aux données de la table. Échoue s’il existe un enregistrement avec une clé dupliquée qui n’est pas identique. Fonctionne uniquement avec les enregistrements en lecture-écriture. Ce mode ne peut pas être utilisé avec une vue contenant des jointures.<br/>                                                                                                                                                                                                |
| <span id="msiViewModifyDelete"></span><span id="msiviewmodifydelete"></span><span id="MSIVIEWMODIFYDELETE"></span><dl> <dt>**msiViewModifyDelete**</dt> <dt>6</dt> </dl>                                     | Supprime une ligne de la table. Vous devez d’abord appeler la méthode [**Fetch**](view-fetch.md) avec le même enregistrement. Échoue si la ligne a été supprimée. Fonctionne uniquement avec les enregistrements en lecture-écriture. Ce mode ne peut pas être utilisé avec une vue contenant des jointures.<br/>                                                                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyInsertTemporary"></span><span id="msiviewmodifyinserttemporary"></span><span id="MSIVIEWMODIFYINSERTTEMPORARY"></span><dl> <dt>**msiViewModifyInsertTemporary**</dt> <dt>7</dt> </dl> | Insère un enregistrement temporaire. Les informations ne sont pas persistantes. Échoue s’il existe une ligne avec la même clé primaire. Fonctionne uniquement avec les enregistrements en lecture-écriture. Ce mode ne peut pas être utilisé avec une vue contenant des jointures.<br/>                                                                                                                                                                                                                                                                                                                                           |
| <span id="msiViewModifyValidate"></span><span id="msiviewmodifyvalidate"></span><span id="MSIVIEWMODIFYVALIDATE"></span><dl> <dt>**msiViewModifyValidate**</dt> <dt>8</dt> </dl>                             | Valide un enregistrement. N’effectue pas de validation sur les jointures. Vous devez d’abord appeler la méthode [**Fetch**](view-fetch.md) avec le même enregistrement. Obtenez des erreurs de validation à l’aide de la méthode [**GetError**](view-geterror.md) . Fonctionne avec les enregistrements en lecture-écriture et en lecture seule. Ce mode ne peut pas être utilisé avec une vue contenant des jointures.<br/>                                                                                                                                                                                                                                         |
| <span id="msiViewModifyValidateNew"></span><span id="msiviewmodifyvalidatenew"></span><span id="MSIVIEWMODIFYVALIDATENEW"></span><dl> <dt>**msiViewModifyValidateNew**</dt> <dt>9</dt> </dl>                 | Valide un nouvel enregistrement. N’effectue pas de validation sur les jointures. Recherche les clés dupliquées. Obtient des erreurs de validation en appelant la méthode [**GetError**](view-geterror.md) . Nécessite l’appel de la méthode [**MsiDatabase. OpenView**](database-openview.md) avec une valeur de modification. Fonctionne avec les enregistrements en lecture-écriture et en lecture seule. Ce mode ne peut pas être utilisé avec une vue contenant des jointures.<br/>                                                                                                                                                                                 |
| <span id="msiViewModifyValidateField"></span><span id="msiviewmodifyvalidatefield"></span><span id="MSIVIEWMODIFYVALIDATEFIELD"></span><dl> <dt>**msiViewModifyValidateField**</dt> <dt>10</dt> </dl>        | Valide les champs d’un enregistrement extrait ou nouveau. Peut valider un ou plusieurs champs d’un enregistrement incomplet. Obtient des erreurs de validation en appelant la méthode [**GetError**](view-geterror.md) . Fonctionne avec les enregistrements en lecture-écriture et en lecture seule. Ce mode ne peut pas être utilisé avec une vue contenant des jointures.<br/>                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyValidateDelete"></span><span id="msiviewmodifyvalidatedelete"></span><span id="MSIVIEWMODIFYVALIDATEDELETE"></span><dl> <dt>**msiViewModifyValidateDelete**</dt> <dt>11</dt> </dl>    | Valide un enregistrement qui sera supprimé ultérieurement. Vous devez d’abord appeler la méthode [**Fetch**](view-fetch.md) avec le même enregistrement. Échoue si une autre ligne fait référence aux clés primaires de cette ligne. La validation ne vérifie pas l’existence des clés primaires de cette ligne dans les propriétés ou les chaînes. Ne vérifie pas si une colonne est une clé étrangère pour plusieurs tables. Obtenez des erreurs de validation en appelant la méthode [**GetError**](view-geterror.md) . Fonctionne avec les enregistrements en lecture-écriture et en lecture seule. Ce mode ne peut pas être utilisé avec une vue contenant des jointures.<br/> |



 

</dd> <dt>

*enregistrement* 
</dt> <dd>

Obligatoire. Objet [**Record**](record-object.md) obtenu par la méthode [**Fetch**](view-fetch.md) avec les données de champ modifiées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode doit être appelée après la méthode [**Execute**](view-execute.md) .

Pour exécuter une instruction SQL, vous devez créer une vue. Toutefois, une vue qui ne crée pas de jeu de résultats, comme CREATE TABLE ou INSERT INTO, ne peut pas être utilisée avec la méthode **Modify** pour mettre à jour des tables via la vue.

Les valeurs msiViewModifyValidate, msiViewModifyValidateNew, msiViewModifyValidateField et msiViewModifyValidateDelete de la méthode **Modify** n’effectuent pas de mises à jour réelles. ils garantissent que les données de l’enregistrement sont valides. L’utilisation de ces actions nécessite que la base de données contienne une [ \_ table de validation](-validation-table.md) .

Vous ne pouvez pas extraire un enregistrement contenant des données binaires d’une base de données, puis utiliser cet enregistrement pour insérer les données dans une base de données complètement différente. Pour déplacer des données binaires d’une base de données vers une autre, exportez les données vers un fichier, puis importez-les dans la nouvelle base de données à l’aide de la méthode [**SetStream**](record-setstream.md) de l’objet [**Record**](record-object.md) . Cela garantit que chaque base de données possède sa propre copie des données binaires.

> [!Note]  
> Les actions personnalisées peuvent uniquement ajouter, modifier ou supprimer des lignes, des colonnes ou des tables temporaires dans une base de données. Les actions personnalisées ne peuvent pas modifier les données persistantes dans une base de données, telles que les données qui font partie de la base de données stockée sur le disque. Pour plus d’informations, consultez [accès à la session de programme d’installation actuelle à partir d’une action personnalisée](accessing-the-current-installer-session-from-inside-a-custom-action.md).

 

Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | L’IID \_ IView est défini en tant que 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




