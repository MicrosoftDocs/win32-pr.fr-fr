---
title: IMsRdpClientAdvancedSettings5 propriété BitmapVirtualCache32BppSize
description: Définit ou récupère la taille du fichier de cache virtuel pour les bitmaps de 32 bits par pixel (BPP).
ms.assetid: 7084293a-ae75-4711-a8d8-f813117333e7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété BitmapVirtualCache32BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache32BppSize, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété BitmapVirtualCache32BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache32BppSize, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété BitmapVirtualCache32BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache32BppSize, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété BitmapVirtualCache32BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache32BppSize, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété BitmapVirtualCache32BppSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache32BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache32BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d43de82b97e16fa36f83a5edde43712b2a9cbbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384299"
---
# <a name="imsrdpclientadvancedsettings5bitmapvirtualcache32bppsize-property"></a><span data-ttu-id="d117a-112">IMsRdpClientAdvancedSettings5 :: BitmapVirtualCache32BppSize, propriété</span><span class="sxs-lookup"><span data-stu-id="d117a-112">IMsRdpClientAdvancedSettings5::BitmapVirtualCache32BppSize property</span></span>

<span data-ttu-id="d117a-113">Définit ou récupère la taille du fichier de cache virtuel pour les bitmaps de 32 bits par pixel (BPP).</span><span class="sxs-lookup"><span data-stu-id="d117a-113">Sets or retrieves the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span>

<span data-ttu-id="d117a-114">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d117a-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d117a-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d117a-115">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache32BppSize(
  [in]  LONG bitmapVirtualCache32BppSize
);

HRESULT get_BitmapVirtualCache32BppSize(
  [out] LONG *pbitmapVirtualCache32BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="d117a-116">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d117a-116">Property value</span></span>

<span data-ttu-id="d117a-117">Définit la taille du fichier de cache virtuel pour les bitmaps 32 BPP, en mégaoctets (Mo).</span><span class="sxs-lookup"><span data-stu-id="d117a-117">Sets the size of the virtual cache file for 32 bpp bitmaps, in megabytes (MB).</span></span> <span data-ttu-id="d117a-118">La valeur maximale est de 48 Mo.</span><span class="sxs-lookup"><span data-stu-id="d117a-118">The maximum value is 48 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="d117a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d117a-119">Requirements</span></span>



| <span data-ttu-id="d117a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d117a-120">Requirement</span></span> | <span data-ttu-id="d117a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d117a-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d117a-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d117a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d117a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d117a-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="d117a-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d117a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d117a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d117a-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="d117a-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d117a-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="d117a-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d117a-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="d117a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d117a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d117a-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d117a-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="d117a-130">IID</span><span class="sxs-lookup"><span data-stu-id="d117a-130">IID</span></span><br/>                      | <span data-ttu-id="d117a-131">IID \_ IMsRdpClientAdvancedSettings5 est défini en tant que FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="d117a-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d117a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d117a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d117a-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d117a-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d117a-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d117a-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d117a-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d117a-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d117a-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d117a-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





