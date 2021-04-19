---
title: Méthode IWMDRMDeviceApp2 QueryDeviceStatus2 (WMDRMDeviceApp. h)
description: La méthode QueryDeviceStatus2 interroge un appareil pour obtenir un État ou une fonctionnalité DRM spécifique.
ms.assetid: f7e95fb7-5929-4a70-8580-a443e152e6d1
keywords:
- Méthode QueryDeviceStatus2 Gestionnaire de périphériques Windows Media
- Méthode QueryDeviceStatus2 Gestionnaire de périphériques Windows Media, interface IWMDRMDeviceApp2
- Interface IWMDRMDeviceApp2 Windows Media Gestionnaire de périphériques, méthode QueryDeviceStatus2
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2.QueryDeviceStatus2
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d1f03f8d1e63086bb260c9854c7dcf3e88514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520980"
---
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a><span data-ttu-id="c96d5-106">IWMDRMDeviceApp2 :: QueryDeviceStatus2, méthode</span><span class="sxs-lookup"><span data-stu-id="c96d5-106">IWMDRMDeviceApp2::QueryDeviceStatus2 method</span></span>

<span data-ttu-id="c96d5-107">La méthode **QueryDeviceStatus2** interroge un appareil pour obtenir un État ou une fonctionnalité DRM spécifique.</span><span class="sxs-lookup"><span data-stu-id="c96d5-107">The **QueryDeviceStatus2** method queries a device for a specific DRM status or capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="c96d5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c96d5-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus2(
  [in]  IWMDMDevice *pDevice,
  [in]  DWORD       dwFlags,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="c96d5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c96d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c96d5-110">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c96d5-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c96d5-111">Pointeur vers un objet [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="c96d5-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="c96d5-112">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c96d5-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c96d5-113">Une ou plusieurs des valeurs **DWORD** suivantes spécifiant les fonctionnalités à demander, combinées avec une **opération or** au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="c96d5-113">One or more of the following **DWORD** values specifying which capabilities to request, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="c96d5-114">Indicateur</span><span class="sxs-lookup"><span data-stu-id="c96d5-114">Flag</span></span>                              | <span data-ttu-id="c96d5-115">Description</span><span class="sxs-lookup"><span data-stu-id="c96d5-115">Description</span></span>                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c96d5-116">\_INDIVSTATUS du \_ client de requête WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="c96d5-116">WMDRM\_QUERY\_CLIENT\_INDIVSTATUS</span></span> | <span data-ttu-id="c96d5-117">Demander si les composants DRM de l’ordinateur doivent être individualisés.</span><span class="sxs-lookup"><span data-stu-id="c96d5-117">Query whether the computer's DRM components need to be individualized.</span></span>       |
| <span data-ttu-id="c96d5-118">CLOCKSTATUS de l' \_ appareil de requête WMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="c96d5-118">WMDRM\_QUERY\_DEVICE\_CLOCKSTATUS</span></span> | <span data-ttu-id="c96d5-119">Demander si l’horloge sécurisée de l’appareil doit être ajoutée ou mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c96d5-119">Query whether the device's secure clock needs to be added or updated.</span></span>        |
| <span data-ttu-id="c96d5-120">ISREVOKED de l' \_ appareil de requête WMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="c96d5-120">WMDRM\_QUERY\_DEVICE\_ISREVOKED</span></span>   | <span data-ttu-id="c96d5-121">Demander si l’appareil est révoqué.</span><span class="sxs-lookup"><span data-stu-id="c96d5-121">Query whether the device is revoked.</span></span>                                         |
| <span data-ttu-id="c96d5-122">ISWMDRM de l' \_ appareil de requête WMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="c96d5-122">WMDRM\_QUERY\_DEVICE\_ISWMDRM</span></span>     | <span data-ttu-id="c96d5-123">Demander si l’appareil prend en charge Windows Media DRM 10 pour les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="c96d5-123">Query whether the device supports Windows Media DRM 10 for Portable Devices.</span></span> |



 

</dd> <dt>

