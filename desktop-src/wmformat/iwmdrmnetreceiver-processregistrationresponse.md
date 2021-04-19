---
title: Méthode IWMDRMNetReceiver ProcessRegistrationResponse (wmdrmsdk. h)
description: La méthode ProcessRegistrationResponse traite une réponse d’inscription envoyée par l’émetteur en réponse à une demande d’inscription.
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- Méthode ProcessRegistrationResponse format Windows Media
- Méthode ProcessRegistrationResponse format Windows Media, interface IWMDRMNetReceiver
- Interface IWMDRMNetReceiver Windows Media format, méthode ProcessRegistrationResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessRegistrationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77b01f443d57825d82b7cf9556d7585745bb99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530425"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a><span data-ttu-id="73c7c-106">IWMDRMNetReceiver ::P méthode rocessRegistrationResponse</span><span class="sxs-lookup"><span data-stu-id="73c7c-106">IWMDRMNetReceiver::ProcessRegistrationResponse method</span></span>

<span data-ttu-id="73c7c-107">La méthode **ProcessRegistrationResponse** traite une réponse d’inscription envoyée par l’émetteur en réponse à une demande d’inscription.</span><span class="sxs-lookup"><span data-stu-id="73c7c-107">The **ProcessRegistrationResponse** method processes a registration response sent by the transmitter in reply to a registration challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c7c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73c7c-108">Syntax</span></span>


```C++
HRESULT ProcessRegistrationResponse(
  [in]  BYTE     *pbRegistrationResponse,
  [in]  DWORD    cbRegistrationResponse,
  [out] IUnknown **ppunkCancellationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="73c7c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73c7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73c7c-110">*pbRegistrationResponse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73c7c-110">*pbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c7c-111">Réponse d’inscription reçue de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="73c7c-111">Registration response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="73c7c-112">*cbRegistrationResponse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73c7c-112">*cbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c7c-113">Taille de la réponse d’inscription en octets.</span><span class="sxs-lookup"><span data-stu-id="73c7c-113">Size of the registration response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="73c7c-114">*ppunkCancellationCookie* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="73c7c-114">*ppunkCancellationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73c7c-115">Pointeur qui reçoit un pointeur vers l’interface **IUnknown** d’un objet qui identifie cet appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="73c7c-115">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="73c7c-116">Ce pointeur d’interface peut être utilisé pour annuler l’appel asynchrone en appelant la méthode [**IWMDRMEventGenerator :: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="73c7c-116">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73c7c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73c7c-117">Return value</span></span>

<span data-ttu-id="73c7c-118">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="73c7c-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="73c7c-119">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="73c7c-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="73c7c-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="73c7c-120">Return code</span></span>                                                                          | <span data-ttu-id="73c7c-121">Description</span><span class="sxs-lookup"><span data-stu-id="73c7c-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="73c7c-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="73c7c-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="73c7c-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="73c7c-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="73c7c-124">Notes</span><span class="sxs-lookup"><span data-stu-id="73c7c-124">Remarks</span></span>

<span data-ttu-id="73c7c-125">Cette méthode s’exécute de façon asynchrone ; une fois le traitement terminé, l’événement MEProximityCompleted est envoyé à l’interface **IMFMediaEventGenerator** .</span><span class="sxs-lookup"><span data-stu-id="73c7c-125">This method executes asynchronously; when processing is complete, the MEProximityCompleted event is sent to the **IMFMediaEventGenerator** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="73c7c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73c7c-126">Requirements</span></span>



| <span data-ttu-id="73c7c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73c7c-127">Requirement</span></span> | <span data-ttu-id="73c7c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="73c7c-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73c7c-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="73c7c-129">Header</span></span><br/> | <dl> <span data-ttu-id="73c7c-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="73c7c-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73c7c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73c7c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c7c-132">**Interface IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="73c7c-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="73c7c-133">**IWMDRMNetReceiver::GetRegistrationChallenge**</span><span class="sxs-lookup"><span data-stu-id="73c7c-133">**IWMDRMNetReceiver::GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 





