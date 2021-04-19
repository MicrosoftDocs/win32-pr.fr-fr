---
description: La méthode CreateTransformSummaryInfo de l’objet de base de données crée et remplit le flux d’informations de synthèse d’un fichier de transformation existant. Cette méthode remplit les propriétés avec les ProductCode et ProductVersion de base et de référence.
ms.assetid: 67df9b9c-0e7c-49a6-a35e-5196327d6aff
title: Database. CreateTransformSummaryInfo, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.CreateTransformSummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 824f46fd17eb51fddbf09c2f34569574c50c570a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541059"
---
# <a name="databasecreatetransformsummaryinfo-method"></a>Database. CreateTransformSummaryInfo, méthode

La méthode **CreateTransformSummaryInfo** de l’objet [**de base de données**](database-object.md) crée et remplit le flux d’informations de synthèse d’un fichier de transformation existant. Cette méthode remplit les propriétés avec les [**ProductCode**](productcode.md) et [**ProductVersion**](productversion.md)de base et de référence.

## <a name="syntax"></a>Syntaxe


```JScript
Database.CreateTransformSummaryInfo(
  reference,
  storage,
  errorConditions,
  validation
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*reference* 
</dt> <dd>

Base de données requise qui n’inclut pas les modifications.

</dd> <dt>

*storage* 
</dt> <dd>

Nom du fichier de transformation généré. Cette étape est facultative.

</dd> <dt>

*errorConditions* 
</dt> <dd>

Conditions d’erreur requises qui doivent être supprimées lors de l’application de la transformation. Combinez une ou plusieurs des valeurs de condition d’erreur suivantes.



| Nom de la condition d’erreur                                                                                                                                                                                                                                                                                                                                        | Signification                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="msiTransformErrorNone"></span><span id="msitransformerrornone"></span><span id="MSITRANSFORMERRORNONE"></span><dl> <dt>**msiTransformErrorNone**</dt> <dt>0</dt> </dl>                                                                         | Aucune des conditions suivantes.<br/>                                                |
| <span id="msiTransformErrorAddExistingRow"></span><span id="msitransformerroraddexistingrow"></span><span id="MSITRANSFORMERRORADDEXISTINGROW"></span><dl> <dt>**msiTransformErrorAddExistingRow**</dt> <dt>1</dt> </dl>                                 | Ajoute une ligne qui existe déjà.<br/>                                                  |
| <span id="msiTransformErrorDeleteNonExistingRow"></span><span id="msitransformerrordeletenonexistingrow"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorDeleteNonExistingRow**</dt> <dt>2</dt> </dl>         | Supprime une ligne qui n’existe pas.<br/>                                               |
| <span id="msiTransformErrorAddExistingTable"></span><span id="msitransformerroraddexistingtable"></span><span id="MSITRANSFORMERRORADDEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorAddExistingTable**</dt> <dt>4</dt> </dl>                         | Ajoute une table qui existe déjà.<br/>                                                |
| <span id="msiTransformErrorDeleteNonExistingTable"></span><span id="msitransformerrordeletenonexistingtable"></span><span id="MSITRANSFORMERRORDELETENONEXISTINGTABLE"></span><dl> <dt>**msiTransformErrorDeleteNonExistingTable**</dt> <dt>8</dt> </dl> | Supprime une table qui n’existe pas.<br/>                                             |
| <span id="msiTransformErrorUpdateNonExistingRow"></span><span id="msitransformerrorupdatenonexistingrow"></span><span id="MSITRANSFORMERRORUPDATENONEXISTINGROW"></span><dl> <dt>**msiTransformErrorUpdateNonExistingRow**</dt> <dt>16</dt> </dl>        | Met à jour une ligne qui n’existe pas.<br/>                                               |
| <span id="msiTransformErrorChangeCodepage"></span><span id="msitransformerrorchangecodepage"></span><span id="MSITRANSFORMERRORCHANGECODEPAGE"></span><dl> <dt>**msiTransformErrorChangeCodepage**</dt> <dt>32</dt> </dl>                                | Les pages de codes de transformation et de base de données ne correspondent pas et aucune page de codes n’est neutre.<br/> |



 

</dd> <dt>

*validation* 
</dt> <dd>

Obligatoire lorsque la transformation est appliquée à une base de données ; indique les propriétés qui doivent être validées pour vérifier que cette transformation peut être appliquée à la base de données. Les propriétés sont toutes contenues dans le [jeu de propriétés de flux d’informations de synthèse](summary-information-stream-property-set.md).

Combinez une ou plusieurs des valeurs suivantes.



| Indicateur de validation                                                                                                                                                                                                                                                                                                         | Signification                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="msiTransformValidationNone"></span><span id="msitransformvalidationnone"></span><span id="MSITRANSFORMVALIDATIONNONE"></span><dl> <dt>**msiTransformValidationNone**</dt> <dt>0</dt> </dl>                 | Aucune validation n’a été effectuée.<br/>                        |
| <span id="msiTransformValidationLanguage"></span><span id="msitransformvalidationlanguage"></span><span id="MSITRANSFORMVALIDATIONLANGUAGE"></span><dl> <dt>**msiTransformValidationLanguage**</dt> <dt>1</dt> </dl> | La langue par défaut doit correspondre à la base de données de base.<br/> |
| <span id="msiTransformValidationProduct"></span><span id="msitransformvalidationproduct"></span><span id="MSITRANSFORMVALIDATIONPRODUCT"></span><dl> <dt>**msiTransformValidationProduct**</dt> <dt>2</dt> </dl>     | Le produit doit correspondre à la base de données de base.<br/>          |



 

Pour valider la version du produit, commencez par choisir un ou plusieurs de ces trois indicateurs pour indiquer la quantité de la version à vérifier.



| Indicateur de validation                                                                                                                                                                                                                                                                                                              | Signification                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="msiTransformValidationMajorVer"></span><span id="msitransformvalidationmajorver"></span><span id="MSITRANSFORMVALIDATIONMAJORVER"></span><dl> <dt>**msiTransformValidationMajorVer**</dt> <dt>8</dt> </dl>      | Vérifie uniquement la version principale.<br/>                |
| <span id="msiTransformValidationMinorVer"></span><span id="msitransformvalidationminorver"></span><span id="MSITRANSFORMVALIDATIONMINORVER"></span><dl> <dt>**msiTransformValidationMinorVer**</dt> <dt>16</dt> </dl>     | Vérifie uniquement la version majeure et la version mineure.<br/>      |
| <span id="msiTransformValidationUpdateVer"></span><span id="msitransformvalidationupdatever"></span><span id="MSITRANSFORMVALIDATIONUPDATEVER"></span><dl> <dt>**msiTransformValidationUpdateVer**</dt> <dt>32</dt> </dl> | Vérifie les versions majeures, mineures et mises à jour.<br/> |



 

Choisissez ensuite l’une des options suivantes pour indiquer la relation requise entre la version du produit de la base de données à laquelle la transformation est appliquée et celle de la base de données de base.



| Indicateur de validation                                                                                                                                                                                                                                                                                                                                   | Signification                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="msiTransformValidationLess"></span><span id="msitransformvalidationless"></span><span id="MSITRANSFORMVALIDATIONLESS"></span><dl> <dt>**msiTransformValidationLess**</dt> <dt>64</dt> </dl>                                          | Version appliquée < version de base<br/>  |
| <span id="msiTransformValidationLessOrEqual"></span><span id="msitransformvalidationlessorequal"></span><span id="MSITRANSFORMVALIDATIONLESSOREQUAL"></span><dl> <dt>**msiTransformValidationLessOrEqual**</dt> <dt>128</dt> </dl>             | Version appliquée <= version de base<br/> |
| <span id="msiTransformValidationEqual"></span><span id="msitransformvalidationequal"></span><span id="MSITRANSFORMVALIDATIONEQUAL"></span><dl> <dt>**msiTransformValidationEqual**</dt> <dt>256</dt> </dl>                                     | Version appliquée = version de base<br/>     |
| <span id="msiTransformValidationGreaterOrEqual"></span><span id="msitransformvalidationgreaterorequal"></span><span id="MSITRANSFORMVALIDATIONGREATEROREQUAL"></span><dl> <dt>**msiTransformValidationGreaterOrEqual**</dt> <dt>512</dt> </dl> | Version appliquée >= version de base<br/> |
| <span id="msiTransformValidationGreater"></span><span id="msitransformvalidationgreater"></span><span id="MSITRANSFORMVALIDATIONGREATER"></span><dl> <dt>**msiTransformValidationGreater**</dt> <dt>1024</dt> </dl>                            | Version appliquée > version de base<br/>  |



 

Pour valider l’application de la transformation à un package ayant la [**UpgradeCode**](upgradecode.md)appropriée, définissez l’indicateur suivant.



| Indicateur de validation                                                                                                                                                                                                                                                                                                                        | Signification                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiTransformValidationUpgradeCode"></span><span id="msitransformvalidationupgradecode"></span><span id="MSITRANSFORMVALIDATIONUPGRADECODE"></span><dl> <dt>**msiTransformValidationUpgradeCode**</dt> <dt>2048</dt> </dl> | Valide le fait que la transformation soit la [**UpgradeCode**](upgradecode.md)appropriée.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour créer un flux d’informations de synthèse pour une transformation, les propriétés [**ProductCode**](productcode.md) et [**ProductVersion**](productversion.md) doivent être définies dans les tables de [Propriétés](property-table.md) des bases de données de base et de référence. Si msiTransformValidationUpgradeCode est utilisé, la propriété [**UpgradeCode**](upgradecode.md) doit être définie dans les deux bases de données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase est défini en tant que 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Transformations de base de données](database-transforms.md)
</dt> </dl>

 

 




