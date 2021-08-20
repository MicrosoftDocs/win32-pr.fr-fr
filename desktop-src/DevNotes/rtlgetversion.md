---
description: Obtient des informations de version sur le système d’exploitation en cours d’exécution.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: RtlGetVersion, fonction (Ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: 7420b9dba03e3b136331f4463f476908882ca5564d0fc7ac563036c7acccb356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161681"
---
# <a name="rtlgetversion-function"></a>RtlGetVersion fonction)

Obtient des informations de version sur le système d’exploitation en cours d’exécution.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpVersionInformation* \[ à\]
</dt> <dd>

Pointeur vers une structure [**\_ OSVERSIONINFOW RTL**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) ou une structure [**\_ OSVERSIONINFOEXW RTL**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) qui contient les informations de version relatives au système d’exploitation en cours d’exécution. Un appelant spécifie la structure d’entrée utilisée en affectant à la taille du membre **dwOSVersionInfoSize** de la structure la taille en octets de la structure utilisée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’état \_ réussite.

## <a name="remarks"></a>Remarques

**RtlGetVersion** est l’équivalent de la fonction [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) dans le SDK Windows. consultez l’exemple dans le SDK Windows qui montre comment obtenir la version du système.

Quand vous utilisez **RtlGetVersion** pour déterminer si une version particulière du système d’exploitation est en cours d’exécution, un appelant doit vérifier les numéros de version qui sont supérieurs ou égaux au numéro de version requis. Cela garantit qu’un test de version est correctement effectué pour les versions ultérieures de Windows.

Étant donné que les fonctionnalités du système d’exploitation peuvent être ajoutées à une DLL redistribuable, la vérification des numéros de version majeure et mineure n’est pas la méthode la plus fiable pour vérifier la présence d’une fonctionnalité système spécifique. Un pilote doit utiliser [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) pour tester la présence d’une fonctionnalité système spécifique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| Plateforme cible<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl>                  |
| En-tête<br/>                   | <dl> <dt>Ntddk. h (inclure Ntddk. h)</dt> </dl>                                                     |
| Bibliothèque<br/>                  | <dl> <dt>Ntdll. lib ; </dt> <dt>NtosKrnl. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll ; </dt> <dt>NtosKrnl.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PsGetVersion**](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 
