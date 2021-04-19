---
description: La méthode SourceListForceResolution efface la propriété LastUsedSource.
ms.assetid: 554bc321-51d8-4595-b79c-7975bad8c555
title: Méthode Product. SourceListForceResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 668a74d2327dad918f1f2389bc163dcfde198c2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540577"
---
# <a name="productsourcelistforceresolution-method"></a><span data-ttu-id="410d4-103">Méthode Product. SourceListForceResolution</span><span class="sxs-lookup"><span data-stu-id="410d4-103">Product.SourceListForceResolution method</span></span>

<span data-ttu-id="410d4-104">La méthode **SourceListForceResolution** efface la propriété LastUsedSource.</span><span class="sxs-lookup"><span data-stu-id="410d4-104">The **SourceListForceResolution** method clears the LastUsedSource property.</span></span> <span data-ttu-id="410d4-105">Cela oblige le programme d’installation à rechercher dans la liste source une source de produit valide la prochaine fois qu’une source est requise, par exemple quand le programme d’installation effectue une installation ou une réinstallation, ou lorsque le chemin d’accès est requis pour qu’un composant soit exécuté à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="410d4-105">This forces the installer to search the source list for a valid product source the next time a source is required, such as when the installer performs an installation or a reinstallation, or when the path is required for a component set to run from the source.</span></span>

<span data-ttu-id="410d4-106">Cette méthode appelle [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span><span class="sxs-lookup"><span data-stu-id="410d4-106">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="410d4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="410d4-107">Syntax</span></span>


```JScript
Product.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="410d4-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="410d4-108">Parameters</span></span>

<span data-ttu-id="410d4-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="410d4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="410d4-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="410d4-110">Return value</span></span>

<span data-ttu-id="410d4-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="410d4-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="410d4-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="410d4-112">Requirements</span></span>



| <span data-ttu-id="410d4-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="410d4-113">Requirement</span></span> | <span data-ttu-id="410d4-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="410d4-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="410d4-115">Version</span><span class="sxs-lookup"><span data-stu-id="410d4-115">Version</span></span><br/> | <span data-ttu-id="410d4-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="410d4-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="410d4-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="410d4-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="410d4-118">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="410d4-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="410d4-119">DLL</span><span class="sxs-lookup"><span data-stu-id="410d4-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="410d4-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="410d4-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="410d4-121">IID</span><span class="sxs-lookup"><span data-stu-id="410d4-121">IID</span></span><br/>     | <span data-ttu-id="410d4-122">IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="410d4-122">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="410d4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="410d4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="410d4-124">**Production**</span><span class="sxs-lookup"><span data-stu-id="410d4-124">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="410d4-125">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="410d4-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="410d4-126">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="410d4-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




