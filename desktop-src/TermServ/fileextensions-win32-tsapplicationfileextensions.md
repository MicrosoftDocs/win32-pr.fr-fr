---
title: Méthode FileExtensions de la classe Win32_TSApplicationFileExtensions
description: Fournit une liste des extensions de nom de fichier qui sont gérées par une application.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode FileExtensions
- Services Bureau à distance de la méthode FileExtensions, classe Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions de la classe Services Bureau à distance, méthode FileExtensions
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c7c44acd410566c4f048cdf36bac904c18b21df42f53543051e3b94f49bfbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609371"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a>Méthode FileExtensions de la \_ classe Win32 TSApplicationFileExtensions

Fournit une liste des extensions de nom de fichier qui sont gérées par une application.

## <a name="syntax"></a>Syntaxe


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Chemin* \[ dans\]
</dt> <dd>

Chemin d'accès de l'application.

</dd> <dt>

*Extensions* \[ à\]
</dt> <dd>

Extensions de nom de fichier gérées par l’application.

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

[**\_TSApplicationFileExtensions Win32**](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

