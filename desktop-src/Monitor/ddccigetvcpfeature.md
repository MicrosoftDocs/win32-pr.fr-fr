---
title: DDCCIGetVCPFeature fonction)
description: Obtient la valeur actuelle, la valeur maximale et le type de code d’un code du panneau de configuration virtuel (VCP) pour une analyse.
ms.assetid: 7749d45c-a0d5-44ee-8f91-811677cbf59f
keywords:
- Configuration de l’analyse de fonction DDCCIGetVCPFeature
topic_type:
- apiref
api_name:
- DDCCIGetVCPFeature
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5758bbd1c86b9f228b64063fdd05c04cb05bedcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942100"
---
# <a name="ddccigetvcpfeature-function"></a>DDCCIGetVCPFeature fonction)

> [!IMPORTANT]
> Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage. Les applications ne doivent pas appeler cette fonction.

 

Obtient la valeur actuelle, la valeur maximale et le type de code d’un code du panneau de configuration virtuel (VCP) pour une analyse.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI DDCCIGetVCPFeature(
  _In_      HANDLE             hMonitor,
  _In_      DWORD              dwVCPCode,
  _Out_opt_ LPMC_VCP_CODE_TYPE pvct,
  _Out_     DWORD              *pdwCurrentValue,
  _Out_opt_ DWORD              *pdwMaximumValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMonitor* \[ dans\]
</dt> <dd>

Handle d’une analyse physique.

</dd> <dt>

*dwVCPCode* \[ dans\]
</dt> <dd>

Code VCP à interroger.

</dd> <dt>

*pvct* \[ out, facultatif\]
</dt> <dd>

Reçoit le type de code VCP, en tant que membre de l’énumération de [**\_ \_ \_ type de code VCP MD**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ne-lowlevelmonitorconfigurationapi-mc_vcp_code_type) .

</dd> <dt>

*pdwCurrentValue* \[ à\]
</dt> <dd>

Reçoit la valeur actuelle du code VCP.

</dd> <dt>

*pdwMaximumValue* \[ out, facultatif\]
</dt> <dd>

Reçoit la valeur maximale du code VCP.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, elle retourne l' **état \_ Success**. Sinon, elle retourne un code d’erreur **NTSTATUS** .

## <a name="remarks"></a>Notes

Les applications doivent appeler [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) au lieu d’appeler cette fonction.

Cette fonction n’a pas de bibliothèque d’importation associée. Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Surveiller les fonctions de configuration](monitor-configuration-functions.md)
</dt> </dl>

 

