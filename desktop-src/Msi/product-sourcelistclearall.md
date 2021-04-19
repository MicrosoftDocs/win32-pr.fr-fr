---
description: La méthode SourceListClearAll l’objet Product supprime toutes les sources du produit. Le type de source à supprimer peut être spécifié.
ms.assetid: c8a63b54-7be6-424a-8653-0182b561faab
title: Méthode Product. SourceListClearAll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4c921bd45b1acbac40444e4d11bb67d589149c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545391"
---
# <a name="productsourcelistclearall-method"></a><span data-ttu-id="f29bc-104">Méthode Product. SourceListClearAll</span><span class="sxs-lookup"><span data-stu-id="f29bc-104">Product.SourceListClearAll method</span></span>

<span data-ttu-id="f29bc-105">La méthode **SourceListClearAll** l’objet [**Product**](product-object.md) supprime toutes les sources du produit.</span><span class="sxs-lookup"><span data-stu-id="f29bc-105">The **SourceListClearAll** method the [**Product**](product-object.md) object removes all sources for the product.</span></span> <span data-ttu-id="f29bc-106">Le type de source à supprimer peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="f29bc-106">The type of source to remove can be specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="f29bc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f29bc-107">Syntax</span></span>


```JScript
Product.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="f29bc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f29bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f29bc-109">*Type*</span><span class="sxs-lookup"><span data-stu-id="f29bc-109">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="f29bc-110">Type de source à supprimer : MSISOURCETYPE \_ Media, MSISOURCETYPE \_ Network ou MSISOURCETYPE \_ URL.</span><span class="sxs-lookup"><span data-stu-id="f29bc-110">Type of source to be removed: MSISOURCETYPE\_MEDIA, MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f29bc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f29bc-111">Return value</span></span>

<span data-ttu-id="f29bc-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f29bc-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f29bc-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f29bc-113">Requirements</span></span>



| <span data-ttu-id="f29bc-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f29bc-114">Requirement</span></span> | <span data-ttu-id="f29bc-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f29bc-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f29bc-116">Version</span><span class="sxs-lookup"><span data-stu-id="f29bc-116">Version</span></span><br/> | <span data-ttu-id="f29bc-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f29bc-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f29bc-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f29bc-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f29bc-119">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f29bc-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="f29bc-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f29bc-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="f29bc-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f29bc-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="f29bc-122">IID</span><span class="sxs-lookup"><span data-stu-id="f29bc-122">IID</span></span><br/>     | <span data-ttu-id="f29bc-123">IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f29bc-123">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="f29bc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f29bc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f29bc-125">**Production**</span><span class="sxs-lookup"><span data-stu-id="f29bc-125">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="f29bc-126">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="f29bc-126">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="f29bc-127">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="f29bc-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




