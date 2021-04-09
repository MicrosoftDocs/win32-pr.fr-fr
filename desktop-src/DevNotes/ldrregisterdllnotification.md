---
description: Enregistre une notification lorsqu’une DLL est chargée pour la première fois. Cette notification se produit avant que la liaison dynamique ait lieu.
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: LdrRegisterDllNotification fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033597"
---
# <a name="ldrregisterdllnotification-function"></a>LdrRegisterDllNotification fonction)

\[Cette fonction peut être modifiée ou supprimée de Windows sans préavis.\]

Enregistre une notification lorsqu’une DLL est chargée pour la première fois. Cette notification se produit avant que la liaison dynamique ait lieu.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Ce paramètre doit être égal à zéro.

</dd> <dt>

*NotificationFunction* \[ dans\]
</dt> <dd>

Pointeur vers une fonction de rappel de notification [*LdrDllNotification*](ldrdllnotification.md) à appeler lorsque la dll est chargée.

</dd> <dt>

*Contexte* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers les données de contexte pour la fonction de rappel.

</dd> <dt>

*Cookie* \[ à\]
</dt> <dd>

Pointeur vers une variable qui doit recevoir un identificateur pour la fonction de rappel. Cet identificateur est utilisé pour annuler l’inscription de la fonction de rappel de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, elle retourne l' **état \_ Success**.

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

[*LdrDllNotification*](ldrdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
