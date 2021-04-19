---
title: Méthode IWMDRMLicenseManagement MonitorLicenseAcquisition (wmdrmsdk. h)
description: La méthode MonitorLicenseAcquisition lance la surveillance d’un processus d’acquisition de licence.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- Méthode MonitorLicenseAcquisition format Windows Media
- Méthode MonitorLicenseAcquisition format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode MonitorLicenseAcquisition
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25171d36a9d360f7c8eb77211c580c4f7676618f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529649"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a><span data-ttu-id="7212a-106">IWMDRMLicenseManagement :: MonitorLicenseAcquisition, méthode</span><span class="sxs-lookup"><span data-stu-id="7212a-106">IWMDRMLicenseManagement::MonitorLicenseAcquisition method</span></span>

<span data-ttu-id="7212a-107">La méthode **MonitorLicenseAcquisition** lance la surveillance d’un processus d’acquisition de licence.</span><span class="sxs-lookup"><span data-stu-id="7212a-107">The **MonitorLicenseAcquisition** method initiates monitoring for a license acquisition process.</span></span>

## <a name="syntax"></a><span data-ttu-id="7212a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7212a-108">Syntax</span></span>


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="7212a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7212a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7212a-110">*bstrKID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7212a-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7212a-111">ID de clé (KID) de la licence acquise.</span><span class="sxs-lookup"><span data-stu-id="7212a-111">Key ID (KID) of the license being acquired.</span></span>

</dd> <dt>

<span data-ttu-id="7212a-112">*bstrHeader* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7212a-112">*bstrHeader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7212a-113">En-tête de contenu qui a été utilisé dans l’appel à la méthode [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .</span><span class="sxs-lookup"><span data-stu-id="7212a-113">Content header that was used in the call to the [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="7212a-114">*bstrActions* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7212a-114">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7212a-115">Chaîne contenant les actions demandées dans l’appel à la méthode **AcquireLicense** .</span><span class="sxs-lookup"><span data-stu-id="7212a-115">String containing the actions requested in the call to the **AcquireLicense** method.</span></span>

</dd> <dt>

<span data-ttu-id="7212a-116">*ppunkCancelationCookie* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7212a-116">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7212a-117">Pointeur qui reçoit un pointeur vers l’interface **IUnknown** d’un objet qui identifie cet appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7212a-117">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="7212a-118">Ce pointeur d’interface peut être utilisé pour annuler l’appel asynchrone en appelant la méthode [**IWMDRMEventGenerator :: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="7212a-118">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7212a-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7212a-119">Return value</span></span>

<span data-ttu-id="7212a-120">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7212a-120">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7212a-121">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7212a-121">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7212a-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7212a-122">Return code</span></span>                                                                          | <span data-ttu-id="7212a-123">Description</span><span class="sxs-lookup"><span data-stu-id="7212a-123">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7212a-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7212a-124"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7212a-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="7212a-125">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7212a-126">Notes</span><span class="sxs-lookup"><span data-stu-id="7212a-126">Remarks</span></span>

<span data-ttu-id="7212a-127">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7212a-127">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="7212a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7212a-128">Requirements</span></span>



| <span data-ttu-id="7212a-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7212a-129">Requirement</span></span> | <span data-ttu-id="7212a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="7212a-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7212a-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="7212a-131">Header</span></span><br/>  | <dl> <span data-ttu-id="7212a-132"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="7212a-132"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="7212a-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7212a-133">Library</span></span><br/> | <dl> <span data-ttu-id="7212a-134"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7212a-134"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7212a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7212a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7212a-136">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="7212a-136">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





