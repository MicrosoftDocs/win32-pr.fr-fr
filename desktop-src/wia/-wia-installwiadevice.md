---
description: la fonction InstallWiaDevice installe un appareil d’Acquisition d’images Windows (WIA) comme appareil énuméré à la racine. Il est possible qu’un message d’avertissement de sécurité s’indique si un programme d’installation ou un Coinstallateur n’est pas signé numériquement et approuvé.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Fonction InstallWiaDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallWiaDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 10006e234c9a76054a77fb64f89a31d9a21e394066bcc98813912bad9f804e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965838"
---
# <a name="installwiadevice-function"></a>InstallWiaDevice fonction)

la fonction **InstallWiaDevice** installe un appareil d’Acquisition d’images Windows (WIA) comme appareil énuméré à la racine. Il est possible qu’un message d’avertissement de sécurité s’indique si un programme d’installation ou un Coinstallateur n’est pas signé numériquement et approuvé.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pWiaDeviceInstall* \[ dans\]
</dt> <dd>

Type : **PWIADEVICEINSTALL \***

Pointeur vers une structure WIADEVICEINSTALL. Le membre *szFriendlyName* de la structure doit avoir la valeur de l’appareil FriendlyName réel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **DWORD**

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, elle retourne un code d’erreur Win32.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




