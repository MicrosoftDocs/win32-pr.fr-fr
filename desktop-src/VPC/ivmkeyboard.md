---
title: Interface IVMKeyboard (VPCCOMInterfaces. h)
description: Contrôle le périphérique clavier au sein d’un ordinateur virtuel. Le IVMKeyboard d’un ordinateur virtuel peut être récupéré à l’aide de la propriété de clavier IVMVirtualMachine.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- Virtual PC de l’interface IVMKeyboard
- IVMKeyboard interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMKeyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce2ddddd00de509278760a22fe3ab464f27c1c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513034"
---
# <a name="ivmkeyboard-interface"></a><span data-ttu-id="05edb-106">Interface IVMKeyboard</span><span class="sxs-lookup"><span data-stu-id="05edb-106">IVMKeyboard interface</span></span>

<span data-ttu-id="05edb-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="05edb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="05edb-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="05edb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="05edb-109">Contrôle le périphérique clavier au sein d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="05edb-109">Controls the keyboard device within a virtual machine.</span></span> <span data-ttu-id="05edb-110">Le **IVMKeyboard** d’un ordinateur virtuel peut être récupéré à l’aide de la propriété [**IVMVirtualMachine :: Keyboard**](ivmvirtualmachine-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="05edb-110">The **IVMKeyboard** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Keyboard**](ivmvirtualmachine-keyboard.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="05edb-111">Membres</span><span class="sxs-lookup"><span data-stu-id="05edb-111">Members</span></span>

<span data-ttu-id="05edb-112">L’interface **IVMKeyboard** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="05edb-112">The **IVMKeyboard** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="05edb-113">**IVMKeyboard** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="05edb-113">**IVMKeyboard** also has these types of members:</span></span>

-   [<span data-ttu-id="05edb-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="05edb-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="05edb-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="05edb-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="05edb-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="05edb-116">Methods</span></span>

<span data-ttu-id="05edb-117">L’interface **IVMKeyboard** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="05edb-117">The **IVMKeyboard** interface has these methods.</span></span>



| <span data-ttu-id="05edb-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="05edb-118">Method</span></span>                                                       | <span data-ttu-id="05edb-119">Description</span><span class="sxs-lookup"><span data-stu-id="05edb-119">Description</span></span>                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="05edb-120">**IsPressed**</span><span class="sxs-lookup"><span data-stu-id="05edb-120">**IsPressed**</span></span>](ivmkeyboard-ispressed.md)                   | <span data-ttu-id="05edb-121">Détermine si la touche spécifiée est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="05edb-121">Determines whether the specified key is down.</span></span><br/>                      |
| [<span data-ttu-id="05edb-122">**PressAndReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="05edb-122">**PressAndReleaseKey**</span></span>](ivmkeyboard-pressandreleasekey.md) | <span data-ttu-id="05edb-123">Simule une touche enfoncée, puis relâchée.</span><span class="sxs-lookup"><span data-stu-id="05edb-123">Simulates a key being pressed down and then released.</span></span><br/>              |
| [<span data-ttu-id="05edb-124">**PressKey**</span><span class="sxs-lookup"><span data-stu-id="05edb-124">**PressKey**</span></span>](ivmkeyboard-presskey.md)                     | <span data-ttu-id="05edb-125">Simule une touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="05edb-125">Simulates a key being pressed down.</span></span><br/>                                |
| [<span data-ttu-id="05edb-126">**ReleaseKey**</span><span class="sxs-lookup"><span data-stu-id="05edb-126">**ReleaseKey**</span></span>](ivmkeyboard-releasekey.md)                 | <span data-ttu-id="05edb-127">Simule une touche en cours de libération.</span><span class="sxs-lookup"><span data-stu-id="05edb-127">Simulates a key being released.</span></span><br/>                                    |
| [<span data-ttu-id="05edb-128">**TypeAsciiText**</span><span class="sxs-lookup"><span data-stu-id="05edb-128">**TypeAsciiText**</span></span>](ivmkeyboard-typeasciitext.md)           | <span data-ttu-id="05edb-129">Simule une série de touches ASCII tapées dans l’invité.</span><span class="sxs-lookup"><span data-stu-id="05edb-129">Simulates a series of ASCII keys being typed into the guest.</span></span><br/>       |
| [<span data-ttu-id="05edb-130">**TypeKeySequence**</span><span class="sxs-lookup"><span data-stu-id="05edb-130">**TypeKeySequence**</span></span>](ivmkeyboard-typekeysequence.md)       | <span data-ttu-id="05edb-131">Simule une liste délimitée par des virgules des clés en cours de saisie dans l’invité.</span><span class="sxs-lookup"><span data-stu-id="05edb-131">Simulates a comma-delimited list of keys being typed in the guest.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="05edb-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="05edb-132">Properties</span></span>

<span data-ttu-id="05edb-133">L’interface **IVMKeyboard** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="05edb-133">The **IVMKeyboard** interface has these properties.</span></span>



| <span data-ttu-id="05edb-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="05edb-134">Property</span></span>                                                                | <span data-ttu-id="05edb-135">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="05edb-135">Access type</span></span>           | <span data-ttu-id="05edb-136">Description</span><span class="sxs-lookup"><span data-stu-id="05edb-136">Description</span></span>                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05edb-137">**HasExclusiveAccess**</span><span class="sxs-lookup"><span data-stu-id="05edb-137">**HasExclusiveAccess**</span></span>](ivmkeyboard-hasexclusiveaccess.md)<br/> | <span data-ttu-id="05edb-138">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="05edb-138">Read/write</span></span><br/> | <span data-ttu-id="05edb-139">Indique si cet objet a un contrôle exclusif sur le périphérique clavier de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="05edb-139">Indicates whether this object has exclusive control over the virtual machine's keyboard device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="05edb-140">Notes</span><span class="sxs-lookup"><span data-stu-id="05edb-140">Remarks</span></span>

<span data-ttu-id="05edb-141">Les clés peuvent être tapées dans la machine virtuelle de plusieurs façons.</span><span class="sxs-lookup"><span data-stu-id="05edb-141">Keys can be typed into the virtual machine in several ways.</span></span> <span data-ttu-id="05edb-142">Pour taper une séquence de caractères ASCII normale, utilisez la méthode [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) .</span><span class="sxs-lookup"><span data-stu-id="05edb-142">To type a normal ASCII sequence of characters, use the [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) method.</span></span> <span data-ttu-id="05edb-143">Si vous avez besoin d’une plus grande flexibilité, **IVMKeyboard** dispose de plusieurs méthodes conçues pour être utilisées avec les codes de touches de la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="05edb-143">If greater flexibility is required, **IVMKeyboard** has several methods that are designed to be used with the key codes in the following list.</span></span> <span data-ttu-id="05edb-144">La méthode [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) peut accepter une chaîne délimitée par des virgules de codes clés, qui sera appuyée et libérée, dans l’ordre, dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="05edb-144">The [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) method can accept a comma-delimited string of key codes, which will be pressed and released, in order, within the virtual machine.</span></span> <span data-ttu-id="05edb-145">En plus de ces codes clés, les mots clés UP et UpDown peuvent être utilisés pour forcer une touche à uniquement être enfoncée ou être libérée.</span><span class="sxs-lookup"><span data-stu-id="05edb-145">In addition to these key codes, the keywords UP and DOWN can be used to force a key to only be pressed, or only be released.</span></span> <span data-ttu-id="05edb-146">Les mots clés UP et UpDown s’appliquent uniquement au code clé qui suit directement le mot clé.</span><span class="sxs-lookup"><span data-stu-id="05edb-146">The UP and DOWN keywords only apply to the key code directly following the keyword.</span></span>

<span data-ttu-id="05edb-147">Pour éviter que plusieurs scripts, applications ou utilisateurs essaient d’accéder simultanément au même périphérique clavier, affectez la valeur **true** à la propriété [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) .</span><span class="sxs-lookup"><span data-stu-id="05edb-147">To avoid multiple scripts, applications, or users from simultaneously attempting to access the same keyboard device, set the [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) property to **TRUE**.</span></span> <span data-ttu-id="05edb-148">Si l’accès exclusif est acquis par un processus, toute tentative d’envoi d’une entrée au clavier par d’autres processus est ignorée jusqu’à ce que l’accès exclusif soit libéré.</span><span class="sxs-lookup"><span data-stu-id="05edb-148">If exclusive access is acquired by one process, any attempts by other processes to send input to the keyboard device will be ignored until exclusive access has been released.</span></span>

## <a name="requirements"></a><span data-ttu-id="05edb-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05edb-149">Requirements</span></span>



| <span data-ttu-id="05edb-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05edb-150">Requirement</span></span> | <span data-ttu-id="05edb-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="05edb-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="05edb-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05edb-152">Minimum supported client</span></span><br/> | <span data-ttu-id="05edb-153">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05edb-153">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="05edb-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05edb-154">Minimum supported server</span></span><br/> | <span data-ttu-id="05edb-155">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="05edb-155">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="05edb-156">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="05edb-156">End of client support</span></span><br/>    | <span data-ttu-id="05edb-157">Windows 7</span><span class="sxs-lookup"><span data-stu-id="05edb-157">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="05edb-158">Produit</span><span class="sxs-lookup"><span data-stu-id="05edb-158">Product</span></span><br/>                  | <span data-ttu-id="05edb-159">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="05edb-159">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="05edb-160">En-tête</span><span class="sxs-lookup"><span data-stu-id="05edb-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="05edb-161"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="05edb-161"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="05edb-162">IID</span><span class="sxs-lookup"><span data-stu-id="05edb-162">IID</span></span><br/>                      | <span data-ttu-id="05edb-163">IID \_ IVMKeyboard est défini en tant que 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="05edb-163">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="05edb-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05edb-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05edb-165">Interfaces de PC virtuels Windows</span><span class="sxs-lookup"><span data-stu-id="05edb-165">Windows Virtual PC Interfaces</span></span>](virtual-pc-interfaces.md)
</dt> <dt>

[<span data-ttu-id="05edb-166">Séquences de touches</span><span class="sxs-lookup"><span data-stu-id="05edb-166">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

