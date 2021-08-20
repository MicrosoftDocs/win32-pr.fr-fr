---
description: La méthode ApplyTransform de l’objet de base de données applique la transformation à cette base de données.
ms.assetid: bcf1ea78-54ad-49d9-8fba-7b88ced236eb
title: Database. ApplyTransform, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.ApplyTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9c3424dab82b6981af033b40b33481937fd7c36d3c00dcf3ddfcba5f13f56ec7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289619"
---
# <a name="databaseapplytransform-method"></a>Database. ApplyTransform, méthode

La méthode **ApplyTransform** de l’objet [**de base de données**](database-object.md) applique la transformation à cette base de données.

## <a name="syntax"></a>Syntaxe


```JScript
Database.ApplyTransform(
  storage,
  errorConditions
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*storage* 
</dt> <dd>

Chemin d’accès au fichier de transformation en cours d’application. Ce paramètre est obligatoire.

</dd> <dt>

*errorConditions* 
</dt> <dd>

Spécifie les conditions d’erreur qui doivent être supprimées. Spécifiez en tant que combinaison des valeurs entières suivantes.



| État d’erreur                                                                                                                                                                                                                                                                                                                                                  | Signification                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**msiTransformErrorAddExistingRow**</dt> <dt>0x0001</dt> </dl>                                 | Ajoute une ligne qui existe déjà.<br/>                                                     |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>0x0002</dt> </dl>         | Supprime une ligne qui n’existe pas.<br/>                                                  |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorAddExistingTable**</dt> <dt>0x0004</dt> </dl>                         | Ajoute une table qui existe déjà.<br/>                                                   |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>0x0008</dt> </dl> | Supprime une table qui n’existe pas.<br/>                                                |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>0x0010</dt> </dl>         | Met à jour une ligne qui n’existe pas.<br/>                                                  |
| <span id="msiTransformErrorChangeCodePage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**msiTransformErrorChangeCodePage**</dt> <dt>0x0020</dt> </dl>                                 | Les pages de codes de transformation et de base de données ne correspondent pas et n’ont aucune page de codes neutre.<br/> |
| <span id="msiTransformErrorViewTransform"></span><span id="msitransformerrorviewtransform"></span><span id="MSITRANSFORMERRORVIEWTRANSFORM"></span><dl> <dt>**msiTransformErrorViewTransform**</dt> <dt>0x0100</dt> </dl>                                     | Crée la [ \_ table TransformView](-transformview-table.md)temporaire.<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La méthode **ApplyTransform** retarde la transformation des tables jusqu’au dernier moment possible. Les étapes effectuées dans **ApplyTransform** sont de transformer immédiatement les catalogues de tables et de colonnes pour la base de données. Les catalogues de tables et de colonnes sont mis à jour en fonction de la table qui est ajoutée ou supprimée et de la colonne ajoutée (aucune suppression de colonnes n’est autorisée). Si une table est actuellement chargée en mémoire et doit être transformée, elle est transformée. Dans le cas contraire, l’état de la table a la valeur, ce qui nécessite une transformation, de sorte que lorsque la table est chargée, ou lorsque la base de données est validée, la transformation est appliquée. La transformation dans cette instance signifie que les données (ligne) réelles de la table sont ajoutées, supprimées ou mises à jour.

Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Base de données**](database-object.md)
</dt> <dt>

[Transformations de base de données](database-transforms.md)
</dt> </dl>

 

 




