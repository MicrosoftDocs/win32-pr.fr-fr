---
title: Méthode IVMKeyboard TypeKeySequence (VPCCOMInterfaces. h)
description: Simule une liste délimitée par des virgules des clés en cours de saisie.
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- Méthode TypeKeySequence Virtual PC
- Méthode TypeKeySequence Virtual PC, interface IVMKeyboard
- IVMKeyboard interface Virtual PC, méthode TypeKeySequence
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeKeySequence
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34bd96077c1d28aad196ee0d6b11de122725d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942782"
---
# <a name="ivmkeyboardtypekeysequence-method"></a><span data-ttu-id="2d3d9-106">IVMKeyboard :: TypeKeySequence, méthode</span><span class="sxs-lookup"><span data-stu-id="2d3d9-106">IVMKeyboard::TypeKeySequence method</span></span>

<span data-ttu-id="2d3d9-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2d3d9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2d3d9-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2d3d9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2d3d9-109">Simule une liste délimitée par des virgules des clés en cours de saisie.</span><span class="sxs-lookup"><span data-stu-id="2d3d9-109">Simulates a comma-delimited list of keys being typed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d3d9-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d3d9-110">Syntax</span></span>


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a><span data-ttu-id="2d3d9-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d3d9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d3d9-112">*séquence de touches* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d3d9-112">*keySequence* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d3d9-113">Séquence de codes clés délimités par des virgules à taper.</span><span class="sxs-lookup"><span data-stu-id="2d3d9-113">The comma-delimited sequence of key codes to be typed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d3d9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d3d9-114">Return value</span></span>

<span data-ttu-id="2d3d9-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2d3d9-115">This method can return one of these values.</span></span>



| <span data-ttu-id="2d3d9-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2d3d9-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="2d3d9-117">Description</span><span class="sxs-lookup"><span data-stu-id="2d3d9-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d3d9-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2d3d9-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2d3d9-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2d3d9-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2d3d9-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2d3d9-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2d3d9-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="2d3d9-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="2d3d9-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="2d3d9-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="2d3d9-123">La chaîne spécifiée est vide ou contient un code de clé non valide.</span><span class="sxs-lookup"><span data-stu-id="2d3d9-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="2d3d9-124"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2d3d9-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2d3d9-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2d3d9-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="2d3d9-126">Notes</span><span class="sxs-lookup"><span data-stu-id="2d3d9-126">Remarks</span></span>

<span data-ttu-id="2d3d9-127">Une chaîne de séquence clé est un ensemble d’identificateurs de clé délimités par des virgules, qui sont utilisés pour simuler l’appui sur la touche et la séquence de mise en version d’un clavier standard de style « 101 ».</span><span class="sxs-lookup"><span data-stu-id="2d3d9-127">A key sequence string is a comma-delimited set of key identifiers which are used to simulate the key press and release sequence of a standard U.S. 101-key AT-style keyboard.</span></span>

<span data-ttu-id="2d3d9-128">Si un identificateur de clé apparaît dans la chaîne sans modificateur précédent, un code appuyé sur la touche est envoyé à la session de l’ordinateur virtuel, suivi immédiatement du code de sortie de la clé correspondant.</span><span class="sxs-lookup"><span data-stu-id="2d3d9-128">If a key identifier appears in the string without a preceding modifier, a key-pressed code is sent to the virtual machine session, followed immediately by its corresponding key-released code.</span></span> <span data-ttu-id="2d3d9-129">Les modificateurs de clé peuvent être utilisés pour modifier ce comportement.</span><span class="sxs-lookup"><span data-stu-id="2d3d9-129">Key modifiers can be used to change this behavior.</span></span>

<span data-ttu-id="2d3d9-130">Par exemple, le modificateur UpDown envoie le code appuyé sur la touche pour l’identificateur de clé suivant sans envoyer le code de sortie de clé.</span><span class="sxs-lookup"><span data-stu-id="2d3d9-130">For example, the DOWN modifier will send the key-pressed code for the following key identifier without sending the key-released code.</span></span> <span data-ttu-id="2d3d9-131">Cela est utile pour simuler les touches Ctrl, Alt et Maj lorsqu’elles sont maintenues pendant que d’autres touches sont envoyées.</span><span class="sxs-lookup"><span data-stu-id="2d3d9-131">This is useful for simulating Ctrl, Alt, and Shift keys when they are held down while other keys are being sent.</span></span> <span data-ttu-id="2d3d9-132">Pour libérer la clé, elle doit être incluse dans la chaîne de clé avec un modificateur UP précédent.</span><span class="sxs-lookup"><span data-stu-id="2d3d9-132">To release the key, it must be included in the key string again along with a preceding UP modifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d3d9-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d3d9-133">Requirements</span></span>



| <span data-ttu-id="2d3d9-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d3d9-134">Requirement</span></span> | <span data-ttu-id="2d3d9-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d3d9-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d3d9-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d3d9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2d3d9-137">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d3d9-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d3d9-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d3d9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2d3d9-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d3d9-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2d3d9-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2d3d9-140">End of client support</span></span><br/>    | <span data-ttu-id="2d3d9-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d3d9-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2d3d9-142">Produit</span><span class="sxs-lookup"><span data-stu-id="2d3d9-142">Product</span></span><br/>                  | <span data-ttu-id="2d3d9-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2d3d9-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2d3d9-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d3d9-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d3d9-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d3d9-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2d3d9-146">IID</span><span class="sxs-lookup"><span data-stu-id="2d3d9-146">IID</span></span><br/>                      | <span data-ttu-id="2d3d9-147">IID \_ IVMKeyboard est défini en tant que 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="2d3d9-147">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="2d3d9-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d3d9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d3d9-149">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="2d3d9-149">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> <dt>

[<span data-ttu-id="2d3d9-150">Séquences de touches</span><span class="sxs-lookup"><span data-stu-id="2d3d9-150">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

