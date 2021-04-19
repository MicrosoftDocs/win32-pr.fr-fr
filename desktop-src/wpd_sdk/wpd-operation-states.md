---
description: L' \_ opération wpd \_ indique les valeurs d’énumération qui décrivent l’état actuel d’une opération en cours.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: Énumération WPD_OPERATION_STATES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1746ab6a798c74974708ac10b9c4d137bf6c1d42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535303"
---
# <a name="wpd_operation_states-enumeration"></a><span data-ttu-id="d6fb7-103">\_Énumération des États de l’opération wpd \_</span><span class="sxs-lookup"><span data-stu-id="d6fb7-103">WPD\_OPERATION\_STATES enumeration</span></span>

<span data-ttu-id="d6fb7-104">L' **\_ opération wpd \_ indique** les valeurs d’énumération qui décrivent l’état actuel d’une opération en cours.</span><span class="sxs-lookup"><span data-stu-id="d6fb7-104">The **WPD\_OPERATION\_STATES** enumeration values describe the current state of an operation in progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6fb7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6fb7-105">Syntax</span></span>


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a><span data-ttu-id="d6fb7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d6fb7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d6fb7-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**État de l' \_ opération wpd \_ \_ non spécifié**</span><span class="sxs-lookup"><span data-stu-id="d6fb7-107"><span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**WPD\_OPERATION\_STATE\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="d6fb7-108">L’opération actuelle est dans un État non spécifié (non défini) et inconnu.</span><span class="sxs-lookup"><span data-stu-id="d6fb7-108">The current operation is in an unspecified state (not set) and unknown.</span></span>

</dd> <dt>

<span data-ttu-id="d6fb7-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**État de l' \_ opération wpd \_ \_ démarré**</span><span class="sxs-lookup"><span data-stu-id="d6fb7-109"><span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**WPD\_OPERATION\_STATE\_STARTED**</span></span>
</dt> <dd>

<span data-ttu-id="d6fb7-110">L’opération est démarrée.</span><span class="sxs-lookup"><span data-stu-id="d6fb7-110">The operation is started.</span></span>

</dd> <dt>

<span data-ttu-id="d6fb7-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**État de l' \_ opération wpd \_ \_ en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="d6fb7-111"><span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**WPD\_OPERATION\_STATE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="d6fb7-112">L’opération est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d6fb7-112">The operation is running.</span></span>

</dd> <dt>

<span data-ttu-id="d6fb7-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**État de l' \_ opération wpd \_ \_ suspendu**</span><span class="sxs-lookup"><span data-stu-id="d6fb7-113"><span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**WPD\_OPERATION\_STATE\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="d6fb7-114">L’opération est suspendue.</span><span class="sxs-lookup"><span data-stu-id="d6fb7-114">The operation is paused.</span></span>

</dd> <dt>

<span data-ttu-id="d6fb7-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**État de l' \_ opération wpd \_ \_ annulé**</span><span class="sxs-lookup"><span data-stu-id="d6fb7-115"><span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**WPD\_OPERATION\_STATE\_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="d6fb7-116">L’opération est annulée.</span><span class="sxs-lookup"><span data-stu-id="d6fb7-116">The operation is canceled.</span></span>

</dd> <dt>

<span data-ttu-id="d6fb7-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**État de l' \_ opération wpd \_ \_ terminé**</span><span class="sxs-lookup"><span data-stu-id="d6fb7-117"><span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**WPD\_OPERATION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="d6fb7-118">L’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="d6fb7-118">The operation is finished.</span></span>

</dd> <dt>

<span data-ttu-id="d6fb7-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**État de l' \_ opération wpd \_ \_ abandonné**</span><span class="sxs-lookup"><span data-stu-id="d6fb7-119"><span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**WPD\_OPERATION\_STATE\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="d6fb7-120">L’opération est abandonnée.</span><span class="sxs-lookup"><span data-stu-id="d6fb7-120">The operation is aborted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6fb7-121">Notes</span><span class="sxs-lookup"><span data-stu-id="d6fb7-121">Remarks</span></span>

<span data-ttu-id="d6fb7-122">Ces valeurs sont reçues dans le rappel défini par l’application ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).</span><span class="sxs-lookup"><span data-stu-id="d6fb7-122">These values are received in the application-defined callback ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6fb7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6fb7-123">Requirements</span></span>



| <span data-ttu-id="d6fb7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6fb7-124">Requirement</span></span> | <span data-ttu-id="d6fb7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6fb7-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6fb7-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6fb7-126">Header</span></span><br/> | <dl> <span data-ttu-id="d6fb7-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6fb7-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6fb7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6fb7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6fb7-129">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="d6fb7-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




