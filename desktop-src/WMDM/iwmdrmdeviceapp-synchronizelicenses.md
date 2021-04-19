---
title: Méthode IWMDRMDeviceApp SynchronizeLicenses (WMDRMDeviceApp. h)
description: La méthode SynchronizeLicenses met à jour les licences sur un appareil lorsque celles-ci arrivent à expiration.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- Méthode SynchronizeLicenses Gestionnaire de périphériques Windows Media
- Méthode SynchronizeLicenses Gestionnaire de périphériques Windows Media, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques, méthode SynchronizeLicenses
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.SynchronizeLicenses
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08f3457fec55a0eb519419feddf4594a2cbfac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524059"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a><span data-ttu-id="e2fea-106">IWMDRMDeviceApp :: SynchronizeLicenses, méthode</span><span class="sxs-lookup"><span data-stu-id="e2fea-106">IWMDRMDeviceApp::SynchronizeLicenses method</span></span>

<span data-ttu-id="e2fea-107">La méthode **SynchronizeLicenses** met à jour les licences sur un appareil lorsque celles-ci arrivent à expiration.</span><span class="sxs-lookup"><span data-stu-id="e2fea-107">The **SynchronizeLicenses** method updates licenses on a device when they are close to expiring.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2fea-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2fea-108">Syntax</span></span>


```C++
HRESULT SynchronizeLicenses(
  [in] IWMDMDevice    *pDevice,
  [in] IWMDMProgress3 *pProgressCallback,
  [in] DWORD          cMinCountThreshold,
  [in] DWORD          cMinHoursThreshold
);
```



## <a name="parameters"></a><span data-ttu-id="e2fea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2fea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2fea-110">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2fea-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fea-111">Pointeur vers un objet [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="e2fea-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="e2fea-112">*pProgressCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2fea-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fea-113">Rappel de progression qui reçoit la progression de toutes les étapes qu’il peut être amené à effectuer. L’étape est identifiée par le paramètre *eventID* de la méthode [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) appelée.</span><span class="sxs-lookup"><span data-stu-id="e2fea-113">Progress callback that will receive progress of any steps that it might need to carry out. The step is identified by the *EventId* parameter of the [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) method called.</span></span>

</dd> <dt>

<span data-ttu-id="e2fea-114">*cMinCountThreshold* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2fea-114">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fea-115">Nombre minimal de jeux de lecture restant facultatif sur une licence d’appareil.</span><span class="sxs-lookup"><span data-stu-id="e2fea-115">Optional minimum remaining play count on a device license.</span></span>

</dd> <dt>

<span data-ttu-id="e2fea-116">*cMinHoursThreshold* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2fea-116">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2fea-117">Heures restantes minimales facultatives sur une licence d’appareil.</span><span class="sxs-lookup"><span data-stu-id="e2fea-117">Optional minimum remaining hours on a device license.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2fea-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e2fea-118">Return value</span></span>

