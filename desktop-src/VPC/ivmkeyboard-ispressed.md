---
title: IVMKeyboard IsPressed, méthode (VPCCOMInterfaces. h)
description: Détermine si la touche spécifiée est enfoncée.
ms.assetid: 7541d678-762a-4c2e-80cd-686bb56c9cd7
keywords:
- Méthode IsPressed Virtual PC
- IsPressed, méthode Virtual PC, interface IVMKeyboard
- IVMKeyboard interface Virtual PC, IsPressed, méthode
topic_type:
- apiref
api_name:
- IVMKeyboard.IsPressed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a4185fa0310994bc1cffa917348dfca2fdedfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742597"
---
# <a name="ivmkeyboardispressed-method"></a><span data-ttu-id="0e580-106">IVMKeyboard :: IsPressed, méthode</span><span class="sxs-lookup"><span data-stu-id="0e580-106">IVMKeyboard::IsPressed method</span></span>

<span data-ttu-id="0e580-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0e580-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0e580-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0e580-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0e580-109">Détermine si la touche spécifiée est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="0e580-109">Determines whether the specified key is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e580-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e580-110">Syntax</span></span>


```C++
HRESULT IsPressed(
  [in]          BSTR         key,
  [out, retval] VARIANT_BOOL *pressed
);
```



## <a name="parameters"></a><span data-ttu-id="0e580-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e580-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e580-112">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e580-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e580-113">Code clé de la clé dont l’État doit être interrogé.</span><span class="sxs-lookup"><span data-stu-id="0e580-113">The key code for the key whose state is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="0e580-114">*enfoncé* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0e580-114">*pressed* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0e580-115">**True** si la touche est actuellement enfoncée ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="0e580-115">**TRUE** if the key is currently pressed down, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e580-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e580-116">Return value</span></span>

<span data-ttu-id="0e580-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="0e580-117">This method can return one of these values.</span></span>



| <span data-ttu-id="0e580-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0e580-118">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="0e580-119">Description</span><span class="sxs-lookup"><span data-stu-id="0e580-119">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e580-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0e580-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0e580-121">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0e580-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0e580-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0e580-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0e580-123">Un paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0e580-123">A parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="0e580-124"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="0e580-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="0e580-125">La chaîne spécifiée est vide ou contient un code de clé non valide.</span><span class="sxs-lookup"><span data-stu-id="0e580-125">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="0e580-126"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0e580-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0e580-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0e580-127">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="0e580-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e580-128">Requirements</span></span>



| <span data-ttu-id="0e580-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e580-129">Requirement</span></span> | <span data-ttu-id="0e580-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e580-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e580-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e580-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0e580-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e580-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0e580-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e580-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0e580-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e580-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0e580-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0e580-135">End of client support</span></span><br/>    | <span data-ttu-id="0e580-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e580-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0e580-137">Produit</span><span class="sxs-lookup"><span data-stu-id="0e580-137">Product</span></span><br/>                  | <span data-ttu-id="0e580-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0e580-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0e580-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e580-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e580-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e580-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0e580-141">IID</span><span class="sxs-lookup"><span data-stu-id="0e580-141">IID</span></span><br/>                      | <span data-ttu-id="0e580-142">IID \_ IVMKeyboard est défini en tant que 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="0e580-142">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="0e580-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e580-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e580-144">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="0e580-144">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

