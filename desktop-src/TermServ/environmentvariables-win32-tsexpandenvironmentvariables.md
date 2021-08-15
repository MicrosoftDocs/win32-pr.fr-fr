---
title: Méthode EnvironmentVariables de la classe Win32_TSExpandEnvironmentVariables
description: Développe les variables d’environnement définies par le système. | Méthode EnvironmentVariables de la classe Win32_TSExpandEnvironmentVariables
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnvironmentVariables
- Services Bureau à distance de la méthode EnvironmentVariables, classe Win32_TSExpandEnvironmentVariables
- Win32_TSExpandEnvironmentVariables de la classe Services Bureau à distance, méthode EnvironmentVariables
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49416291293d621739ab7c721ca349f5d87bb4582d1289f431a8c443d3414da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353891"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a>Méthode EnvironmentVariables de la \_ classe Win32 TSExpandEnvironmentVariables

Développe les variables d’environnement définies par le système.

## <a name="syntax"></a>Syntaxe


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*OriginalString* \[ dans\]
</dt> <dd>

Chaîne qui contient les variables d’environnement à développer.

</dd> <dt>

*ExpandedString* \[ à\]
</dt> <dd>

Chaîne avec les variables d’environnement développées.

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSExpandEnvironmentVariables Win32**](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

