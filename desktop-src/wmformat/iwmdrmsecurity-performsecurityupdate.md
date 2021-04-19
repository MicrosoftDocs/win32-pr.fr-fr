---
title: Méthode IWMDRMSecurity PerformSecurityUpdate (wmdrmsdk. h)
description: La méthode PerformSecurityUpdate lance une mise à jour de sécurité pour le sous-système DRM sur l’ordinateur local.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Méthode PerformSecurityUpdate format Windows Media
- Méthode PerformSecurityUpdate format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode PerformSecurityUpdate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.PerformSecurityUpdate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34a1e92edd279655737a2e8f3b7ce4e77e27fd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530422"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a><span data-ttu-id="3c2fa-106">IWMDRMSecurity ::P méthode erformSecurityUpdate</span><span class="sxs-lookup"><span data-stu-id="3c2fa-106">IWMDRMSecurity::PerformSecurityUpdate method</span></span>

<span data-ttu-id="3c2fa-107">La méthode **PerformSecurityUpdate** lance une mise à jour de sécurité pour le sous-système DRM sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-107">The **PerformSecurityUpdate** method initiates a security update to the DRM subsystem on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2fa-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c2fa-108">Syntax</span></span>


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="3c2fa-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c2fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c2fa-110">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c2fa-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2fa-111">Option de mise à jour exprimée sous la forme de l’un des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-111">Update option expressed as one of the following flags.</span></span>



| <span data-ttu-id="3c2fa-112">Indicateur</span><span class="sxs-lookup"><span data-stu-id="3c2fa-112">Flag</span></span>                                          | <span data-ttu-id="3c2fa-113">Description</span><span class="sxs-lookup"><span data-stu-id="3c2fa-113">Description</span></span>                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2fa-114">\_sécurité WMDRM \_ exécuter \_ indiv</span><span class="sxs-lookup"><span data-stu-id="3c2fa-114">WMDRM\_SECURITY\_PERFORM\_INDIV</span></span>               | <span data-ttu-id="3c2fa-115">Fait en sorte que le composant DRM soit individualisé uniquement si la version du client est obsolète.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-115">Causes the DRM component to be individualized only if the version of the client is out of date.</span></span> |
| <span data-ttu-id="3c2fa-116">sécurité WMDRM effectuer l’actualisation de la \_ \_ \_ révocation \_</span><span class="sxs-lookup"><span data-stu-id="3c2fa-116">WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH</span></span> | <span data-ttu-id="3c2fa-117">Entraîne la mise à jour des listes de révocation sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-117">Causes the revocation lists on the client computer to be updated.</span></span>                               |
| <span data-ttu-id="3c2fa-118">\_forcer la sécurité WMDRM \_ \_ \_ indiv</span><span class="sxs-lookup"><span data-stu-id="3c2fa-118">WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV</span></span>        | <span data-ttu-id="3c2fa-119">Fait en sorte que le composant DRM soit individualisé même si la version du client est à jour.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-119">Causes the DRM component to be individualized even if the version of the client is up to date.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3c2fa-120">*ppunkCancelationCookie* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3c2fa-120">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2fa-121">Adresse d’une variable qui reçoit un pointeur vers un objet qui peut être utilisé pour annuler cette opération.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-121">Address of a variable that receives a pointer to an object that can be used to cancel this operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c2fa-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c2fa-122">Return value</span></span>

<span data-ttu-id="3c2fa-123">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3c2fa-124">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3c2fa-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3c2fa-125">Return code</span></span>                                                                          | <span data-ttu-id="3c2fa-126">Description</span><span class="sxs-lookup"><span data-stu-id="3c2fa-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3c2fa-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3c2fa-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3c2fa-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="3c2fa-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3c2fa-129">Notes</span><span class="sxs-lookup"><span data-stu-id="3c2fa-129">Remarks</span></span>

