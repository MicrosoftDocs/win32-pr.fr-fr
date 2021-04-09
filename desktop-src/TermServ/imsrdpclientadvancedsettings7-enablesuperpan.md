---
title: IMsRdpClientAdvancedSettings7 propriété EnableSuperPan
description: Spécifie ou récupère une valeur booléenne qui indique si SuperPan est activé ou désactivé.
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété EnableSuperPan
- Services Bureau à distance de la propriété EnableSuperPan, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété EnableSuperPan
- Services Bureau à distance de la propriété EnableSuperPan, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété EnableSuperPan
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.EnableSuperPan
- IMsRdpClientAdvancedSettings7.get_EnableSuperPan
- IMsRdpClientAdvancedSettings7.put_EnableSuperPan
- IMsRdpClientAdvancedSettings8.EnableSuperPan
- IMsRdpClientAdvancedSettings8.get_EnableSuperPan
- IMsRdpClientAdvancedSettings8.put_EnableSuperPan
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21ac0664b99dc0533d3e26840445ef22c8c08385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742133"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a><span data-ttu-id="887f8-108">IMsRdpClientAdvancedSettings7 :: EnableSuperPan, propriété</span><span class="sxs-lookup"><span data-stu-id="887f8-108">IMsRdpClientAdvancedSettings7::EnableSuperPan property</span></span>

<span data-ttu-id="887f8-109">Spécifie ou récupère une valeur booléenne qui indique si SuperPan est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="887f8-109">Specifies or retrieves a Boolean value that indicates whether SuperPan is enabled or disabled.</span></span> <span data-ttu-id="887f8-110">SuperPan est une fonctionnalité qui permet à un utilisateur de naviguer facilement dans un bureau à distance en mode plein écran, lorsque les dimensions du Bureau à distance sont supérieures à celles de la fenêtre du client en cours.</span><span class="sxs-lookup"><span data-stu-id="887f8-110">SuperPan is a feature that allows a user to easily navigate a remote desktop in full-screen mode, when the dimensions of the remote desktop are larger than the dimensions of the current client window.</span></span> <span data-ttu-id="887f8-111">Au lieu d’utiliser des barres de défilement pour naviguer sur le bureau, l’utilisateur peut pointer sur la bordure de la fenêtre et le Bureau à distance effectue un défilement automatique dans cette direction.</span><span class="sxs-lookup"><span data-stu-id="887f8-111">Instead of using scroll bars to navigate the desktop, the user can point to the window border, and the remote desktop will scroll automatically in that direction.</span></span> <span data-ttu-id="887f8-112">SuperPan ne prend pas en charge plus d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="887f8-112">SuperPan does not support more than one monitor.</span></span>

<span data-ttu-id="887f8-113">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="887f8-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="887f8-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="887f8-114">Syntax</span></span>


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a><span data-ttu-id="887f8-115">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="887f8-115">Property value</span></span>

<span data-ttu-id="887f8-116">Valeur **\_ booléenne variant** qui spécifie si SuperPan est activé.</span><span class="sxs-lookup"><span data-stu-id="887f8-116">A **VARIANT\_BOOL** value that specifies whether SuperPan is enabled.</span></span> <span data-ttu-id="887f8-117">La valeur **Variant \_ true** spécifie que SuperPan est activé.</span><span class="sxs-lookup"><span data-stu-id="887f8-117">A value of **VARIANT\_TRUE** specifies that SuperPan is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="887f8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="887f8-118">Requirements</span></span>



| <span data-ttu-id="887f8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="887f8-119">Requirement</span></span> | <span data-ttu-id="887f8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="887f8-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="887f8-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="887f8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="887f8-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="887f8-122">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="887f8-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="887f8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="887f8-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="887f8-124">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="887f8-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="887f8-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="887f8-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="887f8-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="887f8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="887f8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="887f8-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="887f8-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="887f8-129">IID</span><span class="sxs-lookup"><span data-stu-id="887f8-129">IID</span></span><br/>                      | <span data-ttu-id="887f8-130">IID \_ IMsRdpClientAdvancedSettings7 est défini en tant que 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="887f8-130">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="887f8-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="887f8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="887f8-132">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="887f8-132">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="887f8-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="887f8-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





