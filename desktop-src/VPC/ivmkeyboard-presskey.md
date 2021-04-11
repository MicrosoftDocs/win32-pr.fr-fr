---
title: Méthode IVMKeyboard PressKey (VPCCOMInterfaces. h)
description: Simule une touche enfoncée.
ms.assetid: d945128a-ffde-465c-b615-83a1d5dc789f
keywords:
- Méthode PressKey Virtual PC
- Méthode PressKey Virtual PC, interface IVMKeyboard
- IVMKeyboard interface Virtual PC, méthode PressKey
topic_type:
- apiref
api_name:
- IVMKeyboard.PressKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8175447a819afa7f761899a7e0dd3cbbcc780631
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032992"
---
# <a name="ivmkeyboardpresskey-method"></a><span data-ttu-id="5ef75-106">IVMKeyboard ::P méthode ressKey</span><span class="sxs-lookup"><span data-stu-id="5ef75-106">IVMKeyboard::PressKey method</span></span>

<span data-ttu-id="5ef75-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5ef75-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5ef75-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5ef75-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5ef75-109">Simule une touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="5ef75-109">Simulates a key being pressed down.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ef75-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ef75-110">Syntax</span></span>


```C++
HRESULT PressKey(
  [in] BSTR key
);
```



## <a name="parameters"></a><span data-ttu-id="5ef75-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ef75-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ef75-112">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5ef75-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ef75-113">Code clé de la touche à enfoncée.</span><span class="sxs-lookup"><span data-stu-id="5ef75-113">The key code for the key to be pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ef75-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ef75-114">Return value</span></span>

<span data-ttu-id="5ef75-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="5ef75-115">This method can return one of these values.</span></span>



| <span data-ttu-id="5ef75-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5ef75-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="5ef75-117">Description</span><span class="sxs-lookup"><span data-stu-id="5ef75-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ef75-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5ef75-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5ef75-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="5ef75-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5ef75-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="5ef75-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="5ef75-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5ef75-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="5ef75-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="5ef75-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="5ef75-123">La chaîne spécifiée est vide ou contient un code de clé non valide.</span><span class="sxs-lookup"><span data-stu-id="5ef75-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="5ef75-124"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5ef75-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="5ef75-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="5ef75-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="5ef75-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ef75-126">Requirements</span></span>



| <span data-ttu-id="5ef75-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ef75-127">Requirement</span></span> | <span data-ttu-id="5ef75-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ef75-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef75-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ef75-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef75-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ef75-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5ef75-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ef75-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef75-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ef75-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5ef75-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="5ef75-133">End of client support</span></span><br/>    | <span data-ttu-id="5ef75-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5ef75-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5ef75-135">Produit</span><span class="sxs-lookup"><span data-stu-id="5ef75-135">Product</span></span><br/>                  | <span data-ttu-id="5ef75-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5ef75-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5ef75-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ef75-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ef75-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ef75-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5ef75-139">IID</span><span class="sxs-lookup"><span data-stu-id="5ef75-139">IID</span></span><br/>                      | <span data-ttu-id="5ef75-140">IID \_ IVMKeyboard est défini en tant que 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="5ef75-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="5ef75-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ef75-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef75-142">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="5ef75-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

