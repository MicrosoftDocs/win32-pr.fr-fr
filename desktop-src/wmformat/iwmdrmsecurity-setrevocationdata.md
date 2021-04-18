---
title: Méthode IWMDRMSecurity SetRevocationData (wmdrmsdk. h)
description: La méthode SetRevocationData définit une liste de révocation de certificats dans le magasin local.
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- Méthode SetRevocationData format Windows Media
- Méthode SetRevocationData format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode SetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.SetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3ece5a9285420261add123a61d0b7123896e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543163"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a><span data-ttu-id="e3094-106">IWMDRMSecurity :: SetRevocationData, méthode</span><span class="sxs-lookup"><span data-stu-id="e3094-106">IWMDRMSecurity::SetRevocationData method</span></span>

<span data-ttu-id="e3094-107">La méthode **SetRevocationData** définit une liste de révocation de certificats dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="e3094-107">The **SetRevocationData** method sets a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3094-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3094-108">Syntax</span></span>


```C++
HRESULT SetRevocationData(
  [in] REFGUID f_guidRevocationType,
  [in] BYTE    *f_pbCRL,
  [in] DWORD   f_cbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="e3094-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3094-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3094-110">*f \_ guidRevocationType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3094-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3094-111">GUID spécifiant le type de liste de révocation.</span><span class="sxs-lookup"><span data-stu-id="e3094-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="e3094-112">Définissez l’une des constantes dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e3094-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="e3094-113">GUID, constante</span><span class="sxs-lookup"><span data-stu-id="e3094-113">GUID constant</span></span>                 | <span data-ttu-id="e3094-114">Description</span><span class="sxs-lookup"><span data-stu-id="e3094-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e3094-115">\_application REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="e3094-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="e3094-116">Spécifie la liste de révocation des certificats d’application.</span><span class="sxs-lookup"><span data-stu-id="e3094-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="e3094-117">\_appareil REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="e3094-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="e3094-118">Spécifie la liste de révocation de certificats de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e3094-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="e3094-119">\_REVOCATIONTYPE WMDRM \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="e3094-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="e3094-120">Spécifie la liste de révocation de certificats Windows Media DRM pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="e3094-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e3094-121">*f \_ pbCRL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3094-121">*f\_pbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3094-122">Mémoire tampon contenant la liste de révocation de certificats.</span><span class="sxs-lookup"><span data-stu-id="e3094-122">Buffer containing the certificate revocation list.</span></span>

</dd> <dt>

<span data-ttu-id="e3094-123">*f \_ cbCRL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3094-123">*f\_cbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3094-124">Taille de la mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="e3094-124">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3094-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3094-125">Return value</span></span>

<span data-ttu-id="e3094-126">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e3094-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e3094-127">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e3094-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e3094-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e3094-128">Return code</span></span>                                                                          | <span data-ttu-id="e3094-129">Description</span><span class="sxs-lookup"><span data-stu-id="e3094-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e3094-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e3094-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e3094-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3094-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e3094-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3094-132">Requirements</span></span>



| <span data-ttu-id="e3094-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3094-133">Requirement</span></span> | <span data-ttu-id="e3094-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3094-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3094-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3094-135">Header</span></span><br/>  | <dl> <span data-ttu-id="e3094-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3094-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3094-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e3094-137">Library</span></span><br/> | <dl> <span data-ttu-id="e3094-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3094-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3094-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3094-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3094-140">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="e3094-140">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="e3094-141">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="e3094-141">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="e3094-142">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="e3094-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





