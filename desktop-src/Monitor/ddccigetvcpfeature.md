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
ms.openlocfilehash: 15549d69bb446d7a7e6d5c44517bade3e9158d1a6d5f9b9ae839d6b1b547717a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640997"
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

## <a name="remarks"></a>Remarques

Les applications doivent appeler [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) au lieu d’appeler cette fonction.

Cette fonction n’a pas de bibliothèque d’importation associée. Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Surveiller les fonctions de configuration](monitor-configuration-functions.md)
</dt> </dl>

 

