---
description: La fonction InstallWiaDevice installe un appareil WIA (Windows Image Acquisition) comme périphérique énuméré à la racine. Il est possible qu’un message d’avertissement de sécurité s’indique si un programme d’installation ou un Coinstallateur n’est pas signé numériquement et approuvé.
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
ms.openlocfilehash: 62060d538b4b51fe22e10df09093f1f7f8c26a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752861"
---
# <a name="installwiadevice-function"></a>InstallWiaDevice fonction)

La fonction **InstallWiaDevice** installe un appareil WIA (Windows Image Acquisition) comme périphérique énuméré à la racine. Il est possible qu’un message d’avertissement de sécurité s’indique si un programme d’installation ou un Coinstallateur n’est pas signé numériquement et approuvé.

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

Tapez : **PWIADEVICEINSTALL \** _

Pointeur vers une structure WIADEVICEINSTALL. Le membre _szFriendlyName * de la structure doit avoir la valeur de l’appareil FriendlyName réel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **DWORD**

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, elle retourne un code d’erreur Win32.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




