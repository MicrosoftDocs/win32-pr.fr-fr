---
description: La propriété sources énumère toutes les sources de l’instance de produit.
ms.assetid: 26602099-d0e0-4269-91d9-82943859811a
title: Propriété Product. sources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a82363f6a61ebb9c441dfcfeeeafe3760e63c462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533153"
---
# <a name="productsources-property"></a><span data-ttu-id="5d1fe-103">Propriété Product. sources</span><span class="sxs-lookup"><span data-stu-id="5d1fe-103">Product.Sources property</span></span>

<span data-ttu-id="5d1fe-104">La propriété **sources** énumère toutes les sources de l’instance de produit.</span><span class="sxs-lookup"><span data-stu-id="5d1fe-104">The **Sources** property enumerates all the sources for the product instance.</span></span> <span data-ttu-id="5d1fe-105">Cette propriété appelle [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) et retourne le tableau de chaînes et accepte le type de source comme argument.</span><span class="sxs-lookup"><span data-stu-id="5d1fe-105">This property calls [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) and returns the array of strings, and accepts the source type as argument.</span></span> <span data-ttu-id="5d1fe-106">Le type de source peut être MSISOURCETYPE \_ réseau ou MSISOURCETYPE \_ URL.</span><span class="sxs-lookup"><span data-stu-id="5d1fe-106">The source type can be MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

<span data-ttu-id="5d1fe-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5d1fe-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d1fe-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d1fe-108">Syntax</span></span>


```JScript
propVal = Product.Sources
```



## <a name="property-value"></a><span data-ttu-id="5d1fe-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5d1fe-109">Property value</span></span>

<span data-ttu-id="5d1fe-110">Type de source à énumérer.</span><span class="sxs-lookup"><span data-stu-id="5d1fe-110">The type of source to enumerate.</span></span> <span data-ttu-id="5d1fe-111">La valeur peut être *msiInstallSourceTypeNetwork* (1) ou *msiInstallSourceTypeURL* (2).</span><span class="sxs-lookup"><span data-stu-id="5d1fe-111">The value can be *msiInstallSourceTypeNetwork* (1) or *msiInstallSourceTypeURL* (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d1fe-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d1fe-112">Requirements</span></span>



| <span data-ttu-id="5d1fe-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d1fe-113">Requirement</span></span> | <span data-ttu-id="5d1fe-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d1fe-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d1fe-115">Version</span><span class="sxs-lookup"><span data-stu-id="5d1fe-115">Version</span></span><br/> | <span data-ttu-id="5d1fe-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5d1fe-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5d1fe-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5d1fe-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5d1fe-118">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5d1fe-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="5d1fe-119">DLL</span><span class="sxs-lookup"><span data-stu-id="5d1fe-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="5d1fe-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d1fe-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="5d1fe-121">IID</span><span class="sxs-lookup"><span data-stu-id="5d1fe-121">IID</span></span><br/>     | <span data-ttu-id="5d1fe-122">IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5d1fe-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="5d1fe-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d1fe-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d1fe-124">**Production**</span><span class="sxs-lookup"><span data-stu-id="5d1fe-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="5d1fe-125">**MsiSourceListEnumSources**</span><span class="sxs-lookup"><span data-stu-id="5d1fe-125">**MsiSourceListEnumSources**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[<span data-ttu-id="5d1fe-126">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="5d1fe-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




