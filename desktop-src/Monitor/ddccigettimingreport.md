---
title: DDCCIGetTimingReport fonction)
description: Obtient les fréquences de synchronisation horizontale et verticale d’une analyse.
ms.assetid: d490cb89-082a-42a1-ac0a-335c929cd5d7
keywords:
- Configuration de l’analyse de fonction DDCCIGetTimingReport
topic_type:
- apiref
api_name:
- DDCCIGetTimingReport
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 930149ebc2acfa69f479c889c6fa2c33acdfb3f528a67f83ee0bfbe7ab0467a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382362"
---
# <a name="ddccigettimingreport-function"></a>DDCCIGetTimingReport fonction)

> [!IMPORTANT]
> Cette fonction est utilisée par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage. Les applications ne doivent pas appeler cette fonction.

 

Obtient les fréquences de synchronisation horizontale et verticale d’une analyse.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI DDCCIGetTimingReport(
  _In_  HANDLE             hMonitor,
  _Out_ LPMC_TIMING_REPORT pmtr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMonitor* \[ dans\]
</dt> <dd>

Handle d’une analyse physique.

</dd> <dt>

*PMTR* \[ à\]
</dt> <dd>

Pointeur vers une structure [**de \_ \_ rapport de minutage MC**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/ns-lowlevelmonitorconfigurationapi-mc_timing_report) qui reçoit les informations de minutage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, elle retourne l' **état \_ Success**. Sinon, elle retourne un code d’erreur **NTSTATUS** .

## <a name="remarks"></a>Remarques

Les applications doivent appeler [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport) au lieu d’appeler cette fonction.

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

 

