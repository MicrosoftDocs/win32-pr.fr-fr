---
title: Méthode GetCurrentVMMPlugin de la classe Win32_SessionDirectoryVMMPlugin
description: Obtient le plug-in avec la priorité la plus élevée qui est activé.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetCurrentVMMPlugin
- Services Bureau à distance de la méthode GetCurrentVMMPlugin, classe Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance, méthode GetCurrentVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7162322f4e5e3939309d64e27c93cf8d20da540c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844314"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Méthode GetCurrentVMMPlugin de la \_ classe Win32 SessionDirectoryVMMPlugin

Obtient le plug-in avec la priorité la plus élevée qui est activé.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sName* \[ à\]
</dt> <dd>

Nom du plug-in.

</dd> <dt>

*sProvider* \[ à\]
</dt> <dd>

Nom du fournisseur de plug-ins.

</dd> <dt>

*sServiceLocation* \[ à\]
</dt> <dd>

Emplacement du service que le plug-in doit contacter.

</dd> <dt>

*sClassID* \[ à\]
</dt> <dd>

Identificateur de classe du plug-in.

</dd> <dt>

*Priorité* \[ à\]
</dt> <dd>

Priorité du plug-in. Plus la valeur est élevée, plus la priorité du plug-in est élevée.

</dd> <dt>

*Activé* \[ à\]
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

 

 





