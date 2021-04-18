---
title: Méthode IVMDisplay SetDimensions (VPCCOMInterfaces. h)
description: Définit la hauteur et la largeur de l’affichage de la machine virtuelle, en pixels.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- Méthode SetDimensions Virtual PC
- Méthode SetDimensions Virtual PC, interface IVMDisplay
- IVMDisplay interface Virtual PC, méthode SetDimensions
topic_type:
- apiref
api_name:
- IVMDisplay.SetDimensions
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4730d73e06074714c8e6ed31fda992259d5c19ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512197"
---
# <a name="ivmdisplaysetdimensions-method"></a><span data-ttu-id="d5fcc-106">IVMDisplay :: SetDimensions, méthode</span><span class="sxs-lookup"><span data-stu-id="d5fcc-106">IVMDisplay::SetDimensions method</span></span>

<span data-ttu-id="d5fcc-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d5fcc-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d5fcc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d5fcc-109">Définit, en pixels, la hauteur et la largeur de l’affichage de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-109">Sets the height and width of the virtual machine's (VM's) display, in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5fcc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5fcc-110">Syntax</span></span>


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a><span data-ttu-id="d5fcc-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5fcc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5fcc-112">*displayPixelWidth* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5fcc-112">*displayPixelWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5fcc-113">Largeur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-113">The width, in pixels.</span></span> <span data-ttu-id="d5fcc-114">La valeur doit être comprise entre les valeurs 640 et 2048.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-114">The value must be between the values of 640 and 2048.</span></span> <span data-ttu-id="d5fcc-115">Si la valeur n’est pas divisible par 8, elle sera réduite au multiple de 8 inférieur suivant.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-115">If the value is not evenly divisible by 8, then it will be reduced to the next lower multiple of 8.</span></span>

</dd> <dt>

<span data-ttu-id="d5fcc-116">*displayPixelHeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5fcc-116">*displayPixelHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5fcc-117">Hauteur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-117">The height, in pixels.</span></span> <span data-ttu-id="d5fcc-118">La valeur doit être comprise entre les valeurs 480 et 1920.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-118">The value must be between the values of 480 and 1920.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5fcc-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5fcc-119">Return value</span></span>

<span data-ttu-id="d5fcc-120">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-120">This method can return one of these values.</span></span>



| <span data-ttu-id="d5fcc-121">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d5fcc-121">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="d5fcc-122">Description</span><span class="sxs-lookup"><span data-stu-id="d5fcc-122">Description</span></span>                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d5fcc-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d5fcc-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="d5fcc-124">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-124">The operation was successful.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="d5fcc-125"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="d5fcc-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="d5fcc-126">Le paramètre *displayPixelWidth* n’est pas divisible par 8, ou le paramètre *displayPixelWidth* ou *displayPixelHeight* est en dehors des valeurs minimales autorisées (640x480) ou 2048x1920).</span><span class="sxs-lookup"><span data-stu-id="d5fcc-126">The *displayPixelWidth* parameter is not evenly divisible by 8 or the *displayPixelWidth* or *displayPixelHeight* parameter is outside of the allowed minimum (640x480) or maximum 2048x1920) values.</span></span><br/> |
| <dl> <span data-ttu-id="d5fcc-127"><dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="d5fcc-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="d5fcc-128">La modification de la résolution ne s’est pas terminée en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-128">The resolution change did not finish in a timely manner.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="d5fcc-129"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d5fcc-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="d5fcc-130">L’ordinateur virtuel doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-130">The virtual machine must be running for this operation.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="d5fcc-131"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="d5fcc-131"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="d5fcc-132">L’ordinateur virtuel n’est pas valide ou n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-132">The virtual machine is not valid or is not currently running.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="d5fcc-133"><dt>**Ordinateur virtuel \_ E \_ aucun \_**</dt> <dt>0xA0040850</dt> d’affichage</span><span class="sxs-lookup"><span data-stu-id="d5fcc-133"><dt>**VM\_E\_NO\_DISPLAY**</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="d5fcc-134">Impossible de trouver un affichage valide pour la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-134">Unable to locate a valid display for the VM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="d5fcc-135"><dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="d5fcc-135"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="d5fcc-136">La version des composants d’intégration installés dans le système d’exploitation invité ne prend pas en charge cette opération.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-136">The version of the integration components installed in the guest operating system does not support this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="d5fcc-137"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d5fcc-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="d5fcc-138">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-138">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="d5fcc-139">Notes</span><span class="sxs-lookup"><span data-stu-id="d5fcc-139">Remarks</span></span>

<span data-ttu-id="d5fcc-140">La taille minimale de l’affichage de l’ordinateur virtuel est de 640 x 480 pixels.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-140">The minimum size of the virtual machine's display is 640 x 480 pixels.</span></span> <span data-ttu-id="d5fcc-141">La taille maximale est de 2048 x 1920.</span><span class="sxs-lookup"><span data-stu-id="d5fcc-141">The maximum size is 2048 x 1920.</span></span> <span data-ttu-id="d5fcc-142">Toute tentative de définition de la taille d’affichage sur des valeurs en dehors de ces limites, ou sur une largeur qui n’est pas divisible par 8, entraîne le renvoi d’une erreur **E \_ INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="d5fcc-142">Attempts to set the display size to values outside these limits, or to any width not evenly divisible by 8, will result in an **E\_INVALIDARG** error being returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5fcc-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5fcc-143">Requirements</span></span>



| <span data-ttu-id="d5fcc-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5fcc-144">Requirement</span></span> | <span data-ttu-id="d5fcc-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5fcc-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5fcc-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5fcc-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d5fcc-147">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5fcc-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d5fcc-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5fcc-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d5fcc-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5fcc-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d5fcc-150">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d5fcc-150">End of client support</span></span><br/>    | <span data-ttu-id="d5fcc-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5fcc-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d5fcc-152">Produit</span><span class="sxs-lookup"><span data-stu-id="d5fcc-152">Product</span></span><br/>                  | <span data-ttu-id="d5fcc-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d5fcc-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d5fcc-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5fcc-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5fcc-155"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5fcc-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d5fcc-156">IID</span><span class="sxs-lookup"><span data-stu-id="d5fcc-156">IID</span></span><br/>                      | <span data-ttu-id="d5fcc-157">IID \_ IVMDisplay est défini en tant que 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="d5fcc-157">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d5fcc-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5fcc-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5fcc-159">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="d5fcc-159">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

