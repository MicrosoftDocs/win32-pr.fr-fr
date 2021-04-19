---
description: La méthode RegistryValue de l’objet installer lit les informations relatives à une clé de Registre spécifiée de valeur.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Installer. RegistryValue, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6da79ff08eebe62ad177119a35bfc29b21c9350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543205"
---
# <a name="installerregistryvalue-method"></a>Installer. RegistryValue, méthode

La méthode **RegistryValue** de l’objet [**installer**](installer-object.md) lit les informations relatives à une clé de Registre spécifiée de valeur. Si la clé ou la valeur spécifiée n’existe pas, la méthode retourne une erreur 9, « indice hors limites ».

## <a name="syntax"></a>Syntaxe


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*root* 
</dt> <dd>

Dans Windows NT 4,0, la racine du Registre est soit une clé racine numérique, soit un nom d’ordinateur en tant que chaîne. Les noms d’ordinateur sont toujours des chaînes. Dans Windows 95, Windows 98 ou Windows Me, la racine du Registre est une clé racine numérique uniquement. Vous pouvez uniquement accéder à HKLM sur une machine distante.



| Root                                                                                                                                                                                   | Signification      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <dt>**\_racine des classes HKEY \_**</dt> </dl>             | 0<br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <dt>**HKEY \_ Current \_ User**</dt> </dl>             | 1<br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <dt>**HKEY \_ local \_ machine**</dt> </dl>          | 2<br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <dt>**HKEY, \_ utilisateurs**</dt> </dl>                                   | 3<br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <dt>**\_données de performances HKEY \_**</dt> </dl> | 4<br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <dt>**configuration de HKEY \_ Current \_**</dt> </dl>       | 5<br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <dt>**\_données HKEY dyn \_**</dt> </dl>                         | 6<br/> |



 

</dd> <dt>

*key* 
</dt> <dd>

Chaîne contenant le chemin d’accès complet à la clé à partir de la racine.

</dd> <dt>

*value* 
</dt> <dd>

Ce paramètre facultatif désigne la valeur associée à retourner pour la clé spécifiée. La valeur est l’une des valeurs indiquées dans le tableau suivant.



| Valeur                                                                                                                                                                                                    | Signification                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <dt>**Manquant ou vide**</dt> </dl> | Retourne une valeur booléenne désignant si la clé existe.<br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>**String**</dt> </dl>                                         | Retourne les données associées à la valeur nommée, échoue si le nom de la valeur n’existe pas.<br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <dt>**Entier positif**</dt> </dl> | Retourne le nom de la valeur énumérée de base 1, il est vide s’il n’existe pas. Cette option utilise la fonction [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) .<br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <dt>**Entier négatif**</dt> </dl> | Retourne le nom de la sous-clé énumérée de base 1, ce qui est vide s’il n’existe pas. Cette option utilise la fonction [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) .<br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <dt>**Entier zéro**</dt> </dl>                 | Retourne le nom de la classe de chaîne pour la clé désignée.<br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <dt>**Chaîne vide ""**</dt> </dl> | Retourne la valeur par défaut de la clé de registre.<br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 
