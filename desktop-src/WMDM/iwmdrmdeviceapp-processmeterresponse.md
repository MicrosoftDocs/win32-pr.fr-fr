---
title: Méthode IWMDRMDeviceApp ProcessMeterResponse (WMDRMDeviceApp. h)
description: La méthode ProcessMeterResponse réinitialise tout ou partie des nombres de contrôle sur un appareil, une fois que les données de l’appareil ont été envoyées et traitées par le serveur.
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- Méthode ProcessMeterResponse Gestionnaire de périphériques Windows Media
- Méthode ProcessMeterResponse Gestionnaire de périphériques Windows Media, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques, méthode ProcessMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.ProcessMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b57312dc2f401207e41f38f5bf75cddf69a13b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545470"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a><span data-ttu-id="83adc-106">IWMDRMDeviceApp ::P méthode rocessMeterResponse</span><span class="sxs-lookup"><span data-stu-id="83adc-106">IWMDRMDeviceApp::ProcessMeterResponse method</span></span>

<span data-ttu-id="83adc-107">La méthode **ProcessMeterResponse** réinitialise tout ou partie des nombres de contrôle sur un appareil, une fois que les données de l’appareil ont été envoyées et traitées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="83adc-107">The **ProcessMeterResponse** method resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="83adc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83adc-108">Syntax</span></span>


```C++
HRESULT ProcessMeterResponse(
  [in]  IWMDMDevice *pDevice,
  [in]  BYTE        *pbResponse,
  [in]  DWORD       cbResponse,
  [out] DWORD       *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="83adc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83adc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83adc-110">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83adc-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83adc-111">Pointeur vers un objet [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="83adc-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="83adc-112">*pbResponse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83adc-112">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83adc-113">Réponse reçue d’un serveur de contrôle, après l’envoi des données générées à l’aide de [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).</span><span class="sxs-lookup"><span data-stu-id="83adc-113">Response received from a metering server, after sending data generated using [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).</span></span>

</dd> <dt>

<span data-ttu-id="83adc-114">*cbResponse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83adc-114">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83adc-115">Taille de *pbResponse*, en octets.</span><span class="sxs-lookup"><span data-stu-id="83adc-115">Size of *pbResponse*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="83adc-116">*pdwFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="83adc-116">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83adc-117">Un **DWORD** du tableau ci-dessous, indiquant s’il y a plus de données de contrôle sur l’appareil qui doivent être traitées.</span><span class="sxs-lookup"><span data-stu-id="83adc-117">A **DWORD** from the following table indicating whether there is more metering data on the device that needs to be processed.</span></span>



| <span data-ttu-id="83adc-118">Indicateur</span><span class="sxs-lookup"><span data-stu-id="83adc-118">Flag</span></span>                            | <span data-ttu-id="83adc-119">Description</span><span class="sxs-lookup"><span data-stu-id="83adc-119">Description</span></span>                                     |
|---------------------------------|-------------------------------------------------|
| <span data-ttu-id="83adc-120">\_réponse du compteur WMDRM \_ \_ All</span><span class="sxs-lookup"><span data-stu-id="83adc-120">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="83adc-121">Toutes les données de contrôle ont été traitées.</span><span class="sxs-lookup"><span data-stu-id="83adc-121">All metering data has been processed.</span></span>           |
| <span data-ttu-id="83adc-122">réponse de compteur de WMDRM \_ \_ \_ partielle</span><span class="sxs-lookup"><span data-stu-id="83adc-122">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="83adc-123">Des données de contrôle supplémentaires doivent être traitées.</span><span class="sxs-lookup"><span data-stu-id="83adc-123">Additional metering data needs to be processed.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83adc-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83adc-124">Return value</span></span>

<span data-ttu-id="83adc-125">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="83adc-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="83adc-126">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="83adc-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="83adc-127">Code de retour</span><span class="sxs-lookup"><span data-stu-id="83adc-127">Return code</span></span>                                                                                                      | <span data-ttu-id="83adc-128">Description</span><span class="sxs-lookup"><span data-stu-id="83adc-128">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83adc-129"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="83adc-129"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="83adc-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="83adc-130">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="83adc-131"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="83adc-131"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="83adc-132">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="83adc-132">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="83adc-133"><dt>**Erreurs de l’appareil**</dt></span><span class="sxs-lookup"><span data-stu-id="83adc-133"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="83adc-134">Un certain nombre d’erreurs d’appareil.</span><span class="sxs-lookup"><span data-stu-id="83adc-134">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="83adc-135"><dt>**Erreurs du client DRM**</dt></span><span class="sxs-lookup"><span data-stu-id="83adc-135"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="83adc-136">L’une des nombreuses erreurs internes du client DRM.</span><span class="sxs-lookup"><span data-stu-id="83adc-136">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="83adc-137"><dt>**appareil \_ NS \_ E \_ non \_ WMDRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="83adc-137"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="83adc-138">L’appareil spécifié n’est pas un périphérique compatible DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="83adc-138">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="83adc-139">Notes</span><span class="sxs-lookup"><span data-stu-id="83adc-139">Remarks</span></span>

<span data-ttu-id="83adc-140">Pour plus d’informations sur le contrôle, y compris des exemples de code, consultez le livre blanc [contrôle de l’utilisation du contenu multimédia numérique avec Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) sur le site Web MSDN.</span><span class="sxs-lookup"><span data-stu-id="83adc-140">More information on metering, including code examples, can be found in the whitepaper [Metering the Use of Digital Media Content with Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) on the MSDN Web site.</span></span>

## <a name="requirements"></a><span data-ttu-id="83adc-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83adc-141">Requirements</span></span>



| <span data-ttu-id="83adc-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83adc-142">Requirement</span></span> | <span data-ttu-id="83adc-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="83adc-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83adc-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="83adc-144">Header</span></span><br/>  | <dl> <span data-ttu-id="83adc-145"><dt>WMDRMDeviceApp. h (nécessite également Wmdrmdeviceapp \_ i. c, créé à partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="83adc-145"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="83adc-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="83adc-146">Library</span></span><br/> | <dl> <span data-ttu-id="83adc-147"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83adc-147"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="83adc-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83adc-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83adc-149">**Gestion du contenu protégé dans l’application**</span><span class="sxs-lookup"><span data-stu-id="83adc-149">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="83adc-150">**Interface IWMDMDevice**</span><span class="sxs-lookup"><span data-stu-id="83adc-150">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="83adc-151">**Interface IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="83adc-151">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

