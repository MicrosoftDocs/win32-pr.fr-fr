---
description: Retourne un objet RecordList qui énumère la liste des produits.
ms.assetid: 30735b9f-091b-4915-9b07-9688c9be2d26
title: Installer. ProductsEx, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17d5e8290ab61b85fa8269f8b23f3cdabd30e012
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520974"
---
# <a name="installerproductsex-property"></a><span data-ttu-id="17d9a-103">Installer. ProductsEx, propriété</span><span class="sxs-lookup"><span data-stu-id="17d9a-103">Installer.ProductsEx property</span></span>

<span data-ttu-id="17d9a-104">La propriété **ProductsEx** retourne un objet [**RecordList**](recordlist-object.md) qui énumère la liste des produits.</span><span class="sxs-lookup"><span data-stu-id="17d9a-104">The **ProductsEx** property returns a [**RecordList**](recordlist-object.md) object that enumerates the list of products.</span></span> <span data-ttu-id="17d9a-105">Cette propriété appelle [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa).</span><span class="sxs-lookup"><span data-stu-id="17d9a-105">This property calls [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa).</span></span>

<span data-ttu-id="17d9a-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="17d9a-106">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d9a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17d9a-107">Syntax</span></span>


```JScript
propVal = Installer.ProductsEx
```



## <a name="property-value"></a><span data-ttu-id="17d9a-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="17d9a-108">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="17d9a-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17d9a-109">Requirements</span></span>



| <span data-ttu-id="17d9a-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17d9a-110">Requirement</span></span> | <span data-ttu-id="17d9a-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="17d9a-111">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17d9a-112">Version</span><span class="sxs-lookup"><span data-stu-id="17d9a-112">Version</span></span><br/> | <span data-ttu-id="17d9a-113">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="17d9a-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="17d9a-114">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="17d9a-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="17d9a-115">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="17d9a-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="17d9a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="17d9a-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="17d9a-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17d9a-117"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="17d9a-118">IID</span><span class="sxs-lookup"><span data-stu-id="17d9a-118">IID</span></span><br/>     | <span data-ttu-id="17d9a-119">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="17d9a-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="17d9a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17d9a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d9a-121">**Programme d’installation**</span><span class="sxs-lookup"><span data-stu-id="17d9a-121">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="17d9a-122">**MsiEnumProductsEx**</span><span class="sxs-lookup"><span data-stu-id="17d9a-122">**MsiEnumProductsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="17d9a-123">**Produit**</span><span class="sxs-lookup"><span data-stu-id="17d9a-123">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="17d9a-124">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="17d9a-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