<span data-ttu-id="3c2fa-130">Cette méthode s’exécute de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-130">This method executes asynchronously.</span></span> <span data-ttu-id="3c2fa-131">Elle retourne immédiatement après l’appel de, puis génère des événements en fonction de l’indicateur défini dans le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="3c2fa-131">It returns immediately after being called and then generates events depending on the flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="3c2fa-132">Pour individualisation (l’indicateur défini sur la \_ sécurité WMDRM \_ perform \_ indiv ou WMDRM \_ Security \_ perform \_ force \_ indiv), une série d’événements **MEWMDRMIndividualizationProgress** est générée, suivie d’un événement **MEWMDRMIndividualizationCompleted** lorsque le traitement est terminé.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-132">For individualization (flag set to WMDRM\_SECURITY\_PERFORM\_INDIV or WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV), a series of **MEWMDRMIndividualizationProgress** events is generated followed by an **MEWMDRMIndividualizationCompleted** event when processing is complete.</span></span> <span data-ttu-id="3c2fa-133">La valeur de chacun des événements **MEWMDRMIndividualizationProgress** obtenus en appelant **IMFMediaEvent :: GetValue** est un pointeur **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="3c2fa-133">The value of each of the **MEWMDRMIndividualizationProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="3c2fa-134">Vous pouvez appeler la méthode **QueryInterface** de l’interface **IUnknown** Récupérée pour récupérer une instance de l’interface [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="3c2fa-134">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span>

<span data-ttu-id="3c2fa-135">Pour actualiser les listes de révocation (indicateur défini sur la \_ sécurité WMDRM \_ effectuer l' \_ \_ actualisation), un événement **MEWMDRMREvocationDownloadCompleted** est généré lorsque le traitement est terminé.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-135">For refreshing the revocation lists (flag set to WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH), an **MEWMDRMREvocationDownloadCompleted** event is generated when processing is complete.</span></span>

> [!Note]  
> <span data-ttu-id="3c2fa-136">Lorsque **PerformSecurityUpdate** termine l’individualisation, les seuls objets existants qui reflètent le nouvel État individualisé sont ceux qui héritent de **IWMDRMSecurity**.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-136">When **PerformSecurityUpdate** completes individualization, the only existing objects that will reflect the new individualized state are those that inherit from **IWMDRMSecurity**.</span></span> <span data-ttu-id="3c2fa-137">Tous les autres objets existants ne seront pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-137">All other existing objects will not be updated.</span></span> <span data-ttu-id="3c2fa-138">Vous devez libérer et recréer tous les autres objets pour qu’ils reflètent le nouvel État individualisé.</span><span class="sxs-lookup"><span data-stu-id="3c2fa-138">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

 

<span data-ttu-id="3c2fa-139">Pour plus d’informations sur l’utilisation des méthodes asynchrones des API étendues du client Windows Media DRM, consultez [utilisation du modèle d’événement Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="3c2fa-139">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c2fa-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c2fa-140">Requirements</span></span>



| <span data-ttu-id="3c2fa-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c2fa-141">Requirement</span></span> | <span data-ttu-id="3c2fa-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c2fa-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2fa-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c2fa-143">Header</span></span><br/>  | <dl> <span data-ttu-id="3c2fa-144"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c2fa-144"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c2fa-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c2fa-145">Library</span></span><br/> | <dl> <span data-ttu-id="3c2fa-146"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c2fa-146"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c2fa-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c2fa-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c2fa-148">**Révocation et renouvellement de composants automatisés**</span><span class="sxs-lookup"><span data-stu-id="3c2fa-148">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="3c2fa-149">**Exemple d’individualisation DRM**</span><span class="sxs-lookup"><span data-stu-id="3c2fa-149">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="3c2fa-150">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="3c2fa-150">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="3c2fa-151">**Réalisation de l’individualisation DRM**</span><span class="sxs-lookup"><span data-stu-id="3c2fa-151">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> </dl>

 

 





