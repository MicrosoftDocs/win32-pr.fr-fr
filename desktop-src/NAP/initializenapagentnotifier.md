---
title: InitializeNapAgentNotifier, fonction (NapUtil. h)
description: Abonne le processus appelant aux notifications de modification d’État NapAgent et aux notifications de modification d’état de quarantaine.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- InitializeNapAgentNotifier fonction NAP
topic_type:
- apiref
api_name:
- InitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f59c4c342f693038040f374bbdbcdb8ab226f74d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941911"
---
# <a name="initializenapagentnotifier-function"></a><span data-ttu-id="dd033-104">InitializeNapAgentNotifier fonction)</span><span class="sxs-lookup"><span data-stu-id="dd033-104">InitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="dd033-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="dd033-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="dd033-106">La fonction **InitializeNapAgentNotifier** abonne le processus appelant aux notifications de modification d’État NapAgent et aux notifications de modification d’état de quarantaine.</span><span class="sxs-lookup"><span data-stu-id="dd033-106">The **InitializeNapAgentNotifier** function subscribes the calling process to NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="dd033-107">Ces notifications sont fournies par le service NapAgent.</span><span class="sxs-lookup"><span data-stu-id="dd033-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd033-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd033-108">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a><span data-ttu-id="dd033-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd033-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd033-110">*type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd033-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd033-111">Valeur [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) qui spécifie le type de notifications de service à recevoir.</span><span class="sxs-lookup"><span data-stu-id="dd033-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to receive.</span></span>

</dd> <dt>

<span data-ttu-id="dd033-112">*hNotifyEvent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd033-112">*hNotifyEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd033-113">Handle d’événement utilisé pour la notification.</span><span class="sxs-lookup"><span data-stu-id="dd033-113">An event handle used for notification.</span></span> <span data-ttu-id="dd033-114">L’appelant doit passer un handle ouvert au paramètre *hNotifyEvent* .</span><span class="sxs-lookup"><span data-stu-id="dd033-114">The caller must pass an open handle to the *hNotifyEvent* parameter.</span></span> <span data-ttu-id="dd033-115">L’appelant doit également fermer le descripteur d’événement lorsqu’il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dd033-115">The caller must also close the event handle when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd033-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd033-116">Return value</span></span>



| <span data-ttu-id="dd033-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dd033-117">Return code</span></span>                                                                                                | <span data-ttu-id="dd033-118">Description</span><span class="sxs-lookup"><span data-stu-id="dd033-118">Description</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dd033-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dd033-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="dd033-120">L’initialisation s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="dd033-120">Initialization completed successfully.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="dd033-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="dd033-121"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="dd033-122">Échec de l'initialisation.</span><span class="sxs-lookup"><span data-stu-id="dd033-122">Initialization failed.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="dd033-123"><dt>**ERREUR \_ déjà \_ initialisée**</dt></span><span class="sxs-lookup"><span data-stu-id="dd033-123"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="dd033-124">Le processus s’est déjà abonné aux notifications du service NapAgent du *type* spécifié.</span><span class="sxs-lookup"><span data-stu-id="dd033-124">The process has already subscribed to NapAgent service notifications of the *type* specified.</span></span> <br/> |
| <dl> <span data-ttu-id="dd033-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dd033-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="dd033-126">Un argument non valide a été passé.</span><span class="sxs-lookup"><span data-stu-id="dd033-126">An invalid argument was passed.</span></span> <br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="dd033-127">Notes</span><span class="sxs-lookup"><span data-stu-id="dd033-127">Remarks</span></span>

<span data-ttu-id="dd033-128">Cette fonction n’est pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="dd033-128">This function is not thread safe.</span></span>

<span data-ttu-id="dd033-129">Chaque processus qui requiert un abonnement aux notifications de service NapAgent du *type* spécifié doit appeler **InitializeNapAgentNotifier** pour s’abonner aux notifications.</span><span class="sxs-lookup"><span data-stu-id="dd033-129">Each process that requires a subscription to NapAgent service notifications of the specified *type* must call **InitializeNapAgentNotifier** to subscribe to notifications.</span></span> <span data-ttu-id="dd033-130">Si un processus doit s’abonner à plusieurs types de notifications, il doit appeler **InitializeNapAgentNotifier** une fois pour chaque type de notification.</span><span class="sxs-lookup"><span data-stu-id="dd033-130">If a process must subscribe to more than one type of notification, it must call **InitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="dd033-131">Une fois qu’un processus ne nécessite pas d’autres notifications, le processus doit appeler [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) pour le *type* spécifié.</span><span class="sxs-lookup"><span data-stu-id="dd033-131">Once a process does not require further notifications, the process must call [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) for the specified *type*.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd033-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd033-132">Requirements</span></span>



| <span data-ttu-id="dd033-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd033-133">Requirement</span></span> | <span data-ttu-id="dd033-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd033-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dd033-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd033-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dd033-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd033-136">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dd033-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dd033-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dd033-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dd033-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dd033-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd033-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd033-140"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd033-140"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="dd033-141">DLL</span><span class="sxs-lookup"><span data-stu-id="dd033-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd033-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd033-142"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd033-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd033-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd033-144">**UninitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="dd033-144">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





