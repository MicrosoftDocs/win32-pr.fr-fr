---
description: La propriété de contexte retourne le contexte de ce produit.
ms.assetid: aa772a95-eb4e-45af-9788-9833d62139e8
title: Propriété Product. Context
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Context
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8334ca57d552681afeb77d0b213eca8b92bc1234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526774"
---
# <a name="productcontext-property"></a><span data-ttu-id="d55f8-103">Propriété Product. Context</span><span class="sxs-lookup"><span data-stu-id="d55f8-103">Product.Context property</span></span>

<span data-ttu-id="d55f8-104">La propriété de **contexte** retourne le contexte de ce produit.</span><span class="sxs-lookup"><span data-stu-id="d55f8-104">The **Context** property returns the context of this product.</span></span>

<span data-ttu-id="d55f8-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d55f8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d55f8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d55f8-106">Syntax</span></span>


```JScript
propVal = Product.Context
```



## <a name="property-value"></a><span data-ttu-id="d55f8-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d55f8-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="d55f8-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d55f8-108">Remarks</span></span>

<span data-ttu-id="d55f8-109">Cette propriété peut retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d55f8-109">This property can return one of the following values.</span></span>



| <span data-ttu-id="d55f8-110">Context</span><span class="sxs-lookup"><span data-stu-id="d55f8-110">Context</span></span>                        | <span data-ttu-id="d55f8-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="d55f8-111">Value</span></span> | <span data-ttu-id="d55f8-112">Signification</span><span class="sxs-lookup"><span data-stu-id="d55f8-112">Meaning</span></span>                           |
|--------------------------------|-------|-----------------------------------|
| <span data-ttu-id="d55f8-113">MSIINSTALLCONTEXT \_ USERMANAGED</span><span class="sxs-lookup"><span data-stu-id="d55f8-113">MSIINSTALLCONTEXT\_USERMANAGED</span></span> | <span data-ttu-id="d55f8-114">1</span><span class="sxs-lookup"><span data-stu-id="d55f8-114">1</span></span>     | <span data-ttu-id="d55f8-115">Produits sous un contexte géré.</span><span class="sxs-lookup"><span data-stu-id="d55f8-115">Products under managed context.</span></span>   |
| <span data-ttu-id="d55f8-116">\_utilisateur MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="d55f8-116">MSIINSTALLCONTEXT\_USER</span></span>        | <span data-ttu-id="d55f8-117">2</span><span class="sxs-lookup"><span data-stu-id="d55f8-117">2</span></span>     | <span data-ttu-id="d55f8-118">Produits sous un contexte non managé.</span><span class="sxs-lookup"><span data-stu-id="d55f8-118">Products under unmanaged context.</span></span> |
| <span data-ttu-id="d55f8-119">\_machine MSIINSTALLCONTEXT</span><span class="sxs-lookup"><span data-stu-id="d55f8-119">MSIINSTALLCONTEXT\_MACHINE</span></span>     | <span data-ttu-id="d55f8-120">4</span><span class="sxs-lookup"><span data-stu-id="d55f8-120">4</span></span>     | <span data-ttu-id="d55f8-121">Produits sous le contexte de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d55f8-121">Products under machine context.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="d55f8-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d55f8-122">Requirements</span></span>



| <span data-ttu-id="d55f8-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d55f8-123">Requirement</span></span> | <span data-ttu-id="d55f8-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d55f8-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d55f8-125">Version</span><span class="sxs-lookup"><span data-stu-id="d55f8-125">Version</span></span><br/> | <span data-ttu-id="d55f8-126">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d55f8-126">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d55f8-127">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d55f8-127">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d55f8-128">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d55f8-128">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="d55f8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d55f8-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="d55f8-130"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d55f8-130"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="d55f8-131">IID</span><span class="sxs-lookup"><span data-stu-id="d55f8-131">IID</span></span><br/>     | <span data-ttu-id="d55f8-132">IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d55f8-132">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="d55f8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d55f8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d55f8-134">**Production**</span><span class="sxs-lookup"><span data-stu-id="d55f8-134">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="d55f8-135">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="d55f8-135">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




