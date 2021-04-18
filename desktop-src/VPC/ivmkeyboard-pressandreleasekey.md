---
title: Méthode IVMKeyboard PressAndReleaseKey (VPCCOMInterfaces. h)
description: Simule une touche enfoncée, puis relâchée.
ms.assetid: 2a7fc36f-f1bf-4f1d-b8f7-ea5b167c82a7
keywords:
- Méthode PressAndReleaseKey Virtual PC
- Méthode PressAndReleaseKey Virtual PC, interface IVMKeyboard
- IVMKeyboard interface Virtual PC, méthode PressAndReleaseKey
topic_type:
- apiref
api_name:
- IVMKeyboard.PressAndReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4adbcac2c79c02ce69584bbfdf21a6b08b350a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543053"
---
# <a name="ivmkeyboardpressandreleasekey-method"></a><span data-ttu-id="2c93b-106">IVMKeyboard ::P méthode ressAndReleaseKey</span><span class="sxs-lookup"><span data-stu-id="2c93b-106">IVMKeyboard::PressAndReleaseKey method</span></span>

<span data-ttu-id="2c93b-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2c93b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2c93b-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2c93b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2c93b-109">Simule une touche enfoncée, puis relâchée.</span><span class="sxs-lookup"><span data-stu-id="2c93b-109">Simulates a key being pressed down and then released.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c93b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c93b-110">Syntax</span></span>


```C++
HRESULT PressAndReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a><span data-ttu-id="2c93b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c93b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c93b-112">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2c93b-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c93b-113">Code clé pour la touche à enfoncer et à libérer.</span><span class="sxs-lookup"><span data-stu-id="2c93b-113">The key code for the key to be pressed and released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c93b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c93b-114">Return value</span></span>

<span data-ttu-id="2c93b-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2c93b-115">This method can return one of these values.</span></span>



| <span data-ttu-id="2c93b-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2c93b-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="2c93b-117">Description</span><span class="sxs-lookup"><span data-stu-id="2c93b-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c93b-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2c93b-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2c93b-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2c93b-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2c93b-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2c93b-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2c93b-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="2c93b-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="2c93b-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="2c93b-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="2c93b-123">La chaîne spécifiée est vide ou contient un code de clé non valide.</span><span class="sxs-lookup"><span data-stu-id="2c93b-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="2c93b-124"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2c93b-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2c93b-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2c93b-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="2c93b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c93b-126">Requirements</span></span>



| <span data-ttu-id="2c93b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c93b-127">Requirement</span></span> | <span data-ttu-id="2c93b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c93b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c93b-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c93b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2c93b-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c93b-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c93b-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c93b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2c93b-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c93b-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2c93b-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2c93b-133">End of client support</span></span><br/>    | <span data-ttu-id="2c93b-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c93b-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2c93b-135">Produit</span><span class="sxs-lookup"><span data-stu-id="2c93b-135">Product</span></span><br/>                  | <span data-ttu-id="2c93b-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2c93b-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2c93b-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c93b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c93b-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c93b-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2c93b-139">IID</span><span class="sxs-lookup"><span data-stu-id="2c93b-139">IID</span></span><br/>                      | <span data-ttu-id="2c93b-140">IID \_ IVMKeyboard est défini en tant que 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="2c93b-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="2c93b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c93b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c93b-142">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="2c93b-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