<span data-ttu-id="e2fea-119">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e2fea-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e2fea-120">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e2fea-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e2fea-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e2fea-121">Return code</span></span>                                                                                                         | <span data-ttu-id="e2fea-122">Description</span><span class="sxs-lookup"><span data-stu-id="e2fea-122">Description</span></span>                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e2fea-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fea-123"><dt>**S\_OK**</dt></span></span> </dl>                                | <span data-ttu-id="e2fea-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2fea-124">The method succeeded.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="e2fea-125"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fea-125"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="e2fea-126">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e2fea-126">One or more arguments are not valid.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="e2fea-127"><dt>**\_INVALIDXMLTAG DRM E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fea-127"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>                | <span data-ttu-id="e2fea-128">Le format XML est incorrect.</span><span class="sxs-lookup"><span data-stu-id="e2fea-128">XML is improperly formed.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="e2fea-129"><dt>**\_NOTIMPL DRM E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fea-129"><dt>**DRM\_E\_NOTIMPL**</dt></span></span> </dl>                      | <span data-ttu-id="e2fea-130">Cette fonctionnalité n’est pas implémentée pour le moment.</span><span class="sxs-lookup"><span data-stu-id="e2fea-130">This functionality is not currently implemented.</span></span> <span data-ttu-id="e2fea-131">(SyncLicenses w/ *pDevice* = null)</span><span class="sxs-lookup"><span data-stu-id="e2fea-131">(SyncLicenses w/ *pDevice* =NULL)</span></span><br/>                                                               |
| <dl> <span data-ttu-id="e2fea-132"><dt>**\_NOXMLCLOSETAG DRM E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fea-132"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>                | <span data-ttu-id="e2fea-133">Le code XML de la licence est incorrect.</span><span class="sxs-lookup"><span data-stu-id="e2fea-133">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="e2fea-134"><dt>**\_NOXMLOPENTAG DRM E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fea-134"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>                 | <span data-ttu-id="e2fea-135">Le code XML de la licence est incorrect.</span><span class="sxs-lookup"><span data-stu-id="e2fea-135">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="e2fea-136"><dt>**\_OUTOFMEMORY DRM E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fea-136"><dt>**DRM\_E\_OUTOFMEMORY**</dt></span></span> </dl>                  | <span data-ttu-id="e2fea-137">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="e2fea-137">Out of memory.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="e2fea-138"><dt>**\_XMLNOTFOUND DRM E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fea-138"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>                  | <span data-ttu-id="e2fea-139">Impossible de trouver une balise XML obligatoire dans la licence.</span><span class="sxs-lookup"><span data-stu-id="e2fea-139">Failed to find a required XML tag in the license.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="e2fea-140"><dt>**appareil \_ NS \_ E \_ non \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fea-140"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>    | <span data-ttu-id="e2fea-141">L’appareil spécifié n’est pas un périphérique compatible DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e2fea-141">The specified device is not a Windows Media DRM-compatible device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="e2fea-142"><dt>**l' \_ \_ individualisation des droits de l’utilisateur NS E \_ a besoin \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e2fea-142"><dt>**NS\_E\_DRM\_NEEDS\_INDIVIDUALIZATION**</dt></span></span> </dl> | <span data-ttu-id="e2fea-143">La DRM requiert une boîte noire individualisée pour exécuter cette fonction.</span><span class="sxs-lookup"><span data-stu-id="e2fea-143">The DRM requires an individualized black box to perform this function.</span></span> <span data-ttu-id="e2fea-144">En d’autres termes, le kit de développement logiciel (SDK) du format Windows Media requiert une mise à niveau de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e2fea-144">In other words, the Windows Media Format SDK requires a security upgrade.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e2fea-145">Notes</span><span class="sxs-lookup"><span data-stu-id="e2fea-145">Remarks</span></span>

<span data-ttu-id="e2fea-146">Cet appel ne peut être effectué que sur un appareil qui prend en charge Windows Media DRM 10 pour les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="e2fea-146">This call can only be made on a device that supports Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="e2fea-147">Vous devez spécifier au moins un paramètre de seuil.</span><span class="sxs-lookup"><span data-stu-id="e2fea-147">You must specify at least one threshold parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2fea-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2fea-148">Requirements</span></span>



| <span data-ttu-id="e2fea-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2fea-149">Requirement</span></span> | <span data-ttu-id="e2fea-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2fea-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2fea-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2fea-151">Header</span></span><br/>  | <dl> <span data-ttu-id="e2fea-152"><dt>WMDRMDeviceApp. h (nécessite également Wmdrmdeviceapp \_ i. c, créé à partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="e2fea-152"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="e2fea-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e2fea-153">Library</span></span><br/> | <dl> <span data-ttu-id="e2fea-154"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2fea-154"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="e2fea-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2fea-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2fea-156">**Gestion du contenu protégé dans l’application**</span><span class="sxs-lookup"><span data-stu-id="e2fea-156">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="e2fea-157">**Interface IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="e2fea-157">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="e2fea-158">**Interface IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="e2fea-158">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





