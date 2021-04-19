---
description: Le \_ message DEVSPECIFICEX de ligne TAPI est envoyé pour notifier l’application des événements spécifiques à l’appareil qui se produisent sur une ligne, une adresse ou un appel. La signification du message et l’interprétation des paramètres sont spécifiques à l’appareil.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: Message LINE_DEVSPECIFICEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba25047858c641ea4c6cec7d15ba06df24e8ee39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531013"
---
# <a name="line_devspecificex-message"></a><span data-ttu-id="02e20-104">\_Message DEVSPECIFICEX de ligne</span><span class="sxs-lookup"><span data-stu-id="02e20-104">LINE\_DEVSPECIFICEX message</span></span>

<span data-ttu-id="02e20-105">Le message **\_ DEVSPECIFICEX de ligne** TAPI est envoyé pour notifier l’application des événements spécifiques à l’appareil qui se produisent sur une ligne, une adresse ou un appel.</span><span class="sxs-lookup"><span data-stu-id="02e20-105">The TAPI **LINE\_DEVSPECIFICEX** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="02e20-106">La signification du message et l’interprétation des paramètres sont spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="02e20-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="02e20-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02e20-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e20-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="02e20-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="02e20-109">Handle vers un périphérique de ligne ou un appel.</span><span class="sxs-lookup"><span data-stu-id="02e20-109">A handle to either a line device or call.</span></span> <span data-ttu-id="02e20-110">Ce paramètre est spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="02e20-110">This parameter is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="02e20-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="02e20-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="02e20-112">Instance de rappel fournie lors de l’ouverture de la ligne.</span><span class="sxs-lookup"><span data-stu-id="02e20-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="02e20-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="02e20-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="02e20-114">Spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="02e20-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="02e20-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="02e20-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="02e20-116">Spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="02e20-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="02e20-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="02e20-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="02e20-118">Spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="02e20-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02e20-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02e20-119">Return value</span></span>

<span data-ttu-id="02e20-120">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="02e20-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="02e20-121">Notes</span><span class="sxs-lookup"><span data-stu-id="02e20-121">Remarks</span></span>

<span data-ttu-id="02e20-122">Le message de **ligne \_ DEVSPECIFICEX** est utilisé par un fournisseur de services conjointement avec la fonction [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) .</span><span class="sxs-lookup"><span data-stu-id="02e20-122">The **LINE\_DEVSPECIFICEX** message is used by a service provider in conjunction with the [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) function.</span></span> <span data-ttu-id="02e20-123">Sa signification est spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="02e20-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e20-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02e20-124">Requirements</span></span>



| <span data-ttu-id="02e20-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02e20-125">Requirement</span></span> | <span data-ttu-id="02e20-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="02e20-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="02e20-127">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="02e20-127">TAPI version</span></span><br/> | <span data-ttu-id="02e20-128">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="02e20-128">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="02e20-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="02e20-129">Header</span></span><br/>       | <dl> <span data-ttu-id="02e20-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="02e20-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




