---
title: IVMVirtualPC DefaultVMConfigurationPath, propriété (VPCCOMInterfaces. h)
description: Répertoire par défaut dans lequel rechercher les fichiers de configuration d’ordinateur virtuel disponibles.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- DefaultVMConfigurationPath propriété Virtual PC
- DefaultVMConfigurationPath, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété DefaultVMConfigurationPath
topic_type:
- apiref
api_name:
- IVMVirtualPC.DefaultVMConfigurationPath
- IVMVirtualPC.get_DefaultVMConfigurationPath
- IVMVirtualPC.put_DefaultVMConfigurationPath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e13fc2323cb15bdbeb8c42e61810a376e49b3988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742732"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a><span data-ttu-id="1d65b-106">IVMVirtualPC ::D propriété efaultVMConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="1d65b-106">IVMVirtualPC::DefaultVMConfigurationPath property</span></span>

<span data-ttu-id="1d65b-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1d65b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1d65b-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1d65b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1d65b-109">Récupère et définit le répertoire par défaut dans lequel rechercher les fichiers de configuration d’ordinateur virtuel disponibles.</span><span class="sxs-lookup"><span data-stu-id="1d65b-109">Retrieves and sets the default directory to be searched for available virtual machine configuration files.</span></span>

<span data-ttu-id="1d65b-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1d65b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d65b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d65b-111">Syntax</span></span>


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a><span data-ttu-id="1d65b-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1d65b-112">Property value</span></span>

<span data-ttu-id="1d65b-113">Spécifie le chemin d’accès au répertoire pour les fichiers de configuration d’ordinateur virtuel par défaut.</span><span class="sxs-lookup"><span data-stu-id="1d65b-113">Specifies the directory path for the default virtual machine configuration files.</span></span> <span data-ttu-id="1d65b-114">Dans la chaîne de chemin d’accès, une barre oblique inverse ( \) peut apparaître juste avant le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="1d65b-114">In the path string, a backslash (\) may appear immediately before the terminating null character.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1d65b-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="1d65b-115">Error codes</span></span>



| <span data-ttu-id="1d65b-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="1d65b-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="1d65b-117">Signification</span><span class="sxs-lookup"><span data-stu-id="1d65b-117">Meaning</span></span>                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d65b-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1d65b-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="1d65b-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="1d65b-119">The operation was successful.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="1d65b-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1d65b-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="1d65b-121">Le paramètre *ConfigurationPath* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1d65b-121">The *configurationPath* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="1d65b-122">Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="1d65b-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="1d65b-123">Le système ne peut pas trouver le répertoire spécifié par le paramètre *ConfigurationPath* .</span><span class="sxs-lookup"><span data-stu-id="1d65b-123">The system cannot find the directory specified by the *configurationPath* parameter.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="1d65b-124">Valeur <dt>HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="1d65b-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="1d65b-125">Le système ne trouve pas le chemin d’accès spécifié par le paramètre *ConfigurationPath* .</span><span class="sxs-lookup"><span data-stu-id="1d65b-125">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="1d65b-126">Valeur <dt>HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="1d65b-126"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="1d65b-127">Le paramètre *ConfigurationPath* contient un caractère non valide (l’un des éléments suivants : " \* ? <>/ \| " : ").</span><span class="sxs-lookup"><span data-stu-id="1d65b-127">The *configurationPath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                   |
| <dl> <span data-ttu-id="1d65b-128">Valeur <dt>HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="1d65b-128"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="1d65b-129">Le paramètre *ConfigurationPath* spécifie un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="1d65b-129">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="1d65b-130">Un chemin d’accès absolu est requis.</span><span class="sxs-lookup"><span data-stu-id="1d65b-130">An absolute path is required.</span></span><br/>                                          |
| <dl> <span data-ttu-id="1d65b-131">Valeur <dt>HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="1d65b-131"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="1d65b-132">Le chemin d’accès spécifié par le paramètre *ConfigurationPath* est trop long.</span><span class="sxs-lookup"><span data-stu-id="1d65b-132">The path specified by the *configurationPath* parameter is too long.</span></span> <span data-ttu-id="1d65b-133">La longueur du chemin d’accès doit être inférieure à la longueur **maximale \_** (260) caractères.</span><span class="sxs-lookup"><span data-stu-id="1d65b-133">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="1d65b-134"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1d65b-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="1d65b-135">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="1d65b-135">An unexpected error has occurred.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="1d65b-136"><dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="1d65b-136"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="1d65b-137">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="1d65b-137">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                          |



## <a name="remarks"></a><span data-ttu-id="1d65b-138">Notes</span><span class="sxs-lookup"><span data-stu-id="1d65b-138">Remarks</span></span>

<span data-ttu-id="1d65b-139">Par défaut, cette valeur de propriété est définie sur le répertoire suivant : « % LocalAppData% \\ Microsoft \\ Windows Virtual PC \\ machines virtuelles \\ ».</span><span class="sxs-lookup"><span data-stu-id="1d65b-139">By default, this property value is set to the following directory: "%LocalAppData%\\Microsoft\\Windows Virtual PC\\Virtual Machines\\".</span></span>

## <a name="requirements"></a><span data-ttu-id="1d65b-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d65b-140">Requirements</span></span>



| <span data-ttu-id="1d65b-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d65b-141">Requirement</span></span> | <span data-ttu-id="1d65b-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d65b-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d65b-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d65b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1d65b-144">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d65b-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1d65b-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d65b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1d65b-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d65b-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1d65b-147">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1d65b-147">End of client support</span></span><br/>    | <span data-ttu-id="1d65b-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1d65b-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1d65b-149">Produit</span><span class="sxs-lookup"><span data-stu-id="1d65b-149">Product</span></span><br/>                  | <span data-ttu-id="1d65b-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1d65b-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1d65b-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d65b-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d65b-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d65b-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1d65b-153">IID</span><span class="sxs-lookup"><span data-stu-id="1d65b-153">IID</span></span><br/>                      | <span data-ttu-id="1d65b-154">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="1d65b-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="1d65b-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d65b-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d65b-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="1d65b-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

