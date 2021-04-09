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
# <a name="ldrdllnotification-callback-function"></a><span data-ttu-id="39b7a-103">LdrDllNotification fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="39b7a-103">LdrDllNotification callback function</span></span>

<span data-ttu-id="39b7a-104">\[Cette fonction peut être modifiée ou supprimée de Windows sans préavis.\]</span><span class="sxs-lookup"><span data-stu-id="39b7a-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="39b7a-105">Fonction de rappel de notification spécifiée avec la fonction [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="39b7a-105">A notification callback function specified with the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span> <span data-ttu-id="39b7a-106">Le chargeur appelle cette fonction lorsqu’une DLL est chargée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="39b7a-106">The loader calls this function when a DLL is first loaded.</span></span>

<span data-ttu-id="39b7a-107">**Avertissement :** Il n’est pas sûr que la fonction de rappel de notification appelle des fonctions dans une DLL.</span><span class="sxs-lookup"><span data-stu-id="39b7a-107">**Warning:** It is unsafe for the notification callback function to call functions in any DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b7a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39b7a-108">Syntax</span></span>


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a><span data-ttu-id="39b7a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39b7a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39b7a-110">*NotificationReason* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39b7a-110">*NotificationReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39b7a-111">Raison pour laquelle la fonction de rappel de notification a été appelée.</span><span class="sxs-lookup"><span data-stu-id="39b7a-111">The reason that the notification callback function was called.</span></span> <span data-ttu-id="39b7a-112">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="39b7a-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="39b7a-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="39b7a-113">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="39b7a-114">Signification</span><span class="sxs-lookup"><span data-stu-id="39b7a-114">Meaning</span></span>                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <span data-ttu-id="39b7a-115"><dt>**LDR \_ Raison de la \_ notification dll \_ \_ chargée**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="39b7a-115"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_LOADED**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="39b7a-116">La DLL a été chargée.</span><span class="sxs-lookup"><span data-stu-id="39b7a-116">The DLL was loaded.</span></span> <span data-ttu-id="39b7a-117">Le paramètre *NotificationData* pointe vers une structure de **\_ \_ \_ \_ données de notification chargée par une dll LDR** .</span><span class="sxs-lookup"><span data-stu-id="39b7a-117">The *NotificationData* parameter points to an **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <span data-ttu-id="39b7a-118"><dt>**LDR \_ Raison de la \_ notification dll \_ \_ déchargée**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="39b7a-118"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_UNLOADED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="39b7a-119">La DLL a été déchargée.</span><span class="sxs-lookup"><span data-stu-id="39b7a-119">The DLL was unloaded.</span></span> <span data-ttu-id="39b7a-120">Le paramètre *NotificationData* pointe vers une structure de **\_ \_ \_ \_ données de notification déchargée de dll LDR** .</span><span class="sxs-lookup"><span data-stu-id="39b7a-120">The *NotificationData* parameter points to an **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="39b7a-121">*NotificationData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39b7a-121">*NotificationData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39b7a-122">Pointeur vers une Union de **\_ \_ notification de dll LDR** constante qui contient des données de notification.</span><span class="sxs-lookup"><span data-stu-id="39b7a-122">A pointer to a constant **LDR\_DLL\_NOTIFICATION** union that contains notification data.</span></span> <span data-ttu-id="39b7a-123">Cette Union a la définition suivante :</span><span class="sxs-lookup"><span data-stu-id="39b7a-123">This union has the following definition:</span></span>

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

<span data-ttu-id="39b7a-124">La structure des **\_ \_ \_ \_ données de notification chargée de la dll LDR** a la définition suivante :</span><span class="sxs-lookup"><span data-stu-id="39b7a-124">The **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

<span data-ttu-id="39b7a-125">La structure des **\_ \_ \_ \_ données de notification déchargée de la dll LDR** a la définition suivante :</span><span class="sxs-lookup"><span data-stu-id="39b7a-125">The **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

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

<span data-ttu-id="39b7a-126">*Contexte* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="39b7a-126">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="39b7a-127">Pointeur vers les données de contexte pour la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="39b7a-127">A pointer to context data for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39b7a-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39b7a-128">Return value</span></span>

<span data-ttu-id="39b7a-129">Cette fonction de rappel ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="39b7a-129">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39b7a-130">Notes</span><span class="sxs-lookup"><span data-stu-id="39b7a-130">Remarks</span></span>

<span data-ttu-id="39b7a-131">La fonction de rappel de notification est appelée avant que la liaison dynamique ait lieu.</span><span class="sxs-lookup"><span data-stu-id="39b7a-131">The notification callback function is called before dynamic linking takes place.</span></span>

## <a name="requirements"></a><span data-ttu-id="39b7a-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39b7a-132">Requirements</span></span>



| <span data-ttu-id="39b7a-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39b7a-133">Requirement</span></span> | <span data-ttu-id="39b7a-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="39b7a-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="39b7a-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39b7a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="39b7a-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39b7a-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="39b7a-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39b7a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="39b7a-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39b7a-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39b7a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39b7a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39b7a-140">**LdrRegisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="39b7a-140">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> <dt>

[<span data-ttu-id="39b7a-141">**LdrUnregisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="39b7a-141">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




