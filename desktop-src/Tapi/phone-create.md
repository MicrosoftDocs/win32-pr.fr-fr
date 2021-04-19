---
description: Le \_ message de création de téléphone TAPI est envoyé pour informer les applications de la création d’un nouveau périphérique téléphonique.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: Message PHONE_CREATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92dfaad5d4007279f18890021f5cb39c22c4da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542467"
---
# <a name="phone_create-message"></a><span data-ttu-id="ea802-103">Message de création de téléphone \_</span><span class="sxs-lookup"><span data-stu-id="ea802-103">PHONE\_CREATE message</span></span>

<span data-ttu-id="ea802-104">Le message **de \_ création de téléphone** TAPI est envoyé pour informer les applications de la création d’un nouveau périphérique téléphonique.</span><span class="sxs-lookup"><span data-stu-id="ea802-104">The TAPI **PHONE\_CREATE** message is sent to inform applications of the creation of a new phone device.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="ea802-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea802-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea802-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="ea802-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="ea802-107">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="ea802-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="ea802-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="ea802-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="ea802-109">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="ea802-109">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="ea802-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="ea802-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="ea802-111">*HDeviceID* de l’appareil nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="ea802-111">The *hDeviceID* of the newly created device.</span></span>

</dd> <dt>

<span data-ttu-id="ea802-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="ea802-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="ea802-113">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="ea802-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="ea802-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="ea802-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="ea802-115">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="ea802-115">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea802-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea802-116">Return value</span></span>

<span data-ttu-id="ea802-117">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="ea802-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea802-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ea802-118">Remarks</span></span>

<span data-ttu-id="ea802-119">Les applications qui ont négocié la version 1,3 reçoivent un message d' [**\_ État de téléphone**](phone-state.md) spécifiant PHONESTATE \_ rein, ce qui leur demande d’arrêter leur utilisation de l’API et d’appeler à nouveau [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) pour obtenir le nouveau nombre d’appareils.</span><span class="sxs-lookup"><span data-stu-id="ea802-119">Applications that negotiated API version 1.3 are sent a [**PHONE\_STATE**](phone-state.md) message specifying PHONESTATE\_REINIT, which requires them to shut down their use of the API and call [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) again to obtain the new number of devices.</span></span> <span data-ttu-id="ea802-120">Toutefois, TAPI version 1,4 et versions ultérieures ne nécessitent pas l’arrêt de toutes les applications avant d’autoriser la réinitialisation des applications. la réinitialisation peut avoir lieu immédiatement lors de la création d’un nouveau périphérique.</span><span class="sxs-lookup"><span data-stu-id="ea802-120">However, TAPI version 1.4 and above do not require all applications to shut down before allowing applications to reinitialize; reinitialization can take place immediately when a new device is created.</span></span>

<span data-ttu-id="ea802-121">Les applications prenant en charge TAPI version 1,4 ou ultérieure reçoivent un message de **\_ création de téléphone** .</span><span class="sxs-lookup"><span data-stu-id="ea802-121">Applications supporting TAPI version 1.4 or later are sent a **PHONE\_CREATE** message.</span></span> <span data-ttu-id="ea802-122">Cela les informe de l’existence du nouvel appareil et de son nouvel identificateur d’appareil.</span><span class="sxs-lookup"><span data-stu-id="ea802-122">This informs them of the existence of the new device and its new device identifier.</span></span> <span data-ttu-id="ea802-123">L’application peut ensuite choisir s’il faut ou non essayer de travailler avec le nouvel appareil à loisir.</span><span class="sxs-lookup"><span data-stu-id="ea802-123">The application can then choose whether or not to attempt working with the new device at its leisure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea802-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea802-124">Requirements</span></span>



| <span data-ttu-id="ea802-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea802-125">Requirement</span></span> | <span data-ttu-id="ea802-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea802-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ea802-127">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="ea802-127">TAPI version</span></span><br/> | <span data-ttu-id="ea802-128">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ea802-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ea802-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea802-129">Header</span></span><br/>       | <dl> <span data-ttu-id="ea802-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea802-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea802-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea802-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea802-132">**État du téléphone \_**</span><span class="sxs-lookup"><span data-stu-id="ea802-132">**PHONE\_STATE**</span></span>](phone-state.md)
</dt> <dt>

[<span data-ttu-id="ea802-133">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="ea802-133">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="ea802-134">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="ea802-134">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




