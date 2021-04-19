---
description: La propriété State retourne l’état d’installation de cette instance du produit.
ms.assetid: ae4c7a43-d4af-4e06-a3f8-d7c2d0715d84
title: Propriété Product. State
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 64d2f5d39a516fc4a0c00b8e18c159e1f2496e22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543860"
---
# <a name="productstate-property"></a><span data-ttu-id="1d126-103">Propriété Product. State</span><span class="sxs-lookup"><span data-stu-id="1d126-103">Product.State property</span></span>

<span data-ttu-id="1d126-104">La propriété **State** retourne l’état d’installation de cette instance du produit.</span><span class="sxs-lookup"><span data-stu-id="1d126-104">The **State** property returns the installation state of this instance of the product.</span></span>

<span data-ttu-id="1d126-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1d126-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d126-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d126-106">Syntax</span></span>


```JScript
propVal = Product.State
```



## <a name="property-value"></a><span data-ttu-id="1d126-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1d126-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="1d126-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1d126-108">Remarks</span></span>

<span data-ttu-id="1d126-109">Cette propriété retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1d126-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="1d126-110">État de l’installation</span><span class="sxs-lookup"><span data-stu-id="1d126-110">Installation State</span></span>       | <span data-ttu-id="1d126-111">Signification</span><span class="sxs-lookup"><span data-stu-id="1d126-111">Meaning</span></span>                                |
|--------------------------|----------------------------------------|
| <span data-ttu-id="1d126-112">INSTALLSTATE \_ par défaut</span><span class="sxs-lookup"><span data-stu-id="1d126-112">INSTALLSTATE\_DEFAULT</span></span>    | <span data-ttu-id="1d126-113">Instance du produit installée localement.</span><span class="sxs-lookup"><span data-stu-id="1d126-113">Instance of product installed locally.</span></span> |
| <span data-ttu-id="1d126-114">INSTALLSTATE \_ publié</span><span class="sxs-lookup"><span data-stu-id="1d126-114">INSTALLSTATE\_ADVERTISED</span></span> | <span data-ttu-id="1d126-115">Instance de produit publiée.</span><span class="sxs-lookup"><span data-stu-id="1d126-115">Instance of product advertised.</span></span>        |
| <span data-ttu-id="1d126-116">INSTALLSTATE \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="1d126-116">INSTALLSTATE\_UNKNOWN</span></span>    | <span data-ttu-id="1d126-117">Instance de produit inconnue.</span><span class="sxs-lookup"><span data-stu-id="1d126-117">Instance of product unknown.</span></span>           |



 

## <a name="requirements"></a><span data-ttu-id="1d126-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d126-118">Requirements</span></span>



| <span data-ttu-id="1d126-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d126-119">Requirement</span></span> | <span data-ttu-id="1d126-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d126-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d126-121">Version</span><span class="sxs-lookup"><span data-stu-id="1d126-121">Version</span></span><br/> | <span data-ttu-id="1d126-122">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1d126-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1d126-123">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1d126-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1d126-124">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="1d126-124">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="1d126-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1d126-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1d126-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d126-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="1d126-127">IID</span><span class="sxs-lookup"><span data-stu-id="1d126-127">IID</span></span><br/>     | <span data-ttu-id="1d126-128">IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1d126-128">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="1d126-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d126-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d126-130">**Production**</span><span class="sxs-lookup"><span data-stu-id="1d126-130">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="1d126-131">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="1d126-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




