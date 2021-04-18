---
description: Le \_ message DEVSPECIFICFEATURE de ligne TAPI est envoyé pour notifier l’application des événements spécifiques à l’appareil qui se produisent sur une ligne, une adresse ou un appel. La signification du message et l’interprétation des paramètres sont spécifiques à l’appareil.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: Message LINE_DEVSPECIFICFEATURE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d45f91f4b3d45b52a345827e6535b054e9cf2c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526485"
---
# <a name="line_devspecificfeature-message"></a><span data-ttu-id="6af2c-104">\_Message DEVSPECIFICFEATURE de ligne</span><span class="sxs-lookup"><span data-stu-id="6af2c-104">LINE\_DEVSPECIFICFEATURE message</span></span>

<span data-ttu-id="6af2c-105">Le message **\_ DEVSPECIFICFEATURE de ligne** TAPI est envoyé pour notifier l’application des événements spécifiques à l’appareil qui se produisent sur une ligne, une adresse ou un appel.</span><span class="sxs-lookup"><span data-stu-id="6af2c-105">The TAPI **LINE\_DEVSPECIFICFEATURE** message is sent to notify the application about device-specific events occurring on a line, address, or call.</span></span> <span data-ttu-id="6af2c-106">La signification du message et l’interprétation des paramètres sont spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6af2c-106">The meaning of the message and the interpretation of the parameters are device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="6af2c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6af2c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af2c-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="6af2c-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="6af2c-109">Handle vers un périphérique de ligne ou un appel.</span><span class="sxs-lookup"><span data-stu-id="6af2c-109">A handle to either a line device or call.</span></span> <span data-ttu-id="6af2c-110">Il s’agit d’un périphérique spécifique.</span><span class="sxs-lookup"><span data-stu-id="6af2c-110">This is device specific.</span></span>

</dd> <dt>

<span data-ttu-id="6af2c-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="6af2c-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="6af2c-112">Instance de rappel fournie lors de l’ouverture de la ligne.</span><span class="sxs-lookup"><span data-stu-id="6af2c-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="6af2c-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6af2c-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="6af2c-114">Spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6af2c-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="6af2c-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6af2c-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="6af2c-116">Spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6af2c-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="6af2c-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="6af2c-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="6af2c-118">Spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6af2c-118">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af2c-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6af2c-119">Return value</span></span>

<span data-ttu-id="6af2c-120">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="6af2c-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6af2c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="6af2c-121">Remarks</span></span>

<span data-ttu-id="6af2c-122">Le message de **ligne \_ DEVSPECIFICFEATURE** est utilisé par un fournisseur de services conjointement avec la fonction [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) .</span><span class="sxs-lookup"><span data-stu-id="6af2c-122">The **LINE\_DEVSPECIFICFEATURE** message is used by a service provider in conjunction with the [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) function.</span></span> <span data-ttu-id="6af2c-123">Sa signification est spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6af2c-123">Its meaning is device specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="6af2c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6af2c-124">Requirements</span></span>



| <span data-ttu-id="6af2c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6af2c-125">Requirement</span></span> | <span data-ttu-id="6af2c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="6af2c-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6af2c-127">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="6af2c-127">TAPI version</span></span><br/> | <span data-ttu-id="6af2c-128">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6af2c-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6af2c-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="6af2c-129">Header</span></span><br/>       | <dl> <span data-ttu-id="6af2c-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6af2c-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




