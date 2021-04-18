---
title: Méthode IWMDRMDeviceApp AcquireDeviceData (WMDRMDeviceApp. h)
description: La méthode AcquireDeviceData Initialise ou réinitialise une horloge sécurisée d’appareil.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- Méthode AcquireDeviceData Gestionnaire de périphériques Windows Media
- Méthode AcquireDeviceData Gestionnaire de périphériques Windows Media, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques, méthode AcquireDeviceData
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.AcquireDeviceData
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268572e5dad3dffd0fe15956a0ff145f277fb6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540457"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a><span data-ttu-id="1cce2-106">IWMDRMDeviceApp :: AcquireDeviceData, méthode</span><span class="sxs-lookup"><span data-stu-id="1cce2-106">IWMDRMDeviceApp::AcquireDeviceData method</span></span>

<span data-ttu-id="1cce2-107">La méthode **AcquireDeviceData** Initialise ou réinitialise une horloge sécurisée d’appareil.</span><span class="sxs-lookup"><span data-stu-id="1cce2-107">The **AcquireDeviceData** method initializes or resets a device secure clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cce2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cce2-108">Syntax</span></span>


```C++
HRESULT AcquireDeviceData(
  [in]  IWMDMDevice    *pDevice,
  [in]  IWMDMProgress3 *pProgressCallback,
  [in]  DWORD          dwFlags,
  [out] DWORD          *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="1cce2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cce2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cce2-110">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cce2-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cce2-111">Pointeur vers une interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) pour l’appareil qui signale les données de contrôle.</span><span class="sxs-lookup"><span data-stu-id="1cce2-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface for the device that will report metering data.</span></span>

</dd> <dt>

<span data-ttu-id="1cce2-112">*pProgressCallback* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cce2-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cce2-113">Rappel de progression via lequel l’application peut suivre la progression de l’événement ou annuler l’événement.</span><span class="sxs-lookup"><span data-stu-id="1cce2-113">Progress callback through which the application can track the progress of the event, or cancel the event.</span></span> <span data-ttu-id="1cce2-114">La progression est identifiée par le paramètre *eventID* des méthodes [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) .</span><span class="sxs-lookup"><span data-stu-id="1cce2-114">The progress is identified by the *EventId* parameter of [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) methods.</span></span>

</dd> <dt>

<span data-ttu-id="1cce2-115">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cce2-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cce2-116">**Or** logique de l’un des indicateurs suivants, en spécifiant l’action à effectuer.</span><span class="sxs-lookup"><span data-stu-id="1cce2-116">A logical **OR** of one or both of the following flags, specifying what action to perform.</span></span> <span data-ttu-id="1cce2-117">Cette valeur est extraite du paramètre *pdwStatus* de [**IWMDRMDeviceApp :: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) ou [**IWMDRMDeviceApp2 :: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span><span class="sxs-lookup"><span data-stu-id="1cce2-117">This value is retrieved from the *pdwStatus* parameter of [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span> <span data-ttu-id="1cce2-118">Vous pouvez utiliser l’indicateur *pdwStatus* directement.</span><span class="sxs-lookup"><span data-stu-id="1cce2-118">You can use the *pdwStatus* flag directly.</span></span>



| <span data-ttu-id="1cce2-119">Indicateur</span><span class="sxs-lookup"><span data-stu-id="1cce2-119">Flag</span></span>                        | <span data-ttu-id="1cce2-120">Description</span><span class="sxs-lookup"><span data-stu-id="1cce2-120">Description</span></span>                                   |
|-----------------------------|-----------------------------------------------|
| <span data-ttu-id="1cce2-121">\_NEEDCLOCK d’appareil WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="1cce2-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="1cce2-122">Acquérir une horloge à partir d’un serveur d’horloge sécurisé.</span><span class="sxs-lookup"><span data-stu-id="1cce2-122">Acquire a clock from a secure clock server.</span></span>   |
| <span data-ttu-id="1cce2-123">\_REFRESHCLOCK d’appareil WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="1cce2-123">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="1cce2-124">Actualisez l’horloge à partir d’un serveur d’horloge sécurisé.</span><span class="sxs-lookup"><span data-stu-id="1cce2-124">Refresh the clock from a secure clock server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1cce2-125">*pdwStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1cce2-125">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cce2-126">Une des valeurs **DWORD** suivantes spécifiant l’état retourné par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1cce2-126">One of the following **DWORD** values specifying the status returned by the device.</span></span>



| <span data-ttu-id="1cce2-127">Statut</span><span class="sxs-lookup"><span data-stu-id="1cce2-127">Status</span></span> | <span data-ttu-id="1cce2-128">Description</span><span class="sxs-lookup"><span data-stu-id="1cce2-128">Description</span></span>                                                     |
|--------|-----------------------------------------------------------------|
| <span data-ttu-id="1cce2-129">0</span><span class="sxs-lookup"><span data-stu-id="1cce2-129">0</span></span>      | <span data-ttu-id="1cce2-130">L’action n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1cce2-130">The action is not supported.</span></span>                                    |
| <span data-ttu-id="1cce2-131">1</span><span class="sxs-lookup"><span data-stu-id="1cce2-131">1</span></span>      | <span data-ttu-id="1cce2-132">L’horloge sécurisée de l’appareil n’a pas pu être acquise auprès du service.</span><span class="sxs-lookup"><span data-stu-id="1cce2-132">The device secure clock could not be acquired from the service.</span></span> |
| <span data-ttu-id="1cce2-133">2</span><span class="sxs-lookup"><span data-stu-id="1cce2-133">2</span></span>      | <span data-ttu-id="1cce2-134">L’horloge sécurisée de l’appareil n’a pas pu être définie.</span><span class="sxs-lookup"><span data-stu-id="1cce2-134">The device's secure clock could not be set.</span></span>                     |
| <span data-ttu-id="1cce2-135">3</span><span class="sxs-lookup"><span data-stu-id="1cce2-135">3</span></span>      | <span data-ttu-id="1cce2-136">L’horloge sécurisée de l’appareil a été définie.</span><span class="sxs-lookup"><span data-stu-id="1cce2-136">The device's secure clock was set.</span></span>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cce2-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cce2-137">Return value</span></span>

<span data-ttu-id="1cce2-138">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1cce2-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1cce2-139">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1cce2-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1cce2-140">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1cce2-140">Return code</span></span>                                                                                                                             | <span data-ttu-id="1cce2-141">Description</span><span class="sxs-lookup"><span data-stu-id="1cce2-141">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1cce2-142"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1cce2-142"><dt>**S\_OK**</dt></span></span> </dl>                                                    | <span data-ttu-id="1cce2-143">S_OK</span><span class="sxs-lookup"><span data-stu-id="1cce2-143">The method succeeded.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="1cce2-144"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1cce2-144"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                                       | <span data-ttu-id="1cce2-145">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="1cce2-145">One or more arguments are not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="1cce2-146"><dt>**appareil \_ NS \_ E \_ non \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1cce2-146"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>                        | <span data-ttu-id="1cce2-147">L’appareil spécifié n’est pas un périphérique compatible DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1cce2-147">The specified device is not a Windows Media DRM compatible device.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="1cce2-148"><dt>**la \_ \_ protection d’accès du service d’E/DRM \_ ne peut pas \_ obtenir un \_ \_ \_ réveil sécurisé**</dt></span><span class="sxs-lookup"><span data-stu-id="1cce2-148"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="1cce2-149">Impossible de récupérer le challenge d’horloge sécurisée à partir de l’appareil ou de récupérer l’URL d’horloge sécurisée à partir de la demande.</span><span class="sxs-lookup"><span data-stu-id="1cce2-149">Failed to retrieve secure clock challenge from the device or unable to retrieve the secure clock URL from the challenge.</span></span><br/> |
| <dl> <span data-ttu-id="1cce2-150"><dt>**NS \_ E \_ DRM \_ ne peut pas \_ \_ obtenir une \_ horloge sécurisée \_ \_ à partir du \_ serveur**</dt></span><span class="sxs-lookup"><span data-stu-id="1cce2-150"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK\_FROM\_SERVER**</dt></span></span> </dl> | <span data-ttu-id="1cce2-151">Échec de la récupération de la réponse d’horloge sécurisée à partir du serveur d’horloge sécurisé.</span><span class="sxs-lookup"><span data-stu-id="1cce2-151">Failed to retrieve the secure clock response from the secure clock server.</span></span><br/>                                               |
| <dl> <span data-ttu-id="1cce2-152"><dt>**NS \_ E \_ DRM \_ ne peut pas \_ \_ définir l' \_ horloge sécurisée \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1cce2-152"><dt>**NS\_E\_DRM\_UNABLE\_TO\_SET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="1cce2-153">Impossible d’envoyer le challenge d’horloge sécurisée à l’appareil, ou l’appareil n’a pas pu définir l’horloge.</span><span class="sxs-lookup"><span data-stu-id="1cce2-153">Failed to send the secure clock challenge to the device, or the device failed to set the clock.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="1cce2-154">Notes</span><span class="sxs-lookup"><span data-stu-id="1cce2-154">Remarks</span></span>

<span data-ttu-id="1cce2-155">Il s’agit d’une méthode asynchrone ; l’appareil doit attendre le rappel [**IWMDMProgress :: end**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) pour cette opération avant de tenter de lire un contenu sous licence.</span><span class="sxs-lookup"><span data-stu-id="1cce2-155">This is an asynchronous method; the device must await the [**IWMDMProgress::End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) callback for this operation before attempting to play any licensed content.</span></span>

<span data-ttu-id="1cce2-156">Une application peut déterminer si l’horloge de l’appareil doit être réinitialisée ou mise à jour en appelant [**IWMDRMDeviceApp :: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) ou [**IWMDRMDeviceApp2 :: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span><span class="sxs-lookup"><span data-stu-id="1cce2-156">An application can learn if the device must have its clock reset or updated by calling [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span>

<span data-ttu-id="1cce2-157">Votre application doit disposer d’une connexion Internet pour lui permettre d’acquérir ou de réinitialiser une horloge sécurisée.</span><span class="sxs-lookup"><span data-stu-id="1cce2-157">Your application must have an Internet connection to enable it to acquire or reset a secure clock.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cce2-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cce2-158">Requirements</span></span>



| <span data-ttu-id="1cce2-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cce2-159">Requirement</span></span> | <span data-ttu-id="1cce2-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cce2-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cce2-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cce2-161">Header</span></span><br/>  | <dl> <span data-ttu-id="1cce2-162"><dt>WMDRMDeviceApp. h (nécessite également Wmdrmdeviceapp \_ i. c, créé à partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="1cce2-162"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="1cce2-163">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1cce2-163">Library</span></span><br/> | <dl> <span data-ttu-id="1cce2-164"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cce2-164"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="1cce2-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cce2-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cce2-166">**Gestion du contenu protégé dans l’application**</span><span class="sxs-lookup"><span data-stu-id="1cce2-166">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="1cce2-167">**Interface IWMDMDevice**</span><span class="sxs-lookup"><span data-stu-id="1cce2-167">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="1cce2-168">**Interface IWMDMProgress3**</span><span class="sxs-lookup"><span data-stu-id="1cce2-168">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="1cce2-169">**Interface IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="1cce2-169">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





