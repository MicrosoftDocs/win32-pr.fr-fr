---
description: L’interface TAPI envoie le \_ message DEVSPECIFIC de téléphone à une application pour notifier l’application des événements spécifiques à l’appareil qui se produisent au téléphone. La signification du message et l’interprétation des paramètres sont définies par l’implémentation.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: Message PHONE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c817f273a49fdcda36995cec335811fb06c8a917
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527975"
---
# <a name="phone_devspecific-message"></a><span data-ttu-id="f7461-104">\_Message DEVSPECIFIC téléphone</span><span class="sxs-lookup"><span data-stu-id="f7461-104">PHONE\_DEVSPECIFIC message</span></span>

<span data-ttu-id="f7461-105">L’interface TAPI envoie le message **\_ DEVSPECIFIC de téléphone** à une application pour notifier l’application des événements spécifiques à l’appareil qui se produisent au téléphone.</span><span class="sxs-lookup"><span data-stu-id="f7461-105">TAPI sends the **PHONE\_DEVSPECIFIC** message to an application to notify the application about device-specific events occurring at the phone.</span></span> <span data-ttu-id="f7461-106">La signification du message et l’interprétation des paramètres sont définies par l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="f7461-106">The meaning of the message and the interpretation of the parameters is implementation-defined.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="f7461-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7461-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7461-108">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="f7461-108">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="f7461-109">Handle vers l’appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="f7461-109">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="f7461-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="f7461-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f7461-111">Instance de rappel de l’application fournie lors de l’ouverture du périphérique téléphonique.</span><span class="sxs-lookup"><span data-stu-id="f7461-111">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="f7461-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f7461-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f7461-113">Spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f7461-113">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="f7461-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f7461-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f7461-115">Spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f7461-115">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="f7461-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f7461-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f7461-117">Spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f7461-117">Device specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7461-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7461-118">Return value</span></span>

<span data-ttu-id="f7461-119">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f7461-119">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7461-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7461-120">Requirements</span></span>



| <span data-ttu-id="f7461-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7461-121">Requirement</span></span> | <span data-ttu-id="f7461-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7461-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f7461-123">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="f7461-123">TAPI version</span></span><br/> | <span data-ttu-id="f7461-124">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f7461-124">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f7461-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7461-125">Header</span></span><br/>       | <dl> <span data-ttu-id="f7461-126"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7461-126"><dt>Tapi.h</dt></span></span> </dl> |



 

 




