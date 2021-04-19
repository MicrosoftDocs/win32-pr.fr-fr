---
title: Méthode IWMDRMDeviceApp GenerateMeterChallenge (WMDRMDeviceApp. h)
description: La méthode GenerateMeterChallenge acquiert des données de contrôle à partir d’un appareil.
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- Méthode GenerateMeterChallenge Gestionnaire de périphériques Windows Media
- Méthode GenerateMeterChallenge Gestionnaire de périphériques Windows Media, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques, méthode GenerateMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.GenerateMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a71f04a5837f09575a2f4bccf4b17e34e30d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528510"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a><span data-ttu-id="d7642-106">IWMDRMDeviceApp :: GenerateMeterChallenge, méthode</span><span class="sxs-lookup"><span data-stu-id="d7642-106">IWMDRMDeviceApp::GenerateMeterChallenge method</span></span>

<span data-ttu-id="d7642-107">La méthode **GenerateMeterChallenge** acquiert des données de contrôle à partir d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="d7642-107">The **GenerateMeterChallenge** method acquires metering data from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7642-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7642-108">Syntax</span></span>


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a><span data-ttu-id="d7642-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7642-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7642-110">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7642-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7642-111">Pointeur vers une interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="d7642-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="d7642-112">Si l’application transmet la **valeur null**, les informations de contrôle stockées sur l’ordinateur sont utilisées à la place des informations de contrôle d’un appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="d7642-112">If the application passes in **NULL**, metering information stored on the computer is used instead of metering information from a connected device.</span></span>

</dd> <dt>

<span data-ttu-id="d7642-113">*bstrMeterCert* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7642-113">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7642-114">Le certificat de contrôle de l’application, en tant que **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="d7642-114">The application's metering certificate, as a **BSTR**.</span></span> <span data-ttu-id="d7642-115">Il s’agit d’un certificat signé reçu de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d7642-115">This is a signed certificate received from Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="d7642-116">*pbstrMeterURL* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d7642-116">*pbstrMeterURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7642-117">URL à laquelle les données de contrôle doivent être envoyées.</span><span class="sxs-lookup"><span data-stu-id="d7642-117">The URL where metering data should be sent.</span></span> <span data-ttu-id="d7642-118">Elle est allouée par les Gestionnaire de périphériques Windows Media et doit être libérée par l’appelant à l’aide de **SysFreeString**.</span><span class="sxs-lookup"><span data-stu-id="d7642-118">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> <dt>

<span data-ttu-id="d7642-119">*pbstrMeterData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d7642-119">*pbstrMeterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7642-120">Données de contrôle à envoyer au service de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d7642-120">Metering data to send to the metering service.</span></span> <span data-ttu-id="d7642-121">Elle est allouée par les Gestionnaire de périphériques Windows Media et doit être libérée par l’appelant à l’aide de **SysFreeString**.</span><span class="sxs-lookup"><span data-stu-id="d7642-121">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7642-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7642-122">Return value</span></span>

<span data-ttu-id="d7642-123">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d7642-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d7642-124">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d7642-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d7642-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d7642-125">Return code</span></span>                                                                                                      | <span data-ttu-id="d7642-126">Description</span><span class="sxs-lookup"><span data-stu-id="d7642-126">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7642-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d7642-127"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="d7642-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="d7642-128">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="d7642-129"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d7642-129"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="d7642-130">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="d7642-130">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="d7642-131"><dt>**\_INVALIDXMLTAG DRM E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7642-131"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>             | <span data-ttu-id="d7642-132">Le format XML est incorrect.</span><span class="sxs-lookup"><span data-stu-id="d7642-132">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="d7642-133"><dt>**\_NOXMLCLOSETAG DRM E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7642-133"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>             | <span data-ttu-id="d7642-134">Le format XML est incorrect.</span><span class="sxs-lookup"><span data-stu-id="d7642-134">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="d7642-135"><dt>**\_NOXMLOPENTAG DRM E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7642-135"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>              | <span data-ttu-id="d7642-136">Le format XML est incorrect.</span><span class="sxs-lookup"><span data-stu-id="d7642-136">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="d7642-137"><dt>**\_XMLNOTFOUND DRM E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7642-137"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>               | <span data-ttu-id="d7642-138">Impossible de trouver une balise XML obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d7642-138">Failed to find a required XML tag.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d7642-139"><dt>**Erreurs de l’appareil**</dt></span><span class="sxs-lookup"><span data-stu-id="d7642-139"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="d7642-140">Un certain nombre d’erreurs d’appareil.</span><span class="sxs-lookup"><span data-stu-id="d7642-140">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="d7642-141"><dt>**Erreurs du client DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="d7642-141"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="d7642-142">L’une des nombreuses erreurs internes du client DRM.</span><span class="sxs-lookup"><span data-stu-id="d7642-142">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="d7642-143"><dt>**appareil \_ NS \_ E \_ non \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7642-143"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="d7642-144">L’appareil spécifié n’est pas un périphérique compatible DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d7642-144">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7642-145">Notes</span><span class="sxs-lookup"><span data-stu-id="d7642-145">Remarks</span></span>

