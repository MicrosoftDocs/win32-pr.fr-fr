---
title: Méthode IWMDRMDeviceApp QueryDeviceStatus (WMDRMDeviceApp. h)
description: La méthode QueryDeviceStatus interroge l’État et les fonctionnalités DRM actuelles sur un appareil.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Méthode QueryDeviceStatus Gestionnaire de périphériques Windows Media
- Méthode QueryDeviceStatus Gestionnaire de périphériques Windows Media, interface IWMDRMDeviceApp
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques, méthode QueryDeviceStatus
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.QueryDeviceStatus
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e0f4fad5ff9026ce70fc21712506eb4796d76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533056"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a><span data-ttu-id="e071b-106">IWMDRMDeviceApp :: QueryDeviceStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="e071b-106">IWMDRMDeviceApp::QueryDeviceStatus method</span></span>

<span data-ttu-id="e071b-107">La méthode **QueryDeviceStatus** interroge l’État et les fonctionnalités DRM actuelles sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="e071b-107">The **QueryDeviceStatus** method queries a device for its current DRM status and capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="e071b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e071b-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="e071b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e071b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e071b-110">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e071b-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e071b-111">Pointeur vers un objet [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="e071b-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="e071b-112">*pdwStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e071b-112">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e071b-113">Zéro, une ou plusieurs des valeurs **DWORD** suivantes décrivant les aspects DRM de l’appareil, combinés avec **une opération or** au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="e071b-113">Zero or more of the following **DWORD** values describing the DRM aspects of the device, combined with a bitwise **OR**.</span></span> <span data-ttu-id="e071b-114">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="e071b-114">See Remarks.</span></span>



| <span data-ttu-id="e071b-115">Statut</span><span class="sxs-lookup"><span data-stu-id="e071b-115">Status</span></span>                      | <span data-ttu-id="e071b-116">Description</span><span class="sxs-lookup"><span data-stu-id="e071b-116">Description</span></span>                                  |
|-----------------------------|----------------------------------------------|
| <span data-ttu-id="e071b-117">\_ISWMDRM d’appareil WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="e071b-117">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="e071b-118">L’appareil prend en charge Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="e071b-118">The device supports Windows Media DRM.</span></span>       |
| <span data-ttu-id="e071b-119">\_NEEDCLOCK d’appareil WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="e071b-119">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="e071b-120">L’appareil n’a pas d’horloge sécurisée.</span><span class="sxs-lookup"><span data-stu-id="e071b-120">The device does not have a secure clock.</span></span>     |
| <span data-ttu-id="e071b-121">\_appareil WMDRM \_ révoqué</span><span class="sxs-lookup"><span data-stu-id="e071b-121">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="e071b-122">L’appareil a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="e071b-122">The device has been revoked.</span></span>                 |
| <span data-ttu-id="e071b-123">\_NEEDINDIV du client WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="e071b-123">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="e071b-124">La sécurité DRM doit être individualisée.</span><span class="sxs-lookup"><span data-stu-id="e071b-124">The DRM security needs to be individualized.</span></span> |
| <span data-ttu-id="e071b-125">\_REFRESHCLOCK d’appareil WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="e071b-125">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="e071b-126">L’horloge doit être actualisée.</span><span class="sxs-lookup"><span data-stu-id="e071b-126">The clock needs to be refreshed.</span></span>             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e071b-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e071b-127">Return value</span></span>

<span data-ttu-id="e071b-128">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e071b-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e071b-129">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e071b-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e071b-130">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e071b-130">Return code</span></span>                                                                                                              | <span data-ttu-id="e071b-131">Description</span><span class="sxs-lookup"><span data-stu-id="e071b-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e071b-132"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e071b-132"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="e071b-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="e071b-133">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="e071b-134"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e071b-134"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="e071b-135">L’argument d’entrée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e071b-135">The input argument is not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="e071b-136"><dt>**\_ \_ \_ certificat non valide NS E DRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e071b-136"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="e071b-137">Le certificat d’appareil récupéré à partir de l’appareil n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e071b-137">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="e071b-138"><dt>**NS \_ E \_ DRM- \_ Impossible \_ d' \_ accéder au \_ \_ certificat de l’appareil**</dt></span><span class="sxs-lookup"><span data-stu-id="e071b-138"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="e071b-139">Impossible de récupérer le certificat de l’appareil à partir de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e071b-139">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="e071b-140">Notes</span><span class="sxs-lookup"><span data-stu-id="e071b-140">Remarks</span></span>

<span data-ttu-id="e071b-141">Cette méthode doit être appelée avant d’effectuer des actions restreintes sur du contenu DRM, telles que le transfert de contenu DRM sur l’appareil ou l’obtention d’informations de contrôle.</span><span class="sxs-lookup"><span data-stu-id="e071b-141">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="e071b-142">Si les valeurs récupérées par *pdwStatus* indiquent qu’une action doit être effectuée (par exemple, une individualisation pour le bureau ou l’acquisition d’une horloge pour l’appareil), l’application doit appeler [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) et transmettre la valeur *pdwStatus* Récupérée de cette fonction au paramètre *dwFlags* dans **AcquireDeviceData**.</span><span class="sxs-lookup"><span data-stu-id="e071b-142">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="e071b-143">Si la valeur zéro est retournée, l’appareil ne prend pas en charge Windows Media DRM 10 pour les appareils mobiles et aucune action n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e071b-143">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="e071b-144">Pour plus d’informations, consultez [gestion du contenu protégé dans l’application](handling-protected-content-in-the-application.md) .</span><span class="sxs-lookup"><span data-stu-id="e071b-144">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="e071b-145">Exemples</span><span class="sxs-lookup"><span data-stu-id="e071b-145">Examples</span></span>

<span data-ttu-id="e071b-146">L’exemple de code C++ suivant crée un objet **WMDRMDeviceApp** , vérifie que l’appareil est un appareil Windows Media DRM 10, que son horloge est exacte, puis demande les données de contrôle.</span><span class="sxs-lookup"><span data-stu-id="e071b-146">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


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
```



## <a name="requirements"></a><span data-ttu-id="e071b-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e071b-147">Requirements</span></span>



| <span data-ttu-id="e071b-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e071b-148">Requirement</span></span> | <span data-ttu-id="e071b-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="e071b-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e071b-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="e071b-150">Header</span></span><br/>  | <dl> <span data-ttu-id="e071b-151"><dt>WMDRMDeviceApp. h (nécessite également Wmdrmdeviceapp \_ i. c, créé à partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="e071b-151"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="e071b-152">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e071b-152">Library</span></span><br/> | <dl> <span data-ttu-id="e071b-153"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e071b-153"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="e071b-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e071b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e071b-155">**Gestion du contenu protégé dans l’application**</span><span class="sxs-lookup"><span data-stu-id="e071b-155">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="e071b-156">**Interface IWMDRMDeviceApp**</span><span class="sxs-lookup"><span data-stu-id="e071b-156">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="e071b-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="e071b-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





