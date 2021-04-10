---
title: Méthode IVMKeyboard TypeAsciiText (VPCCOMInterfaces. h)
description: Simule une série de touches ASCII tapées dans l’invité.
ms.assetid: 6c7fbfed-d495-4f11-a7d1-dc08bd075870
keywords:
- Méthode TypeAsciiText Virtual PC
- Méthode TypeAsciiText Virtual PC, interface IVMKeyboard
- IVMKeyboard interface Virtual PC, méthode TypeAsciiText
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeAsciiText
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538df9fc3036e43dc36f4ca7425688157e9fca77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104272"
---
# <a name="ivmkeyboardtypeasciitext-method"></a><span data-ttu-id="078c3-106">IVMKeyboard :: TypeAsciiText, méthode</span><span class="sxs-lookup"><span data-stu-id="078c3-106">IVMKeyboard::TypeAsciiText method</span></span>

<span data-ttu-id="078c3-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="078c3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="078c3-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="078c3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="078c3-109">Simule une série de touches ASCII tapées dans l’invité.</span><span class="sxs-lookup"><span data-stu-id="078c3-109">Simulates a series of ASCII keys being typed into the guest.</span></span>

## <a name="syntax"></a><span data-ttu-id="078c3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="078c3-110">Syntax</span></span>


```C++
HRESULT TypeAsciiText(
  [in] BSTR text
);
```



## <a name="parameters"></a><span data-ttu-id="078c3-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="078c3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="078c3-112">*texte* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="078c3-112">*text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="078c3-113">Chaîne de texte ASCII à taper à l’intérieur de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="078c3-113">The ASCII text string to be typed inside the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="078c3-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="078c3-114">Return value</span></span>

<span data-ttu-id="078c3-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="078c3-115">This method can return one of these values.</span></span>



| <span data-ttu-id="078c3-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="078c3-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="078c3-117">Description</span><span class="sxs-lookup"><span data-stu-id="078c3-117">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="078c3-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="078c3-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="078c3-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="078c3-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="078c3-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="078c3-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="078c3-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="078c3-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="078c3-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="078c3-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="078c3-123">La chaîne spécifiée est vide.</span><span class="sxs-lookup"><span data-stu-id="078c3-123">The specified string is empty.</span></span><br/>    |
| <dl> <span data-ttu-id="078c3-124"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="078c3-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="078c3-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="078c3-125">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="078c3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="078c3-126">Requirements</span></span>



| <span data-ttu-id="078c3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="078c3-127">Requirement</span></span> | <span data-ttu-id="078c3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="078c3-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="078c3-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="078c3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="078c3-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="078c3-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="078c3-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="078c3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="078c3-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="078c3-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="078c3-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="078c3-133">End of client support</span></span><br/>    | <span data-ttu-id="078c3-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="078c3-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="078c3-135">Produit</span><span class="sxs-lookup"><span data-stu-id="078c3-135">Product</span></span><br/>                  | <span data-ttu-id="078c3-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="078c3-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="078c3-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="078c3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="078c3-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="078c3-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="078c3-139">IID</span><span class="sxs-lookup"><span data-stu-id="078c3-139">IID</span></span><br/>                      | <span data-ttu-id="078c3-140">IID \_ IVMKeyboard est défini en tant que 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="078c3-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="078c3-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="078c3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="078c3-142">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="078c3-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

