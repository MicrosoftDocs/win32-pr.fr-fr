---
description: Annule la notification de chargement de la DLL précédemment inscrite en appelant la fonction LdrRegisterDllNotification.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: LdrUnregisterDllNotification fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392923"
---
# <a name="ldrunregisterdllnotification-function"></a>LdrUnregisterDllNotification fonction)

\[Cette fonction peut être modifiée ou supprimée de Windows sans préavis.\]

Annule la notification de chargement de la DLL précédemment inscrite en appelant la fonction [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) .

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Cookie* \[ dans\]
</dt> <dd>

Pointeur vers l’identificateur de rappel reçu de l’appel de [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) qui s’est inscrit pour la notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un code **NTSTATUS** ou d’erreur.

Si la fonction réussit, elle retourne l' **état \_ Success**.

Si la fonction de rappel est introuvable, la fonction retourne la **dll d’état \_ \_ \_ introuvable**.

Les formulaires et la signification des codes d’erreur de **NTSTATUS** sont répertoriés dans le fichier d’en-tête Ntstatus. h disponible dans le kit WDK et sont décrits dans la documentation WDK.

## <a name="remarks"></a>Notes

Cette fonction n’a aucun fichier d’en-tête associé. La bibliothèque d’importation associée, ntdll. lib, est disponible dans le kit WDK. Vous pouvez également utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> </dl>

 

 
