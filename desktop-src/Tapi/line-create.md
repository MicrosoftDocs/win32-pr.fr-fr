---
description: Le \_ message de création de la ligne TAPI est envoyé pour informer l’application de la création d’un nouveau périphérique de ligne.
ms.assetid: d4735eab-392f-49d9-a1d9-5895d9232624
title: Message LINE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9973849c3942b5427dfb6b3fe7c47bc4d2a716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520923"
---
# <a name="line_create-message"></a><span data-ttu-id="92a70-103">Créer un message de ligne \_</span><span class="sxs-lookup"><span data-stu-id="92a70-103">LINE\_CREATE message</span></span>

<span data-ttu-id="92a70-104">Le message **de \_ création** de la ligne TAPI est envoyé pour informer l’application de la création d’un nouveau périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="92a70-104">The TAPI **LINE\_CREATE** message is sent to inform the application of the creation of a new line device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="92a70-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92a70-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a70-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="92a70-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="92a70-107">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="92a70-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="92a70-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="92a70-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="92a70-109">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="92a70-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="92a70-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="92a70-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="92a70-111">*HDeviceID* de l’appareil nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="92a70-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="92a70-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="92a70-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="92a70-113">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="92a70-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="92a70-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="92a70-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="92a70-115">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="92a70-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92a70-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92a70-116">Return value</span></span>

<span data-ttu-id="92a70-117">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="92a70-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92a70-118">Notes</span><span class="sxs-lookup"><span data-stu-id="92a70-118">Remarks</span></span>

<span data-ttu-id="92a70-119">Les applications plus anciennes (qui ont négocié la version 1,3 de TAPI) reçoivent un message de [**ligne \_ LINEDEVSTATE**](line-linedevstate.md) qui spécifie LINEDEVSTATE \_ rein, ce qui leur demande d’arrêter leur utilisation de l’API et d’appeler à nouveau [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) pour obtenir le nouveau nombre d’appareils.</span><span class="sxs-lookup"><span data-stu-id="92a70-119">Older applications (that negotiated TAPI version 1.3) are sent a [**LINE\_LINEDEVSTATE**](line-linedevstate.md) message specifying LINEDEVSTATE\_REINIT, which requires them to shut down their use of the API and call [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="92a70-120">Toutefois, contrairement aux versions précédentes de TAPI, cette version ne requiert pas l’arrêt de toutes les applications avant d’autoriser la réinitialisation des applications. la réinitialisation peut avoir lieu immédiatement lors de la création d’un nouveau périphérique (l’arrêt complet est toujours nécessaire lorsqu’un fournisseur de services est supprimé du système).</span><span class="sxs-lookup"><span data-stu-id="92a70-120">Unlike previous versions of TAPI, however, this version does not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created (complete shutdown is still required when a service provider is removed from the system).</span></span>

<span data-ttu-id="92a70-121">Les applications prenant en charge TAPI version 1,4 ou ultérieure reçoivent un message de **\_ création de ligne** .</span><span class="sxs-lookup"><span data-stu-id="92a70-121">Applications supporting TAPI version 1.4 or later are sent a **LINE\_CREATE** message.</span></span> <span data-ttu-id="92a70-122">Cela les informe de l’existence du nouvel appareil et de son nouvel identificateur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="92a70-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="92a70-123">L’application peut ensuite choisir s’il faut ou non essayer de travailler avec le nouvel appareil à loisir.</span><span class="sxs-lookup"><span data-stu-id="92a70-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span> <span data-ttu-id="92a70-124">Ce message est envoyé à toutes les applications prenant en charge cette version ou les versions ultérieures de l’API qui ont appelé [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) ou [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), y compris celles qui n’ont pas d’appareils de ligne ouverts à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="92a70-124">This message is sent to all applications supporting this or subsequent versions of the API that have called [**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize) or [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), including those that do not have any line devices open at the time.</span></span>

## <a name="requirements"></a><span data-ttu-id="92a70-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92a70-125">Requirements</span></span>



| <span data-ttu-id="92a70-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92a70-126">Requirement</span></span> | <span data-ttu-id="92a70-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="92a70-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="92a70-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="92a70-128">TAPI version</span></span><br/> | <span data-ttu-id="92a70-129">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="92a70-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="92a70-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="92a70-130">Header</span></span><br/>       | <dl> <span data-ttu-id="92a70-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="92a70-131"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92a70-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92a70-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a70-133">**LINEDEVSTATE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="92a70-133">**LINE\_LINEDEVSTATE**</span></span>](line-linedevstate.md)
</dt> <dt>

[<span data-ttu-id="92a70-134">**lineInitialize**</span><span class="sxs-lookup"><span data-stu-id="92a70-134">**lineInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[<span data-ttu-id="92a70-135">**lineInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="92a70-135">**lineInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




