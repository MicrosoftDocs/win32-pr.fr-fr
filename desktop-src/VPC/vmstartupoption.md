---
title: Énumération VMStartupOption (VPCCOMInterfaces. h)
description: Spécifie l’option de démarrage.
ms.assetid: ac4de9a7-7fc7-4361-89dd-e7da8f5dbb92
keywords:
- Virtual PC de l’énumération VMStartupOption
topic_type:
- apiref
api_name:
- VMStartupOption
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc4a3bbcc1c82c57dfe144f818c29b403fd83a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465190"
---
# <a name="vmstartupoption-enumeration"></a><span data-ttu-id="1e199-104">Énumération VMStartupOption</span><span class="sxs-lookup"><span data-stu-id="1e199-104">VMStartupOption enumeration</span></span>

<span data-ttu-id="1e199-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1e199-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1e199-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1e199-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1e199-107">Spécifie l’option de démarrage.</span><span class="sxs-lookup"><span data-stu-id="1e199-107">Specifies the start-up option.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e199-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e199-108">Syntax</span></span>


```C++
typedef enum  { 
  vmStartupOption_Normal                      = 0,
  vmStartupOption_FixParentTimestampMismatch  = 1
} VMStartupOption;
```



## <a name="constants"></a><span data-ttu-id="1e199-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="1e199-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1e199-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmStartupOption \_ normal**</span><span class="sxs-lookup"><span data-stu-id="1e199-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmStartupOption\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="1e199-111">Démarrez normalement.</span><span class="sxs-lookup"><span data-stu-id="1e199-111">Start normally.</span></span>

</dd> <dt>

<span data-ttu-id="1e199-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**vmStartupOption \_ FixParentTimestampMismatch**</span><span class="sxs-lookup"><span data-stu-id="1e199-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**vmStartupOption\_FixParentTimestampMismatch**</span></span>
</dt> <dd>

<span data-ttu-id="1e199-113">Corrigez l’incompatibilité d’horodatage parent.</span><span class="sxs-lookup"><span data-stu-id="1e199-113">Fix the parent timestamp mismatch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e199-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e199-114">Requirements</span></span>



| <span data-ttu-id="1e199-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e199-115">Requirement</span></span> | <span data-ttu-id="1e199-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e199-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e199-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e199-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1e199-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e199-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e199-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e199-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1e199-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e199-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1e199-121">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1e199-121">End of client support</span></span><br/>    | <span data-ttu-id="1e199-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e199-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1e199-123">Produit</span><span class="sxs-lookup"><span data-stu-id="1e199-123">Product</span></span><br/>                  | <span data-ttu-id="1e199-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1e199-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1e199-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e199-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e199-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e199-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e199-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e199-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e199-128">**IVMVirtualMachine :: Startup2**</span><span class="sxs-lookup"><span data-stu-id="1e199-128">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
</dt> </dl>

 

