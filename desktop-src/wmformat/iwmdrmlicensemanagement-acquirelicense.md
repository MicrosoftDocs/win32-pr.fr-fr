---
title: IWMDRMLicenseManagement AcquireLicense, méthode (wmdrmsdk. h)
description: La méthode AcquireLicense acquiert de manière asynchrone une licence à partir d’une URL spécifiée.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- Méthode AcquireLicense format Windows Media
- Méthode AcquireLicense format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, AcquireLicense, méthode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.AcquireLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 279a3d4d84617c4a4fa5454d1f39f6f78f0cf3fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523587"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a><span data-ttu-id="3fc9a-106">IWMDRMLicenseManagement :: AcquireLicense, méthode</span><span class="sxs-lookup"><span data-stu-id="3fc9a-106">IWMDRMLicenseManagement::AcquireLicense method</span></span>

<span data-ttu-id="3fc9a-107">La méthode **AcquireLicense** acquiert de manière asynchrone une licence à partir d’une URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-107">The **AcquireLicense** method asynchronously acquires a license from a specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fc9a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fc9a-108">Syntax</span></span>


```C++
HRESULT AcquireLicense(
  [in]  BSTR     bstrURL,
  [in]  BSTR     bstrHeaderData,
  [in]  BSTR     bstrActions,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="3fc9a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3fc9a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fc9a-110">*du bstrURL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3fc9a-110">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fc9a-111">URL du serveur de licences à partir duquel acquérir la licence.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-111">URL of the license server from which to acquire the license.</span></span> <span data-ttu-id="3fc9a-112">Transmettez la **valeur null** pour que la méthode analyse l’URL à partir de l’en-tête de contenu.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-112">Pass **NULL** to have the method parse the URL from the content header.</span></span>

</dd> <dt>

<span data-ttu-id="3fc9a-113">*bstrHeaderData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3fc9a-113">*bstrHeaderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fc9a-114">En-tête de contenu à transmettre au serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-114">Content header to be passed to the license server.</span></span> <span data-ttu-id="3fc9a-115">Si *du bstrURL* a la **valeur null**, la méthode analyse l’URL à partir de cet en-tête.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-115">If *bstrURL* is **NULL**, the method will parse the URL from this header.</span></span> <span data-ttu-id="3fc9a-116">Si *dwFlags* est défini sur WMDRM \_ Acquire la \_ licence \_ héritée \_ non silencieuse, définissez cette valeur sur l’ID de clé au lieu de l’en-tête de contenu entier.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-116">If *dwFlags* is set to WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT, set this value to the key ID instead of the entire content header.</span></span>

</dd> <dt>

<span data-ttu-id="3fc9a-117">*bstrActions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3fc9a-117">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fc9a-118">Chaîne contenant zéro, une ou plusieurs actions pour lesquelles une autorisation doit être demandée dans la licence.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-118">String containing zero or more actions for which to request permission in the license.</span></span> <span data-ttu-id="3fc9a-119">La chaîne doit être mise en forme de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="3fc9a-119">The string must be formatted as follows:</span></span>

-   <span data-ttu-id="3fc9a-120">Chaque action doit être définie dans un élément ACTION.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-120">Each action must be defined within an ACTION element.</span></span> <span data-ttu-id="3fc9a-121">Les données de l’élément sont la chaîne d’action.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-121">The data of the element is the action string.</span></span>
-   <span data-ttu-id="3fc9a-122">Tous les éléments ACTION doivent être contenus dans un élément ACTIONLIST.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-122">All ACTION elements must be contained within an ACTIONLIST element.</span></span>

    <span data-ttu-id="3fc9a-123">Par exemple, la chaîne permettant de demander une licence pour lire du contenu est au format suivant :</span><span class="sxs-lookup"><span data-stu-id="3fc9a-123">For example, the string to request a license to play content is formatted like this:</span></span>

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

<span data-ttu-id="3fc9a-124">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3fc9a-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fc9a-125">Indicateurs d’option d’acquisition de licence.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-125">License acquisition option flags.</span></span> <span data-ttu-id="3fc9a-126">Définissez l’une des constantes dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-126">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="3fc9a-127">Constante</span><span class="sxs-lookup"><span data-stu-id="3fc9a-127">Constant</span></span>                                   | <span data-ttu-id="3fc9a-128">Description</span><span class="sxs-lookup"><span data-stu-id="3fc9a-128">Description</span></span>                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc9a-129">licence d’acquisition WMDRM en \_ \_ \_ mode silencieux</span><span class="sxs-lookup"><span data-stu-id="3fc9a-129">WMDRM\_ACQUIRE\_LICENSE\_SILENT</span></span>            | <span data-ttu-id="3fc9a-130">La licence sera émise directement sur Internet sans aucune confirmation de la part de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-130">The license will be issued directly over the Internet without any confirmation from the client application.</span></span>              |
| <span data-ttu-id="3fc9a-131">licence d’acquisition WMDRM sans \_ \_ \_ silence</span><span class="sxs-lookup"><span data-stu-id="3fc9a-131">WMDRM\_ACQUIRE\_LICENSE\_NONSILENT</span></span>         | <span data-ttu-id="3fc9a-132">Le sous-système DRM crée une demande de licence qui est renvoyée de manière asynchrone pour la publication sur le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-132">The DRM subsystem will create a license request which will be returned asynchronously for posting to the license server.</span></span> |
| <span data-ttu-id="3fc9a-133">l’héritage de la licence d’acquisition WMDRM n’est pas \_ \_ \_ \_ silencieux</span><span class="sxs-lookup"><span data-stu-id="3fc9a-133">WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT</span></span> | <span data-ttu-id="3fc9a-134">Identique à la \_ licence d’acquisition WMDRM sans \_ \_ silence, sauf qu’une demande de licence DRM version 1 sera créée.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-134">The same as WMDRM\_ACQUIRE\_LICENSE\_NONSILENT, except that a DRM version 1 license challenge will be created.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="3fc9a-135">*ppunkCancelationCookie* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3fc9a-135">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fc9a-136">Pointeur qui reçoit un pointeur vers l’interface **IUnknown** d’un objet qui identifie cet appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-136">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="3fc9a-137">Ce pointeur d’interface peut être utilisé pour annuler l’appel asynchrone en appelant la méthode [**IWMDRMEventGenerator :: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="3fc9a-137">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fc9a-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3fc9a-138">Return value</span></span>

<span data-ttu-id="3fc9a-139">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3fc9a-140">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3fc9a-141">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3fc9a-141">Return code</span></span>                                                                          | <span data-ttu-id="3fc9a-142">Description</span><span class="sxs-lookup"><span data-stu-id="3fc9a-142">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3fc9a-143"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3fc9a-143"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3fc9a-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="3fc9a-144">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3fc9a-145">Notes</span><span class="sxs-lookup"><span data-stu-id="3fc9a-145">Remarks</span></span>

<span data-ttu-id="3fc9a-146">Cette méthode s’exécute de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-146">This method executes asynchronously.</span></span> <span data-ttu-id="3fc9a-147">Elle retourne immédiatement après l’appel de, puis génère un événement **MEWMDRMLicenseAcquisitionCompleted** lorsque le traitement est terminé.</span><span class="sxs-lookup"><span data-stu-id="3fc9a-147">It returns immediately after being called and then generates an **MEWMDRMLicenseAcquisitionCompleted** event when processing is complete.</span></span> <span data-ttu-id="3fc9a-148">Pour les opérations d’acquisition de licence non silencieuses, la valeur de l’événement obtenu en appelant **IMFMediaEvent :: GetValue** est un pointeur **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="3fc9a-148">For non-silent license acquisition operations, the value of the event obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="3fc9a-149">Vous pouvez appeler la méthode **QueryInterface** de l’interface **IUnknown** Récupérée pour récupérer une instance de l’interface [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .</span><span class="sxs-lookup"><span data-stu-id="3fc9a-149">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>

<span data-ttu-id="3fc9a-150">Pour plus d’informations sur l’utilisation des méthodes asynchrones des API étendues du client Windows Media DRM, consultez [utilisation du modèle d’événement Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="3fc9a-150">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fc9a-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fc9a-151">Requirements</span></span>



| <span data-ttu-id="3fc9a-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3fc9a-152">Requirement</span></span> | <span data-ttu-id="3fc9a-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fc9a-153">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc9a-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="3fc9a-154">Header</span></span><br/>  | <dl> <span data-ttu-id="3fc9a-155"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fc9a-155"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3fc9a-156">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3fc9a-156">Library</span></span><br/> | <dl> <span data-ttu-id="3fc9a-157"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fc9a-157"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fc9a-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fc9a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fc9a-159">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="3fc9a-159">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="3fc9a-160">**Acquisition de licence en mode silencieux**</span><span class="sxs-lookup"><span data-stu-id="3fc9a-160">**Silent License Acquisition**</span></span>](silent-license-acquisition.md)
</dt> </dl>

 

 





