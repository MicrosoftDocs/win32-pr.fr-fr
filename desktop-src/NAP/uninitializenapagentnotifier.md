---
title: UninitializeNapAgentNotifier, fonction (NapUtil. h)
description: Désabonne le processus appelant des notifications de changement d’État NapAgent et des notifications de changement d’état de quarantaine.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- UninitializeNapAgentNotifier fonction NAP
topic_type:
- apiref
api_name:
- UninitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d68b43fba64be82908d73803113f871b08c93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384383"
---
# <a name="uninitializenapagentnotifier-function"></a><span data-ttu-id="9eedf-104">UninitializeNapAgentNotifier fonction)</span><span class="sxs-lookup"><span data-stu-id="9eedf-104">UninitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="9eedf-105">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="9eedf-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9eedf-106">La fonction **UninitializeNapAgentNotifier** désabonne le processus appelant des notifications de changement d’État NapAgent et des notifications de changement d’état de quarantaine.</span><span class="sxs-lookup"><span data-stu-id="9eedf-106">The **UninitializeNapAgentNotifier** function unsubscribes the calling process from NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="9eedf-107">Ces notifications sont fournies par le service NapAgent.</span><span class="sxs-lookup"><span data-stu-id="9eedf-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eedf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9eedf-108">Syntax</span></span>


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a><span data-ttu-id="9eedf-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9eedf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eedf-110">*type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9eedf-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eedf-111">Valeur [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) qui spécifie le type de notifications de service dont l’abonnement doit être annulé.</span><span class="sxs-lookup"><span data-stu-id="9eedf-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to unsubscribe from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eedf-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9eedf-112">Return value</span></span>

<span data-ttu-id="9eedf-113">Cette fonction n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9eedf-113">This function has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eedf-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9eedf-114">Remarks</span></span>

<span data-ttu-id="9eedf-115">Cette fonction n’est pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="9eedf-115">This function is not thread safe.</span></span>

<span data-ttu-id="9eedf-116">Chaque processus abonné aux notifications de service NapAgent du *type* spécifié doit appeler **UninitializeNapAgentNotifier** pour se désabonner des notifications.</span><span class="sxs-lookup"><span data-stu-id="9eedf-116">Each process subscribed to NapAgent service notifications of the specified *type* must call **UninitializeNapAgentNotifier** to unsubscribe from notifications.</span></span> <span data-ttu-id="9eedf-117">Si un processus est abonné à plusieurs types de notifications, il doit appeler **UninitializeNapAgentNotifier** une fois pour chaque type de notification.</span><span class="sxs-lookup"><span data-stu-id="9eedf-117">If a process is subscribed to more than one type of notification, it must call **UninitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="9eedf-118">Cette fonction échoue en silence si le processus n’a pas précédemment appelé [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) pour le type de notification.</span><span class="sxs-lookup"><span data-stu-id="9eedf-118">This function will fail silently if the process had not previously called [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) for the notification type.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eedf-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9eedf-119">Requirements</span></span>



| <span data-ttu-id="9eedf-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9eedf-120">Requirement</span></span> | <span data-ttu-id="9eedf-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9eedf-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9eedf-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eedf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9eedf-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9eedf-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9eedf-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9eedf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9eedf-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9eedf-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9eedf-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9eedf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eedf-127"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eedf-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="9eedf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9eedf-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eedf-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eedf-129"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eedf-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9eedf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eedf-131">**InitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="9eedf-131">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
</dt> </dl>

 

 





