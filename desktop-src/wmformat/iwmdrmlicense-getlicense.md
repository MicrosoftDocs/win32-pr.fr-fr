---
title: Méthode IWMDRMLicense GetLicense (wmdrmsdk. h)
description: La méthode GetLicense récupère la licence sous forme de données XML ou XMR.
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- Méthode GetLicense format Windows Media
- Méthode GetLicense format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode GetLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0692afb2ff127f9456e6da3c7546c67ae22ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525493"
---
# <a name="iwmdrmlicensegetlicense-method"></a><span data-ttu-id="69012-106">IWMDRMLicense :: GetLicense, méthode</span><span class="sxs-lookup"><span data-stu-id="69012-106">IWMDRMLicense::GetLicense method</span></span>

<span data-ttu-id="69012-107">La méthode **GetLicense** récupère la licence sous forme de données XML ou XMR.</span><span class="sxs-lookup"><span data-stu-id="69012-107">The **GetLicense** method retrieves the license as XML or XMR data.</span></span>

## <a name="syntax"></a><span data-ttu-id="69012-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69012-108">Syntax</span></span>


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a><span data-ttu-id="69012-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69012-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69012-110">*ppbLicense* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="69012-110">*ppbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69012-111">Reçoit la licence.</span><span class="sxs-lookup"><span data-stu-id="69012-111">Receives the license.</span></span>

</dd> <dt>

<span data-ttu-id="69012-112">*pcbLicense* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="69012-112">*pcbLicense* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69012-113">Reçoit la taille de la licence.</span><span class="sxs-lookup"><span data-stu-id="69012-113">Receives the size of the license.</span></span>

</dd> <dt>

<span data-ttu-id="69012-114">*pdwLicenseType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="69012-114">*pdwLicenseType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69012-115">Reçoit le type de la licence retournée.</span><span class="sxs-lookup"><span data-stu-id="69012-115">Receives the type of the license returned.</span></span> <span data-ttu-id="69012-116">Cette valeur est définie sur l’une des constantes dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="69012-116">This value is set to one of the constants in the following table.</span></span>



| <span data-ttu-id="69012-117">Constante</span><span class="sxs-lookup"><span data-stu-id="69012-117">Constant</span></span>                  | <span data-ttu-id="69012-118">Description</span><span class="sxs-lookup"><span data-stu-id="69012-118">Description</span></span>                            |
|---------------------------|----------------------------------------|
| <span data-ttu-id="69012-119">\_type de licence WMDRM \_ \_ XML</span><span class="sxs-lookup"><span data-stu-id="69012-119">WMDRM\_LICENSE\_TYPE\_XML</span></span> | <span data-ttu-id="69012-120">La licence Récupérée est au format XML.</span><span class="sxs-lookup"><span data-stu-id="69012-120">Retrieved license is formatted as XML.</span></span> |
| <span data-ttu-id="69012-121">\_type de licence WMDRM \_ \_ XMR</span><span class="sxs-lookup"><span data-stu-id="69012-121">WMDRM\_LICENSE\_TYPE\_XMR</span></span> | <span data-ttu-id="69012-122">La licence Récupérée est au format XMR.</span><span class="sxs-lookup"><span data-stu-id="69012-122">Retrieved license is formatted as XMR.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69012-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69012-123">Return value</span></span>

<span data-ttu-id="69012-124">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="69012-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="69012-125">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="69012-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="69012-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="69012-126">Return code</span></span>                                                                          | <span data-ttu-id="69012-127">Description</span><span class="sxs-lookup"><span data-stu-id="69012-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="69012-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="69012-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="69012-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="69012-129">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="69012-130">Notes</span><span class="sxs-lookup"><span data-stu-id="69012-130">Remarks</span></span>

<span data-ttu-id="69012-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="69012-131">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="69012-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69012-132">Requirements</span></span>



| <span data-ttu-id="69012-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69012-133">Requirement</span></span> | <span data-ttu-id="69012-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="69012-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69012-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="69012-135">Header</span></span><br/>  | <dl> <span data-ttu-id="69012-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="69012-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="69012-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="69012-137">Library</span></span><br/> | <dl> <span data-ttu-id="69012-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69012-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69012-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69012-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69012-140">**GetLicenseProperty**</span><span class="sxs-lookup"><span data-stu-id="69012-140">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[<span data-ttu-id="69012-141">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="69012-141">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





