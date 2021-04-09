---
description: Fonction de rappel de notification spécifiée avec la fonction LdrRegisterDllNotification.
ms.assetid: 12202797-c80c-4fa3-9cc4-dcb1a9f01551
title: LdrDllNotification fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrDllNotification
- PLDR_DLL_NOTIFICATION_FUNCTION
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e29cd7b17c634250f56cbafcf86379449ac88199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846990"
---
# <a name="ldrdllnotification-callback-function"></a>LdrDllNotification fonction de rappel

\[Cette fonction peut être modifiée ou supprimée de Windows sans préavis.\]

Fonction de rappel de notification spécifiée avec la fonction [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) . Le chargeur appelle cette fonction lorsqu’une DLL est chargée pour la première fois.

**Avertissement :** Il n’est pas sûr que la fonction de rappel de notification appelle des fonctions dans une DLL.

## <a name="syntax"></a>Syntaxe


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NotificationReason* \[ dans\]
</dt> <dd>

Raison pour laquelle la fonction de rappel de notification a été appelée. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                        | Signification                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <dt>**LDR \_ Raison de la \_ notification dll \_ \_ chargée**</dt> <dt>1</dt> </dl>       | La DLL a été chargée. Le paramètre *NotificationData* pointe vers une structure de **\_ \_ \_ \_ données de notification chargée par une dll LDR** . <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <dt>**LDR \_ Raison de la \_ notification dll \_ \_ déchargée**</dt> <dt>2</dt> </dl> | La DLL a été déchargée. Le paramètre *NotificationData* pointe vers une structure de **\_ \_ \_ \_ données de notification déchargée de dll LDR** . <br/> |



 

</dd> <dt>

*NotificationData* \[ dans\]
</dt> <dd>

Pointeur vers une Union de **\_ \_ notification de dll LDR** constante qui contient des données de notification. Cette Union a la définition suivante :

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

La structure des **\_ \_ \_ \_ données de notification chargée de la dll LDR** a la définition suivante :

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

La structure des **\_ \_ \_ \_ données de notification déchargée de la dll LDR** a la définition suivante :

``` syntax
typedef struct _LDR_DLL_UNLOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_UNLOADED_NOTIFICATION_DATA, *PLDR_DLL_UNLOADED_NOTIFICATION_DATA;
```

</dd> <dt>

*Contexte* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers les données de contexte pour la fonction de rappel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction de rappel ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La fonction de rappel de notification est appelée avant que la liaison dynamique ait lieu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




