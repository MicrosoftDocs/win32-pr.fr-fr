---
description: La méthode SourceListClearSource supprime une source réseau ou URL. Accepte le type, le type de source et SourcePath, le chemin d’accès source, en tant que paramètres à supprimer. Cette méthode appelle MsiSourceListClearSource.
ms.assetid: a55676d4-795d-4ffe-8621-ef47c16a936c
title: Méthode Product. SourceListClearSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4988d0ba9003e087b6aeac58ae5587727067e01c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525395"
---
# <a name="productsourcelistclearsource-method"></a><span data-ttu-id="05198-105">Méthode Product. SourceListClearSource</span><span class="sxs-lookup"><span data-stu-id="05198-105">Product.SourceListClearSource method</span></span>

<span data-ttu-id="05198-106">La méthode **SourceListClearSource** supprime une source réseau ou URL.</span><span class="sxs-lookup"><span data-stu-id="05198-106">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="05198-107">Accepte le *type*, le type de source et *SourcePath*, le chemin d’accès source, en tant que paramètres à supprimer.</span><span class="sxs-lookup"><span data-stu-id="05198-107">Accepts *Type*, the source type, and *SourcePath*, the source path, as parameters to be removed.</span></span> <span data-ttu-id="05198-108">Cette méthode appelle [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span><span class="sxs-lookup"><span data-stu-id="05198-108">This method calls the [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="05198-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05198-109">Syntax</span></span>


```JScript
Product.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="05198-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05198-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05198-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="05198-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="05198-112">Type de source à supprimer : réseau MSISOURCETYPE \_ ou URL MSISOURCETYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="05198-112">Type of source to be removed: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="05198-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="05198-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="05198-114">Chemin d’accès à la source à supprimer.</span><span class="sxs-lookup"><span data-stu-id="05198-114">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05198-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05198-115">Return value</span></span>

<span data-ttu-id="05198-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="05198-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="05198-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05198-117">Requirements</span></span>



| <span data-ttu-id="05198-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05198-118">Requirement</span></span> | <span data-ttu-id="05198-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="05198-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05198-120">Version</span><span class="sxs-lookup"><span data-stu-id="05198-120">Version</span></span><br/> | <span data-ttu-id="05198-121">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="05198-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="05198-122">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="05198-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="05198-123">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="05198-123">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="05198-124">DLL</span><span class="sxs-lookup"><span data-stu-id="05198-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="05198-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05198-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="05198-126">IID</span><span class="sxs-lookup"><span data-stu-id="05198-126">IID</span></span><br/>     | <span data-ttu-id="05198-127">IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="05198-127">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="05198-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05198-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05198-129">**Production**</span><span class="sxs-lookup"><span data-stu-id="05198-129">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="05198-130">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="05198-130">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="05198-131">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="05198-131">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