<span data-ttu-id="d7642-146">Avant d’appeler cette méthode, l’application doit appeler [**IWMDRMDeviceApp :: QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) ou [**IWMDRMDeviceApp2 :: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) pour vérifier que tous les composants DRM de l’appareil sont à jour.</span><span class="sxs-lookup"><span data-stu-id="d7642-146">Before calling this method, the application should call [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) to verify that all the device's DRM components are up to date.</span></span> <span data-ttu-id="d7642-147">Cette méthode peut uniquement être appelée sur un appareil qui prend en charge Windows Media DRM 10 pour les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="d7642-147">This method can only be called on a device that supports Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="d7642-148">Le *pbstrMeterData* de données extrait doit être envoyé à l’URL spécifiée par *pbstrMeterURL*.</span><span class="sxs-lookup"><span data-stu-id="d7642-148">The retrieved data *pbstrMeterData* should be sent to the URL specified by *pbstrMeterURL*.</span></span> <span data-ttu-id="d7642-149">Veillez à encoder les données récupérées par URL afin qu’elles ne soient pas modifiées pendant le transfert.</span><span class="sxs-lookup"><span data-stu-id="d7642-149">Be sure to URL-encode the retrieved data so that it does not get modified during transfer.</span></span>

<span data-ttu-id="d7642-150">Pour plus d’informations, consultez [gestion du contenu protégé dans l’application](handling-protected-content-in-the-application.md) .</span><span class="sxs-lookup"><span data-stu-id="d7642-150">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="d7642-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="d7642-151">Examples</span></span>

<span data-ttu-id="d7642-152">L’exemple de code C++ suivant crée un objet **WMDRMDeviceApp** , vérifie que l’appareil est un appareil Windows Media DRM 10, que son horloge est exacte, puis demande les données de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d7642-152">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


```C++
HRESULT hr = S_OK;
// Create the WMDRMDeviceApp object.
CComPtr<IWMDRMDeviceApp> pDRM;
hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

// Find out first if the device is a WMDRM 10 device, and if it requires
// any clock updates.
DWORD status = 0;
hr = pDRM->QueryDeviceStatus(pDevice, &status);

if (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. Nothing can be updated,
    return E_FAIL;                   // and metering cannot be performed.
else if (status & WMDRM_DEVICE_REVOKED) // Device is revoked.
    return E_FAIL;
else if (status & WMDRM_DEVICE_NEEDCLOCK || 
    status & WMDRM_CLIENT_NEEDINDIV ||
    status & WMDRM_DEVICE_REFRESHCLOCK)
{
    // Need to update device clock. 
    // Using custom function, which is synchronous.
    hr = myAcquireDeviceData(pDRM, pDevice, this, status, &result);
    if (hr != S_OK || result != 0)    // Couldn't perform the updates.
        return E_FAIL;    
}

// Any updates have been performed. Now get the metering information from the device.
CComBSTR meterCert(METERCERT);
CComBSTR URL;
CComBSTR rawdata;
CComBSTR data;
hr = pDRM->GenerateMeterChallenge(pDevice, meterCert, &URL, &rawdata);
if (hr == S_OK)
    ..... Send to URL...
```



## <a name="requirements"></a><span data-ttu-id="d7642-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7642-153">Requirements</span></span>



| <span data-ttu-id="d7642-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7642-154">Requirement</span></span> | <span data-ttu-id="d7642-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7642-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7642-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7642-156">Header</span></span><br/>  | <dl> <span data-ttu-id="d7642-157"><dt>WMDRMDeviceApp. h (nécessite également Wmdrmdeviceapp \_ i. c, créé à partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="d7642-157"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="d7642-158">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d7642-158">Library</span></span><br/> | <dl> <span data-ttu-id="d7642-159"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7642-159"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="d7642-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7642-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7642-161">**Gestion du contenu protégé dans l’application**</span><span class="sxs-lookup"><span data-stu-id="d7642-161">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="d7642-162">**Interface IWMDMDevice**</span><span class="sxs-lookup"><span data-stu-id="d7642-162">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="d7642-163">**Interface IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="d7642-163">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





