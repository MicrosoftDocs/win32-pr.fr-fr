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
ms.openlocfilehash: e1e9bea21cd4e21ca7549ce34343b42c50b293471e69576d7c1164f92a371c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004104"
---
# <a name="ldrdllnotification-callback-function"></a>LdrDllNotification fonction de rappel

\[cette fonction peut être modifiée ou supprimée de Windows sans préavis.\]

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

## <a name="remarks"></a>Remarques

La fonction de rappel de notification est appelée avant que la liaison dynamique ait lieu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




