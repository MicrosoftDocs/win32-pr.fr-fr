---
title: Méthode IWMDRMLicenseManagement CreateLicenseEnumeration (wmdrmsdk. h)
description: La méthode CreateLicenseEnumeration crée un objet énumérateur de licence avec lequel vous pouvez obtenir des informations sur les licences dans le magasin de licences local.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- Méthode CreateLicenseEnumeration format Windows Media
- Méthode CreateLicenseEnumeration format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode CreateLicenseEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb75d21cc640da39c3679ac118ead629b24f719
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523897"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a><span data-ttu-id="cd4e6-106">IWMDRMLicenseManagement :: CreateLicenseEnumeration, méthode</span><span class="sxs-lookup"><span data-stu-id="cd4e6-106">IWMDRMLicenseManagement::CreateLicenseEnumeration method</span></span>

<span data-ttu-id="cd4e6-107">La méthode **CreateLicenseEnumeration** crée un objet énumérateur de licence avec lequel vous pouvez obtenir des informations sur les licences dans le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="cd4e6-107">The **CreateLicenseEnumeration** method creates a license enumerator object with which you can get information about licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd4e6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd4e6-108">Syntax</span></span>


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="cd4e6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd4e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd4e6-110">*pLicenseFilter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd4e6-110">*pLicenseFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd4e6-111">Pointeur vers une structure de [**\_ \_ filtre de licence WMDRM**](wmdrm-license-filter.md) contenant les paramètres de filtrage pour la liste de licences dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="cd4e6-111">Pointer to a [**WMDRM\_LICENSE\_FILTER**](wmdrm-license-filter.md) structure containing the filtering parameters for the list of licenses in the enumerator.</span></span>

</dd> <dt>

<span data-ttu-id="cd4e6-112">*pEnumerator* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd4e6-112">*pEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd4e6-113">Pointeur qui reçoit l’adresse de l’interface [**IWMDRMLicense**](iwmdrmlicense.md) de l’objet énumérateur de licence nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="cd4e6-113">Pointer that receives the address of the [**IWMDRMLicense**](iwmdrmlicense.md) interface of the newly created license enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd4e6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd4e6-114">Return value</span></span>

<span data-ttu-id="cd4e6-115">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cd4e6-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cd4e6-116">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cd4e6-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cd4e6-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cd4e6-117">Return code</span></span>                                                                                                | <span data-ttu-id="cd4e6-118">Description</span><span class="sxs-lookup"><span data-stu-id="cd4e6-118">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="cd4e6-119"><dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt></span><span class="sxs-lookup"><span data-stu-id="cd4e6-119"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="cd4e6-120">Une liste de révocation de contenu mise à jour est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="cd4e6-120">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="cd4e6-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cd4e6-121"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="cd4e6-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd4e6-122">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="cd4e6-123">Notes</span><span class="sxs-lookup"><span data-stu-id="cd4e6-123">Remarks</span></span>

<span data-ttu-id="cd4e6-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cd4e6-124">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd4e6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd4e6-125">Requirements</span></span>



| <span data-ttu-id="cd4e6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd4e6-126">Requirement</span></span> | <span data-ttu-id="cd4e6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd4e6-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd4e6-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd4e6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="cd4e6-129"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd4e6-129"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd4e6-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cd4e6-130">Library</span></span><br/> | <dl> <span data-ttu-id="cd4e6-131"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd4e6-131"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd4e6-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd4e6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd4e6-133">**Énumération des licences dans le magasin de licences local**</span><span class="sxs-lookup"><span data-stu-id="cd4e6-133">**Enumerating Licenses in the Local License Store**</span></span>](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[<span data-ttu-id="cd4e6-134">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="cd4e6-134">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





