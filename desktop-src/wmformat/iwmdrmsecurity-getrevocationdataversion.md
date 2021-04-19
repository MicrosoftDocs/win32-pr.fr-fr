---
title: Méthode IWMDRMSecurity GetRevocationDataVersion (wmdrmsdk. h)
description: La méthode GetRevocationDataVersion récupère le numéro de version d’une liste de révocation de certificats dans le magasin local.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- Méthode GetRevocationDataVersion format Windows Media
- Méthode GetRevocationDataVersion format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode GetRevocationDataVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationDataVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705f02622b7298134328b513aa038804995eb1c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523911"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a><span data-ttu-id="fa677-106">IWMDRMSecurity :: GetRevocationDataVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="fa677-106">IWMDRMSecurity::GetRevocationDataVersion method</span></span>

<span data-ttu-id="fa677-107">La méthode **GetRevocationDataVersion** récupère le numéro de version d’une liste de révocation de certificats dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="fa677-107">The **GetRevocationDataVersion** method retrieves the version number of a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa677-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa677-108">Syntax</span></span>


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
);
```



## <a name="parameters"></a><span data-ttu-id="fa677-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa677-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa677-110">*f \_ guidRevocationType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa677-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa677-111">GUID spécifiant le type de liste de révocation.</span><span class="sxs-lookup"><span data-stu-id="fa677-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="fa677-112">Définissez l’une des constantes dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fa677-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="fa677-113">GUID, constante</span><span class="sxs-lookup"><span data-stu-id="fa677-113">GUID constant</span></span>                 | <span data-ttu-id="fa677-114">Description</span><span class="sxs-lookup"><span data-stu-id="fa677-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fa677-115">\_application REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="fa677-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="fa677-116">Spécifie la liste de révocation des certificats d’application.</span><span class="sxs-lookup"><span data-stu-id="fa677-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="fa677-117">\_appareil REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="fa677-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="fa677-118">Spécifie la liste de révocation de certificats de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fa677-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="fa677-119">\_REVOCATIONTYPE WMDRM \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="fa677-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="fa677-120">Spécifie la liste de révocation de certificats Windows Media DRM pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="fa677-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="fa677-121">*f \_ pdwCRLVersion* \[\]</span><span class="sxs-lookup"><span data-stu-id="fa677-121">*f\_pdwCRLVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa677-122">Variable qui reçoit le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="fa677-122">Variable that receives the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa677-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa677-123">Return value</span></span>

<span data-ttu-id="fa677-124">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fa677-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fa677-125">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fa677-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fa677-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fa677-126">Return code</span></span>                                                                          | <span data-ttu-id="fa677-127">Description</span><span class="sxs-lookup"><span data-stu-id="fa677-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fa677-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa677-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fa677-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa677-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fa677-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa677-130">Requirements</span></span>



| <span data-ttu-id="fa677-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa677-131">Requirement</span></span> | <span data-ttu-id="fa677-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa677-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa677-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa677-133">Header</span></span><br/>  | <dl> <span data-ttu-id="fa677-134"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa677-134"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa677-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fa677-135">Library</span></span><br/> | <dl> <span data-ttu-id="fa677-136"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa677-136"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa677-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa677-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa677-138">**Révocation et renouvellement de composants automatisés**</span><span class="sxs-lookup"><span data-stu-id="fa677-138">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="fa677-139">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="fa677-139">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="fa677-140">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="fa677-140">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="fa677-141">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="fa677-141">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