<span data-ttu-id="c96d5-124">*pdwStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c96d5-124">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c96d5-125">Zéro, une ou plusieurs des valeurs **DWORD** suivantes spécifiant l’état de l’appareil demandé, combiné avec **une opération or** au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="c96d5-125">Zero or more of the following **DWORD** values specifying the requested device status, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="c96d5-126">Statut</span><span class="sxs-lookup"><span data-stu-id="c96d5-126">Status</span></span>                      | <span data-ttu-id="c96d5-127">Description</span><span class="sxs-lookup"><span data-stu-id="c96d5-127">Description</span></span>                                              |
|-----------------------------|----------------------------------------------------------|
| <span data-ttu-id="c96d5-128">\_ISWMDRM d’appareil WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="c96d5-128">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="c96d5-129">L’appareil prend en charge Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="c96d5-129">The device supports Windows Media DRM.</span></span>                   |
| <span data-ttu-id="c96d5-130">\_NEEDCLOCK d’appareil WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="c96d5-130">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="c96d5-131">L’appareil n’a pas d’horloge sécurisée.</span><span class="sxs-lookup"><span data-stu-id="c96d5-131">The device does not have a secure clock.</span></span>                 |
| <span data-ttu-id="c96d5-132">\_appareil WMDRM \_ révoqué</span><span class="sxs-lookup"><span data-stu-id="c96d5-132">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="c96d5-133">L’appareil a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="c96d5-133">The device has been revoked.</span></span>                             |
| <span data-ttu-id="c96d5-134">\_NEEDINDIV du client WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="c96d5-134">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="c96d5-135">Les composants DRM de l’ordinateur doivent être individualisés.</span><span class="sxs-lookup"><span data-stu-id="c96d5-135">The computer's DRM components need to be individualized.</span></span> |
| <span data-ttu-id="c96d5-136">\_REFRESHCLOCK d’appareil WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="c96d5-136">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="c96d5-137">L’horloge doit être actualisée.</span><span class="sxs-lookup"><span data-stu-id="c96d5-137">The clock needs to be refreshed.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c96d5-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c96d5-138">Return value</span></span>

<span data-ttu-id="c96d5-139">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c96d5-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c96d5-140">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c96d5-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c96d5-141">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c96d5-141">Return code</span></span>                                                                                                              | <span data-ttu-id="c96d5-142">Description</span><span class="sxs-lookup"><span data-stu-id="c96d5-142">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c96d5-143"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c96d5-143"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="c96d5-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="c96d5-144">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="c96d5-145"><dt>**DRM \_ E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c96d5-145"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="c96d5-146">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="c96d5-146">One or more arguments are not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="c96d5-147"><dt>**\_ \_ \_ certificat non valide NS E DRM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c96d5-147"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="c96d5-148">Le certificat d’appareil récupéré à partir de l’appareil n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c96d5-148">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="c96d5-149"><dt>**NS \_ E \_ DRM- \_ Impossible \_ d' \_ accéder au \_ \_ certificat de l’appareil**</dt></span><span class="sxs-lookup"><span data-stu-id="c96d5-149"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="c96d5-150">Impossible de récupérer le certificat de l’appareil à partir de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c96d5-150">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="c96d5-151">Notes</span><span class="sxs-lookup"><span data-stu-id="c96d5-151">Remarks</span></span>

<span data-ttu-id="c96d5-152">Cette méthode doit être appelée avant d’effectuer des actions restreintes sur du contenu DRM, telles que le transfert de contenu DRM sur l’appareil ou l’obtention d’informations de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c96d5-152">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="c96d5-153">Si les valeurs récupérées par *pdwStatus* indiquent qu’une action doit être exécutée (par exemple, une individualisation pour le bureau ou l’acquisition d’une horloge pour l’appareil), l’application doit appeler [**IWMDRMDeviceApp :: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) et transmettre la valeur *pdwStatus* Récupérée de cette fonction au paramètre *dwFlags* dans **AcquireDeviceData**.</span><span class="sxs-lookup"><span data-stu-id="c96d5-153">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass in the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="c96d5-154">Si la valeur zéro est retournée, l’appareil ne prend pas en charge Windows Media DRM 10 pour les appareils mobiles et aucune action n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c96d5-154">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="c96d5-155">Pour plus d’informations, consultez [gestion du contenu protégé dans l’application](handling-protected-content-in-the-application.md) .</span><span class="sxs-lookup"><span data-stu-id="c96d5-155">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c96d5-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c96d5-156">Requirements</span></span>



| <span data-ttu-id="c96d5-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c96d5-157">Requirement</span></span> | <span data-ttu-id="c96d5-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="c96d5-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c96d5-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="c96d5-159">Header</span></span><br/>  | <dl> <span data-ttu-id="c96d5-160"><dt>WMDRMDeviceApp. h (nécessite également Wmdrmdeviceapp \_ i. c, créé à partir de WMDRMDeviceApp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="c96d5-160"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="c96d5-161">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c96d5-161">Library</span></span><br/> | <dl> <span data-ttu-id="c96d5-162"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c96d5-162"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="c96d5-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c96d5-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c96d5-164">**Gestion du contenu protégé dans l’application**</span><span class="sxs-lookup"><span data-stu-id="c96d5-164">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="c96d5-165">**IWMDRMDeviceApp::QueryDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="c96d5-165">**IWMDRMDeviceApp::QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[<span data-ttu-id="c96d5-166">**Interface IWMDRMDeviceApp2**</span><span class="sxs-lookup"><span data-stu-id="c96d5-166">**IWMDRMDeviceApp2 Interface**</span></span>](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 





