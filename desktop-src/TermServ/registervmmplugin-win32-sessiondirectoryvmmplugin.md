---
title: Méthode RegisterVMMPlugin de la classe Win32_SessionDirectoryVMMPlugin
description: Inscrit un nouveau plug-in VMM.
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RegisterVMMPlugin
- Services Bureau à distance de la méthode RegisterVMMPlugin, classe Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance, méthode RegisterVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384279"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Méthode RegisterVMMPlugin de la \_ classe Win32 SessionDirectoryVMMPlugin

Inscrit un nouveau plug-in VMM.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sName* \[ dans\]
</dt> <dd>

Nom du plug-in.

</dd> <dt>

*sProvider* \[ dans\]
</dt> <dd>

Nom du fournisseur de plug-ins.

</dd> <dt>

*sServiceLocation* \[ dans\]
</dt> <dd>

Emplacement du service que le plug-in doit contacter.

</dd> <dt>

*sClassID* \[ dans\]
</dt> <dd>

Identificateur de classe du plug-in.

</dd> <dt>

*Priorité* \[ dans\]
</dt> <dd>

Priorité du plug-in. Plus la valeur est élevée, plus la priorité du plug-in est élevée.

</dd> <dt>

*Activé* \[ dans\]
</dt> <dd>

Indique si le plug-in est activé ou désactivé. **True** si le plug-in est activé ou **false** dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                      |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SessionDirectoryVMMPlugin Win32**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





