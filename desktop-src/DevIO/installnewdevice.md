---
description: Installe un nouvel appareil. L’utilisateur est invité à sélectionner l’appareil.
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: InstallNewDevice fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: cb12e87ceee4812ffc8c0e39d961ce631e26c4ab8ca7ae555785c8ad8381ca01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405306"
---
# <a name="installnewdevice-function"></a>InstallNewDevice fonction)

Installe un nouvel appareil. L’utilisateur est invité à sélectionner l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Handle de la fenêtre de niveau supérieur à utiliser pour toute interface utilisateur requise.

</dd> <dt>

*ClassGuid* \[ dans\]
</dt> <dd>

Pointeur vers un **GUID** de classe. Ce paramètre est facultatif. Si ce paramètre a la **valeur null**, l’utilisateur démarre sur la page choix de détection. Si ce paramètre est **\_ null GUID** ou **GUID \_ DEVCLASS \_ Unknown**, l’utilisateur démarre sur la page de sélection de la classe.

</dd> <dt>

*prédémarrage* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit l’état de redémarrage. Ce paramètre peut être **di \_ NEEDRESTART** ou **di \_ NEEDREBOOT**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation associée. Vous devez utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à NewDev.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2003<br/>                                                        |
| DLL<br/>                      | <dl> <dt>NewDev.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de gestion des appareils](device-management-functions.md)
</dt> </dl>

 

