---
title: IMsRdpClientAdvancedSettings6 propriété EnableCredSspSupport
description: Spécifie si le fournisseur de services de sécurité des informations d’identification (CredSSP) est activé pour cette connexion.
ms.assetid: 3BC8A265-7AEA-4C9C-9730-7710E1A3159D
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété EnableCredSspSupport
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings6.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings7.put_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.get_EnableCredSspSupport
- IMsRdpClientAdvancedSettings8.put_EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b73ad2b024cd0f8bbcafd6ba05be093c5953d54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508561"
---
# <a name="imsrdpclientadvancedsettings6enablecredsspsupport-property"></a><span data-ttu-id="6f4b8-110">IMsRdpClientAdvancedSettings6 :: EnableCredSspSupport, propriété</span><span class="sxs-lookup"><span data-stu-id="6f4b8-110">IMsRdpClientAdvancedSettings6::EnableCredSspSupport property</span></span>

<span data-ttu-id="6f4b8-111">Spécifie si le fournisseur de services de sécurité des informations d’identification (CredSSP) est activé pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-111">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="6f4b8-112">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f4b8-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f4b8-113">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="6f4b8-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6f4b8-114">Property value</span></span>

<span data-ttu-id="6f4b8-115">Spécifie si CredSSP est activé pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-115">Specifies whether CredSSP is enabled for this connection.</span></span> <span data-ttu-id="6f4b8-116">Affectez la valeur **Variant \_ true** pour activer CredSSP ou la **variante \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-116">Set to **VARIANT\_TRUE** to enable CredSSP or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f4b8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6f4b8-117">Remarks</span></span>

<span data-ttu-id="6f4b8-118">Cette propriété est uniquement prise en charge par les clients Connexion Bureau à distance 6,1 et 7,0.</span><span class="sxs-lookup"><span data-stu-id="6f4b8-118">This property is only supported by Remote Desktop Connection 6.1 and 7.0 clients.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f4b8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f4b8-119">Requirements</span></span>



| <span data-ttu-id="6f4b8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f4b8-120">Requirement</span></span> | <span data-ttu-id="6f4b8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f4b8-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4b8-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f4b8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6f4b8-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f4b8-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="6f4b8-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f4b8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6f4b8-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f4b8-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="6f4b8-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6f4b8-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f4b8-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f4b8-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="6f4b8-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6f4b8-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f4b8-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f4b8-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="6f4b8-130">IID</span><span class="sxs-lookup"><span data-stu-id="6f4b8-130">IID</span></span><br/>                      | <span data-ttu-id="6f4b8-131">IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="6f4b8-131">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6f4b8-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f4b8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f4b8-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6f4b8-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6f4b8-134">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6f4b8-134">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6f4b8-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6f4b8-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





