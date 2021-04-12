---
title: Énumération VMLogoffType (VPCCOMInterfaces. h)
description: Indique comment arrêter un ordinateur virtuel.
ms.assetid: 3a2965e3-2637-4677-b487-98d2b508672c
keywords:
- Virtual PC de l’énumération VMLogoffType
topic_type:
- apiref
api_name:
- VMLogoffType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2311736115390d807058bbfc54c24e7f9e9654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032816"
---
# <a name="vmlogofftype-enumeration"></a><span data-ttu-id="5886a-104">Énumération VMLogoffType</span><span class="sxs-lookup"><span data-stu-id="5886a-104">VMLogoffType enumeration</span></span>

<span data-ttu-id="5886a-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5886a-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5886a-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5886a-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5886a-107">Indique comment arrêter un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="5886a-107">Specifies how to shut down a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="5886a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5886a-108">Syntax</span></span>


```C++
typedef enum  { 
  vmLogoff_Normal    = 0,
  vmLogoff_Forced    = 1,
  vmLogoff_External  = 2
} VMLogoffType;
```



## <a name="constants"></a><span data-ttu-id="5886a-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="5886a-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5886a-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff \_ normal**</span><span class="sxs-lookup"><span data-stu-id="5886a-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="5886a-111">La fermeture de session dans la machine virtuelle invitée était normale.</span><span class="sxs-lookup"><span data-stu-id="5886a-111">The logoff in the guest VM was normal.</span></span>

</dd> <dt>

<span data-ttu-id="5886a-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff \_ forcé**</span><span class="sxs-lookup"><span data-stu-id="5886a-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff\_Forced**</span></span>
</dt> <dd>

<span data-ttu-id="5886a-113">La fermeture de session de la machine virtuelle invitée a été forcée.</span><span class="sxs-lookup"><span data-stu-id="5886a-113">The logoff in the guest VM was forced.</span></span>

</dd> <dt>

<span data-ttu-id="5886a-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff \_ externe**</span><span class="sxs-lookup"><span data-stu-id="5886a-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff\_External**</span></span>
</dt> <dd>

<span data-ttu-id="5886a-115">La déconnexion de la machine virtuelle invitée a été effectuée à l’aide de la méthode [**IVMGuestOS :: Logoff**](ivmguestos-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="5886a-115">The logoff in the guest VM was done using the [**IVMGuestOS::Logoff**](ivmguestos-logoff.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5886a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5886a-116">Requirements</span></span>



| <span data-ttu-id="5886a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5886a-117">Requirement</span></span> | <span data-ttu-id="5886a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5886a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5886a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5886a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5886a-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5886a-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5886a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5886a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5886a-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5886a-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5886a-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="5886a-123">End of client support</span></span><br/>    | <span data-ttu-id="5886a-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5886a-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5886a-125">Produit</span><span class="sxs-lookup"><span data-stu-id="5886a-125">Product</span></span><br/>                  | <span data-ttu-id="5886a-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5886a-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5886a-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="5886a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5886a-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5886a-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5886a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5886a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5886a-130">**IVMVirtualMachine::ShutdownActionOnQuit**</span><span class="sxs-lookup"><span data-stu-id="5886a-130">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

