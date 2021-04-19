---
title: Méthode IWMDRMSecurity GetRevocationData (wmdrmsdk. h)
description: La méthode GetRevocationData récupère une liste de révocation de certificats à partir du magasin local.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- Méthode GetRevocationData format Windows Media
- Méthode GetRevocationData format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode GetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e9e0b428a3922f84141ef855d8468b79b3bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530423"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a><span data-ttu-id="16667-106">IWMDRMSecurity :: GetRevocationData, méthode</span><span class="sxs-lookup"><span data-stu-id="16667-106">IWMDRMSecurity::GetRevocationData method</span></span>

<span data-ttu-id="16667-107">La méthode **GetRevocationData** récupère une liste de révocation de certificats à partir du magasin local.</span><span class="sxs-lookup"><span data-stu-id="16667-107">The **GetRevocationData** method retrieves a certificate revocation list from the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="16667-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16667-108">Syntax</span></span>


```C++
HRESULT GetRevocationData(
  [in]      REFGUID f_guidRevocationType,
  [out]     BYTE    *f_pbCRL,
  [in, out] DWORD   *f_pcbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="16667-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16667-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16667-110">*f \_ guidRevocationType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="16667-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16667-111">GUID identifiant le type de liste de révocation à récupérer.</span><span class="sxs-lookup"><span data-stu-id="16667-111">GUID identifying the type of revocation list to retrieve.</span></span> <span data-ttu-id="16667-112">Utilisez l’une des constantes dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="16667-112">Use one of the constants in the following table.</span></span>



| <span data-ttu-id="16667-113">GUID, constante</span><span class="sxs-lookup"><span data-stu-id="16667-113">GUID constant</span></span>                 | <span data-ttu-id="16667-114">Description</span><span class="sxs-lookup"><span data-stu-id="16667-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="16667-115">\_application REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="16667-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="16667-116">Spécifie la liste de révocation des certificats d’application.</span><span class="sxs-lookup"><span data-stu-id="16667-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="16667-117">\_appareil REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="16667-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="16667-118">Spécifie la liste de révocation de certificats de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="16667-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="16667-119">\_REVOCATIONTYPE WMDRM \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="16667-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="16667-120">Spécifie la liste de révocation de certificats Windows Media DRM pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="16667-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="16667-121">*f \_ pbCRL* \[\]</span><span class="sxs-lookup"><span data-stu-id="16667-121">*f\_pbCRL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16667-122">Mémoire tampon qui reçoit la liste de révocation.</span><span class="sxs-lookup"><span data-stu-id="16667-122">Buffer that receives the revocation list.</span></span> <span data-ttu-id="16667-123">Affectez la valeur **null** pour connaître la taille de mémoire tampon requise.</span><span class="sxs-lookup"><span data-stu-id="16667-123">Set to **NULL** to get the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="16667-124">*f \_ pcbCRL* \[ dans, out\]</span><span class="sxs-lookup"><span data-stu-id="16667-124">*f\_pcbCRL* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="16667-125">Taille, en octets, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="16667-125">Size of the buffer in bytes.</span></span> <span data-ttu-id="16667-126">Si *f \_ pbCRL* a la valeur **null**, cette valeur est définie sur la taille de mémoire tampon requise sur la sortie.</span><span class="sxs-lookup"><span data-stu-id="16667-126">If *f\_pbCRL* is **NULL**, this value is set to the required buffer size on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16667-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16667-127">Return value</span></span>

<span data-ttu-id="16667-128">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="16667-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="16667-129">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="16667-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="16667-130">Code de retour</span><span class="sxs-lookup"><span data-stu-id="16667-130">Return code</span></span>                                                                          | <span data-ttu-id="16667-131">Description</span><span class="sxs-lookup"><span data-stu-id="16667-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="16667-132"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="16667-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="16667-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="16667-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="16667-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16667-134">Requirements</span></span>



| <span data-ttu-id="16667-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16667-135">Requirement</span></span> | <span data-ttu-id="16667-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="16667-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16667-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="16667-137">Header</span></span><br/>  | <dl> <span data-ttu-id="16667-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="16667-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="16667-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="16667-139">Library</span></span><br/> | <dl> <span data-ttu-id="16667-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16667-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16667-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16667-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16667-142">**Révocation et renouvellement de composants automatisés**</span><span class="sxs-lookup"><span data-stu-id="16667-142">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="16667-143">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="16667-143">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="16667-144">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="16667-144">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="16667-145">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="16667-145">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





