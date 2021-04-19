---
description: La méthode AdvertiseProduct de l’objet installer publie un package d’installation.
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: 'Installer :: AdvertiseProduct, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f8e0f92079e1eb5d2690b61acafdefb2f777b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528528"
---
# <a name="installeradvertiseproduct-method"></a><span data-ttu-id="c12ea-103">Installer :: AdvertiseProduct, méthode</span><span class="sxs-lookup"><span data-stu-id="c12ea-103">Installer::AdvertiseProduct method</span></span>

<span data-ttu-id="c12ea-104">La méthode **AdvertiseProduct** de l’objet [**installer**](installer-object.md) publie un package d’installation.</span><span class="sxs-lookup"><span data-stu-id="c12ea-104">The **AdvertiseProduct** method of the [**Installer**](installer-object.md) object advertises an installation package.</span></span>

## <a name="syntax"></a><span data-ttu-id="c12ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c12ea-105">Syntax</span></span>


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="c12ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c12ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c12ea-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="c12ea-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="c12ea-108">Chemin d’accès complet au package de Windows Installer (. msi) à publier.</span><span class="sxs-lookup"><span data-stu-id="c12ea-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="c12ea-109">*context*</span><span class="sxs-lookup"><span data-stu-id="c12ea-109">*context*</span></span> 
</dt> <dd>

<span data-ttu-id="c12ea-110">Contexte de la publication.</span><span class="sxs-lookup"><span data-stu-id="c12ea-110">The context of the advertisement.</span></span> <span data-ttu-id="c12ea-111">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c12ea-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c12ea-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="c12ea-112">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="c12ea-113">Signification</span><span class="sxs-lookup"><span data-stu-id="c12ea-113">Meaning</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <span data-ttu-id="c12ea-114"><dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c12ea-114"><dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="c12ea-115">Publie l’application pour une installation dans le [contexte d’installation](installation-context.md)par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c12ea-115">Advertises the application for an instalation in the per-machine [installation context](installation-context.md).</span></span> <span data-ttu-id="c12ea-116">Cela rend le package disponible pour l’installation par tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c12ea-116">This makes the package available for installation by all users of the computer.</span></span><br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <span data-ttu-id="c12ea-117"><dt>**msiAdvertiseProductUser**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c12ea-117"><dt>**msiAdvertiseProductUser**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="c12ea-118">Publie l’application pour une installation dans le [contexte d’installation](installation-context.md)par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c12ea-118">Advertises the application for an installation in the per-user [installation context](installation-context.md).</span></span><br/>                                                                                   |



 

</dd> <dt>

<span data-ttu-id="c12ea-119">*transformations*</span><span class="sxs-lookup"><span data-stu-id="c12ea-119">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="c12ea-120">Liste des transformations à appliquer au produit.</span><span class="sxs-lookup"><span data-stu-id="c12ea-120">The list of transforms to apply to the product.</span></span> <span data-ttu-id="c12ea-121">Les transformations de la liste sont délimitées par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="c12ea-121">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="c12ea-122">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="c12ea-122">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="c12ea-123">*language*</span><span class="sxs-lookup"><span data-stu-id="c12ea-123">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="c12ea-124">Langue du package d’installation à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c12ea-124">The language of the installation package to use.</span></span> <span data-ttu-id="c12ea-125">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="c12ea-125">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="c12ea-126">*options*</span><span class="sxs-lookup"><span data-stu-id="c12ea-126">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="c12ea-127">Options de publication.</span><span class="sxs-lookup"><span data-stu-id="c12ea-127">The advertisement options.</span></span> <span data-ttu-id="c12ea-128">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="c12ea-128">This parameter is optional.</span></span> <span data-ttu-id="c12ea-129">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c12ea-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c12ea-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="c12ea-130">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="c12ea-131">Signification</span><span class="sxs-lookup"><span data-stu-id="c12ea-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="c12ea-132"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c12ea-132"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="c12ea-133">Publication standard</span><span class="sxs-lookup"><span data-stu-id="c12ea-133">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="c12ea-134"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c12ea-134"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="c12ea-135">Publie une nouvelle instance du produit.</span><span class="sxs-lookup"><span data-stu-id="c12ea-135">Advertises a new instance of the product.</span></span> <span data-ttu-id="c12ea-136">Requiert que la première transformation de la liste transformer du paramètre *transformations* soit la transformation d’instance qui modifie le code du produit.</span><span class="sxs-lookup"><span data-stu-id="c12ea-136">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="c12ea-137">Pour plus d’informations, consultez [installation de plusieurs instances de produits et de correctifs](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="c12ea-137">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c12ea-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c12ea-138">Return value</span></span>

<span data-ttu-id="c12ea-139">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c12ea-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c12ea-140">Notes</span><span class="sxs-lookup"><span data-stu-id="c12ea-140">Remarks</span></span>

<span data-ttu-id="c12ea-141">La méthode **AdvertiseProduct** utilise la fonction [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .</span><span class="sxs-lookup"><span data-stu-id="c12ea-141">The **AdvertiseProduct** method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="c12ea-142">Exemples</span><span class="sxs-lookup"><span data-stu-id="c12ea-142">Examples</span></span>

<span data-ttu-id="c12ea-143">L’exemple suivant illustre l’utilisation de la méthode **AdvertiseProduct** .</span><span class="sxs-lookup"><span data-stu-id="c12ea-143">The following example demonstrates the use of the **AdvertiseProduct** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
```



## <a name="requirements"></a><span data-ttu-id="c12ea-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c12ea-144">Requirements</span></span>



| <span data-ttu-id="c12ea-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c12ea-145">Requirement</span></span> | <span data-ttu-id="c12ea-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="c12ea-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c12ea-147">Version</span><span class="sxs-lookup"><span data-stu-id="c12ea-147">Version</span></span><br/> | <span data-ttu-id="c12ea-148">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c12ea-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c12ea-149">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c12ea-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c12ea-150">Windows Installer 4,5 sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="c12ea-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="c12ea-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c12ea-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="c12ea-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c12ea-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="c12ea-153">IID</span><span class="sxs-lookup"><span data-stu-id="c12ea-153">IID</span></span><br/>     | <span data-ttu-id="c12ea-154">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c12ea-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="c12ea-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c12ea-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c12ea-156">**Programme d’installation**</span><span class="sxs-lookup"><span data-stu-id="c12ea-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="c12ea-157">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="c12ea-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




