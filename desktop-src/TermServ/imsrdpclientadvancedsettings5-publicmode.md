---
title: IMsRdpClientAdvancedSettings5 propriété PublicMode
description: Définit ou récupère la configuration pour le mode public. Le mode public empêche le client de mettre en cache les données utilisateur sur le système local.
ms.assetid: dff6121a-b69c-411f-832b-29f9609f4230
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PublicMode
- Services Bureau à distance de la propriété PublicMode, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété PublicMode
- Services Bureau à distance de la propriété PublicMode, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété PublicMode
- Services Bureau à distance de la propriété PublicMode, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété PublicMode
- Services Bureau à distance de la propriété PublicMode, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété PublicMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.PublicMode
- IMsRdpClientAdvancedSettings5.get_PublicMode
- IMsRdpClientAdvancedSettings5.put_PublicMode
- IMsRdpClientAdvancedSettings6.PublicMode
- IMsRdpClientAdvancedSettings6.get_PublicMode
- IMsRdpClientAdvancedSettings6.put_PublicMode
- IMsRdpClientAdvancedSettings7.PublicMode
- IMsRdpClientAdvancedSettings7.get_PublicMode
- IMsRdpClientAdvancedSettings7.put_PublicMode
- IMsRdpClientAdvancedSettings8.PublicMode
- IMsRdpClientAdvancedSettings8.get_PublicMode
- IMsRdpClientAdvancedSettings8.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9173b7685e77984a28d65129c79c9d1a09cf1458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511134"
---
# <a name="imsrdpclientadvancedsettings5publicmode-property"></a><span data-ttu-id="19b93-113">IMsRdpClientAdvancedSettings5 ::P propriété ublicMode</span><span class="sxs-lookup"><span data-stu-id="19b93-113">IMsRdpClientAdvancedSettings5::PublicMode property</span></span>

<span data-ttu-id="19b93-114">Définit ou récupère la configuration pour le mode public.</span><span class="sxs-lookup"><span data-stu-id="19b93-114">Sets or retrieves the configuration for public mode.</span></span> <span data-ttu-id="19b93-115">Le mode public empêche le client de mettre en cache les données utilisateur sur le système local.</span><span class="sxs-lookup"><span data-stu-id="19b93-115">Public mode prevents the client from caching user data to the local system.</span></span>

<span data-ttu-id="19b93-116">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="19b93-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="19b93-117">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19b93-117">Syntax</span></span>


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a><span data-ttu-id="19b93-118">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="19b93-118">Property value</span></span>

<span data-ttu-id="19b93-119">Définit le paramètre de mode public sur **Variant \_ true** ou **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="19b93-119">Sets the public mode setting to **VARIANT\_TRUE** or **VARIANT\_FALSE**.</span></span> <span data-ttu-id="19b93-120">Si la valeur **est \_ true**, le paramètre de mode public est activé.</span><span class="sxs-lookup"><span data-stu-id="19b93-120">If set to **VARIANT\_TRUE**, the public mode setting is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="19b93-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19b93-121">Requirements</span></span>



| <span data-ttu-id="19b93-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19b93-122">Requirement</span></span> | <span data-ttu-id="19b93-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="19b93-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19b93-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19b93-124">Minimum supported client</span></span><br/> | <span data-ttu-id="19b93-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19b93-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="19b93-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19b93-126">Minimum supported server</span></span><br/> | <span data-ttu-id="19b93-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19b93-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="19b93-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="19b93-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="19b93-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19b93-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="19b93-130">DLL</span><span class="sxs-lookup"><span data-stu-id="19b93-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19b93-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19b93-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="19b93-132">IID</span><span class="sxs-lookup"><span data-stu-id="19b93-132">IID</span></span><br/>                      | <span data-ttu-id="19b93-133">IID \_ IMsRdpClientAdvancedSettings5 est défini en tant que FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="19b93-133">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19b93-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19b93-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19b93-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="19b93-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="19b93-136">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="19b93-136">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="19b93-137">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="19b93-137">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="19b93-138">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="19b93-138">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





