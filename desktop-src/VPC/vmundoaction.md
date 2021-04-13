---
title: Énumération VMUndoAction (VPCCOMInterfaces. h)
description: Spécifie ce qui se passe pour annuler les lecteurs lorsqu’une machine virtuelle est arrêtée ou désactivée.
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- Virtual PC de l’énumération VMUndoAction
topic_type:
- apiref
api_name:
- VMUndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10917a5fb8d00e16a28f4b175237484b977cf914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509326"
---
# <a name="vmundoaction-enumeration"></a><span data-ttu-id="106df-104">Énumération VMUndoAction</span><span class="sxs-lookup"><span data-stu-id="106df-104">VMUndoAction enumeration</span></span>

<span data-ttu-id="106df-105">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="106df-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="106df-106">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="106df-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="106df-107">Spécifie ce qui se passe pour annuler les lecteurs lorsqu’une machine virtuelle est arrêtée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="106df-107">Specifies what happens to undo drives when a virtual machine is shut down or turned off.</span></span>

## <a name="syntax"></a><span data-ttu-id="106df-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="106df-108">Syntax</span></span>


```C++
typedef enum  { 
  vmUndoAction_Discard  = 0,
  vmUndoAction_Keep     = 1,
  vmUndoAction_Commit   = 2
} VMUndoAction;
```



## <a name="constants"></a><span data-ttu-id="106df-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="106df-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="106df-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**vmUndoAction \_ Ignorer**</span><span class="sxs-lookup"><span data-stu-id="106df-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**vmUndoAction\_Discard**</span></span>
</dt> <dd>

<span data-ttu-id="106df-111">Ignorer les lecteurs d’annulations ; les lecteurs parents restent inchangés.</span><span class="sxs-lookup"><span data-stu-id="106df-111">Discard the undo drives; the parent drives remain unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="106df-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction \_ conserver**</span><span class="sxs-lookup"><span data-stu-id="106df-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction\_Keep**</span></span>
</dt> <dd>

<span data-ttu-id="106df-113">Conserver les disques d’annulations ; les lecteurs parents restent inchangés, mais les modifications sont conservées lors du prochain démarrage de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="106df-113">Keep the undo drives; the parent drives remain unchanged, but changes will be maintained the next time the virtual machine starts.</span></span>

</dd> <dt>

<span data-ttu-id="106df-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**\_validation vmUndoAction**</span><span class="sxs-lookup"><span data-stu-id="106df-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**vmUndoAction\_Commit**</span></span>
</dt> <dd>

<span data-ttu-id="106df-115">Valider les modifications apportées aux lecteurs parents.</span><span class="sxs-lookup"><span data-stu-id="106df-115">Commit changes to the parent drives.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="106df-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="106df-116">Requirements</span></span>



| <span data-ttu-id="106df-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="106df-117">Requirement</span></span> | <span data-ttu-id="106df-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="106df-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="106df-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="106df-119">Minimum supported client</span></span><br/> | <span data-ttu-id="106df-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="106df-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="106df-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="106df-121">Minimum supported server</span></span><br/> | <span data-ttu-id="106df-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="106df-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="106df-123">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="106df-123">End of client support</span></span><br/>    | <span data-ttu-id="106df-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="106df-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="106df-125">Produit</span><span class="sxs-lookup"><span data-stu-id="106df-125">Product</span></span><br/>                  | <span data-ttu-id="106df-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="106df-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="106df-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="106df-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="106df-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="106df-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="106df-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="106df-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="106df-130">**IVMVirtualMachine :: UndoAction**</span><span class="sxs-lookup"><span data-stu-id="106df-130">**IVMVirtualMachine::UndoAction**</span></span>](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

