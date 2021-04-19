---
description: Le \_ message CALLHUBCLOSE de ligne TAPI est envoyé lorsqu’un hub d’appel a été fermé.
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: Message LINE_CALLHUBCLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b538d6f154f3dacb2d779b6233722df16cc635d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528734"
---
# <a name="line_callhubclose-message"></a><span data-ttu-id="7b662-103">\_Message CALLHUBCLOSE de ligne</span><span class="sxs-lookup"><span data-stu-id="7b662-103">LINE\_CALLHUBCLOSE message</span></span>

<span data-ttu-id="7b662-104">Le message **\_ CALLHUBCLOSE de ligne** TAPI est envoyé lorsqu’un hub d’appel a été fermé.</span><span class="sxs-lookup"><span data-stu-id="7b662-104">The TAPI **LINE\_CALLHUBCLOSE** message is sent when a call hub has been closed.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="7b662-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b662-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b662-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="7b662-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="7b662-107">Handle de l’appel.</span><span class="sxs-lookup"><span data-stu-id="7b662-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="7b662-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="7b662-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="7b662-109">Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.</span><span class="sxs-lookup"><span data-stu-id="7b662-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="7b662-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="7b662-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="7b662-111">Réservé.</span><span class="sxs-lookup"><span data-stu-id="7b662-111">Reserved.</span></span> <span data-ttu-id="7b662-112">Définit la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="7b662-112">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="7b662-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="7b662-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="7b662-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="7b662-114">Reserved.</span></span> <span data-ttu-id="7b662-115">Définit la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="7b662-115">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="7b662-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="7b662-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="7b662-117">Réservé.</span><span class="sxs-lookup"><span data-stu-id="7b662-117">Reserved.</span></span> <span data-ttu-id="7b662-118">Définit la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="7b662-118">Set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b662-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b662-119">Return value</span></span>

<span data-ttu-id="7b662-120">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="7b662-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b662-121">Notes</span><span class="sxs-lookup"><span data-stu-id="7b662-121">Remarks</span></span>

<span data-ttu-id="7b662-122">Ce message provient de l’interface TAPI plutôt que d’un fournisseur de services, ce qui signifie qu’il n’y a aucun message TSPI correspondant.</span><span class="sxs-lookup"><span data-stu-id="7b662-122">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b662-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b662-123">Requirements</span></span>



| <span data-ttu-id="7b662-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b662-124">Requirement</span></span> | <span data-ttu-id="7b662-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b662-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7b662-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="7b662-126">TAPI version</span></span><br/> | <span data-ttu-id="7b662-127">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="7b662-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="7b662-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b662-128">Header</span></span><br/>       | <dl> <span data-ttu-id="7b662-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b662-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




