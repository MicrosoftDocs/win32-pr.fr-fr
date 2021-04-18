---
title: Méthode IWMDRMLicenseManagement CleanLicenseStore (wmdrmsdk. h)
description: La méthode CleanLicenseStore supprime les licences inutilisables du magasin de licences temporaire et défragmente le magasin de licences local pour améliorer les performances.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Méthode CleanLicenseStore format Windows Media
- Méthode CleanLicenseStore format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode CleanLicenseStore
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CleanLicenseStore
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9327fd836cf742f5495c29767be93d914c0f187
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532957"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a><span data-ttu-id="94e80-106">IWMDRMLicenseManagement :: CleanLicenseStore, méthode</span><span class="sxs-lookup"><span data-stu-id="94e80-106">IWMDRMLicenseManagement::CleanLicenseStore method</span></span>

<span data-ttu-id="94e80-107">La méthode **CleanLicenseStore** supprime les licences inutilisables du magasin de licences temporaire et défragmente le magasin de licences local pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="94e80-107">The **CleanLicenseStore** method removes unusable licenses from the temporary license store and defragments the local license store to improve performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="94e80-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94e80-108">Syntax</span></span>


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="94e80-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94e80-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94e80-110">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="94e80-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94e80-111">Indicateurs spécifiant les options de nettoyage du magasin de licences à utiliser.</span><span class="sxs-lookup"><span data-stu-id="94e80-111">Flags specifying the license store cleaning options to use.</span></span> <span data-ttu-id="94e80-112">Définissez l’une des constantes dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="94e80-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="94e80-113">Constante</span><span class="sxs-lookup"><span data-stu-id="94e80-113">Constant</span></span>                            | <span data-ttu-id="94e80-114">Description</span><span class="sxs-lookup"><span data-stu-id="94e80-114">Description</span></span>                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94e80-115">\_synchronisation du \_ magasin de licences de nettoyage WMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="94e80-115">WMDRM\_CLEAN\_LICENSE\_STORE\_SYNC</span></span>  | <span data-ttu-id="94e80-116">L’opération de nettoyage sera exécutée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="94e80-116">The clean operation will be performed synchronously.</span></span> <span data-ttu-id="94e80-117">Cette méthode n’est pas retournée tant que l’opération n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="94e80-117">This method will not return until the operation is complete.</span></span>                                                              |
| <span data-ttu-id="94e80-118">\_magasin de licences nettoyées WMDRM \_ \_ \_ asynchrone</span><span class="sxs-lookup"><span data-stu-id="94e80-118">WMDRM\_CLEAN\_LICENSE\_STORE\_ASYNC</span></span> | <span data-ttu-id="94e80-119">L’opération de nettoyage sera exécutée de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="94e80-119">The clean operation will be performed asynchronously.</span></span> <span data-ttu-id="94e80-120">Cette méthode est retournée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="94e80-120">This method will return immediately.</span></span> <span data-ttu-id="94e80-121">Une fois l’opération terminée, l’événement de média MELicenseStoreCleaned sera envoyé.</span><span class="sxs-lookup"><span data-stu-id="94e80-121">When the operation is complete, the media event MELicenseStoreCleaned will be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="94e80-122">*ppunkCancelationCookie* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="94e80-122">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94e80-123">Pointeur qui reçoit un pointeur vers l’interface **IUnknown** d’un objet qui identifie cet appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="94e80-123">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="94e80-124">Ce pointeur d’interface peut être utilisé pour annuler l’appel asynchrone en appelant la méthode [**IWMDRMEventGenerator :: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="94e80-124">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94e80-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="94e80-125">Return value</span></span>

<span data-ttu-id="94e80-126">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="94e80-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="94e80-127">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="94e80-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="94e80-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="94e80-128">Return code</span></span>                                                                                            | <span data-ttu-id="94e80-129">Description</span><span class="sxs-lookup"><span data-stu-id="94e80-129">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="94e80-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="94e80-130"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="94e80-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="94e80-131">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="94e80-132"><dt>**\_LICENSENOTFOUND DRM E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="94e80-132"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="94e80-133">Il n’existe pas de magasin de licences temporaire sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="94e80-133">There is no temporary license store on the client computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="94e80-134">Notes</span><span class="sxs-lookup"><span data-stu-id="94e80-134">Remarks</span></span>

<span data-ttu-id="94e80-135">Cette méthode s’exécute de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="94e80-135">This method executes asynchronously.</span></span> <span data-ttu-id="94e80-136">Elle retourne immédiatement après l’appel de, puis génère un événement **MEWMDRMLicenseStoreCleaned** lorsque le traitement est terminé.</span><span class="sxs-lookup"><span data-stu-id="94e80-136">It returns immediately after being called and then generates an **MEWMDRMLicenseStoreCleaned** event when processing is complete.</span></span>

<span data-ttu-id="94e80-137">Pour plus d’informations sur l’utilisation des méthodes asynchrones des API étendues du client Windows Media DRM, consultez [utilisation du modèle d’événement Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="94e80-137">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94e80-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94e80-138">Requirements</span></span>



| <span data-ttu-id="94e80-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94e80-139">Requirement</span></span> | <span data-ttu-id="94e80-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="94e80-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94e80-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="94e80-141">Header</span></span><br/>  | <dl> <span data-ttu-id="94e80-142"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="94e80-142"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="94e80-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="94e80-143">Library</span></span><br/> | <dl> <span data-ttu-id="94e80-144"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94e80-144"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94e80-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94e80-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94e80-146">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="94e80-146">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





