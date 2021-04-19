---
description: La méthode CreateAdvertiseScript de l’objet installer génère un script de publication.
ms.assetid: 32a331e5-d291-49cd-ab0e-7d0e4d72a95b
title: 'Installer :: CreateAdvertiseScript, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateAdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9ec4b18eee376e7bde4824a497ea14b503045f43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540717"
---
# <a name="installercreateadvertisescript-method"></a><span data-ttu-id="c015e-103">Installer :: CreateAdvertiseScript, méthode</span><span class="sxs-lookup"><span data-stu-id="c015e-103">Installer::CreateAdvertiseScript method</span></span>

<span data-ttu-id="c015e-104">La méthode **CreateAdvertiseScript** de l’objet [**installer**](installer-object.md) génère un script de publication.</span><span class="sxs-lookup"><span data-stu-id="c015e-104">The **CreateAdvertiseScript** method of the [**Installer**](installer-object.md) object generates an advertise script.</span></span>

## <a name="syntax"></a><span data-ttu-id="c015e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c015e-105">Syntax</span></span>


```JScript
.CreateAdvertiseScript(
  packagePath,
  scriptFilePath,
  transforms,
  language,
  platform,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="c015e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c015e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c015e-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="c015e-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="c015e-108">Chemin d’accès complet au package de Windows Installer (. msi) à publier.</span><span class="sxs-lookup"><span data-stu-id="c015e-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="c015e-109">*scriptFilePath*</span><span class="sxs-lookup"><span data-stu-id="c015e-109">*scriptFilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="c015e-110">Chemin d’accès complet au fichier de script à créer avec les informations publiées.</span><span class="sxs-lookup"><span data-stu-id="c015e-110">The full path to the script file to be created with the advertised information.</span></span>

</dd> <dt>

<span data-ttu-id="c015e-111">*transformations*</span><span class="sxs-lookup"><span data-stu-id="c015e-111">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="c015e-112">Liste des transformations à appliquer au produit.</span><span class="sxs-lookup"><span data-stu-id="c015e-112">The list of transforms to apply to the product.</span></span> <span data-ttu-id="c015e-113">Les transformations de la liste sont délimitées par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="c015e-113">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="c015e-114">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="c015e-114">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="c015e-115">*language*</span><span class="sxs-lookup"><span data-stu-id="c015e-115">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="c015e-116">Langue du package d’installation à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c015e-116">The language of the installation package to use.</span></span> <span data-ttu-id="c015e-117">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="c015e-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="c015e-118">*platform*</span><span class="sxs-lookup"><span data-stu-id="c015e-118">*platform*</span></span> 
</dt> <dd>

<span data-ttu-id="c015e-119">Ce paramètre spécifie la plateforme pour laquelle le programme d’installation doit créer le script.</span><span class="sxs-lookup"><span data-stu-id="c015e-119">This parameter specifies for which platform the installer should create the script.</span></span> <span data-ttu-id="c015e-120">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c015e-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c015e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c015e-121">Value</span></span>                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="c015e-122">Signification</span><span class="sxs-lookup"><span data-stu-id="c015e-122">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="msiAdvertiseCurrentPlatform"></span><span id="msiadvertisecurrentplatform"></span><span id="MSIADVERTISECURRENTPLATFORM"></span><dl> <span data-ttu-id="c015e-123"><dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c015e-123"><dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="c015e-124">Crée un script pour la plateforme actuelle.</span><span class="sxs-lookup"><span data-stu-id="c015e-124">Creates a script for the current platform.</span></span><br/>  |
| <span id="msiAdvertiseX86Platform"></span><span id="msiadvertisex86platform"></span><span id="MSIADVERTISEX86PLATFORM"></span><dl> <span data-ttu-id="c015e-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c015e-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="c015e-126">Crée un script pour la plateforme x86.</span><span class="sxs-lookup"><span data-stu-id="c015e-126">Creates a script for the x86 platform.</span></span><br/>      |
| <span id="msiAdvertiseIA64Platform"></span><span id="msiadvertiseia64platform"></span><span id="MSIADVERTISEIA64PLATFORM"></span><dl> <span data-ttu-id="c015e-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c015e-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="c015e-128">Crée un script pour les systèmes Itanium.</span><span class="sxs-lookup"><span data-stu-id="c015e-128">Creates a script for Itanium-based systems.</span></span><br/> |
| <span id="msiAdvertiseX64Platform"></span><span id="msiadvertisex64platform"></span><span id="MSIADVERTISEX64PLATFORM"></span><dl> <span data-ttu-id="c015e-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c015e-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="c015e-130">Crée un script pour la plateforme x64.</span><span class="sxs-lookup"><span data-stu-id="c015e-130">Creates a script for the x64 platform.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="c015e-131">*options*</span><span class="sxs-lookup"><span data-stu-id="c015e-131">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="c015e-132">Options de publication.</span><span class="sxs-lookup"><span data-stu-id="c015e-132">Advertisement options.</span></span> <span data-ttu-id="c015e-133">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="c015e-133">This parameter is optional.</span></span> <span data-ttu-id="c015e-134">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c015e-134">This parameter can be one of the following values.</span></span> <span data-ttu-id="c015e-135">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="c015e-135">This parameter is optional.</span></span>



| <span data-ttu-id="c015e-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="c015e-136">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="c015e-137">Signification</span><span class="sxs-lookup"><span data-stu-id="c015e-137">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="c015e-138"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c015e-138"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="c015e-139">Publication standard</span><span class="sxs-lookup"><span data-stu-id="c015e-139">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="c015e-140"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c015e-140"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="c015e-141">Publie une nouvelle instance du produit.</span><span class="sxs-lookup"><span data-stu-id="c015e-141">Advertises a new instance of the product.</span></span> <span data-ttu-id="c015e-142">Requiert que la première transformation de la liste transformer du paramètre *transformations* soit la transformation d’instance qui modifie le code du produit.</span><span class="sxs-lookup"><span data-stu-id="c015e-142">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="c015e-143">Pour plus d’informations, consultez [installation de plusieurs instances de produits et de correctifs](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="c015e-143">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c015e-144">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c015e-144">Return value</span></span>

<span data-ttu-id="c015e-145">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c015e-145">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c015e-146">Notes</span><span class="sxs-lookup"><span data-stu-id="c015e-146">Remarks</span></span>

<span data-ttu-id="c015e-147">La méthode [**AdvertiseProduct**](installer-advertiseproduct.md) utilise la fonction [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .</span><span class="sxs-lookup"><span data-stu-id="c015e-147">The [**AdvertiseProduct**](installer-advertiseproduct.md) method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="c015e-148">Exemples</span><span class="sxs-lookup"><span data-stu-id="c015e-148">Examples</span></span>

<span data-ttu-id="c015e-149">L’exemple suivant illustre l’utilisation de la méthode **CreateAdvertiseScript** .</span><span class="sxs-lookup"><span data-stu-id="c015e-149">The following example demonstrates the use of the **CreateAdvertiseScript** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Create an advertise script for Orca
'

Installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scripts\orca.aas"
```



## <a name="requirements"></a><span data-ttu-id="c015e-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c015e-150">Requirements</span></span>



| <span data-ttu-id="c015e-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c015e-151">Requirement</span></span> | <span data-ttu-id="c015e-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="c015e-152">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c015e-153">Version</span><span class="sxs-lookup"><span data-stu-id="c015e-153">Version</span></span><br/> | <span data-ttu-id="c015e-154">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c015e-154">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c015e-155">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c015e-155">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c015e-156">Windows Installer 4,5 sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="c015e-156">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="c015e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="c015e-157">DLL</span></span><br/>     | <dl> <span data-ttu-id="c015e-158"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c015e-158"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="c015e-159">IID</span><span class="sxs-lookup"><span data-stu-id="c015e-159">IID</span></span><br/>     | <span data-ttu-id="c015e-160">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c015e-160">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="c015e-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c015e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c015e-162">**Programme d’installation**</span><span class="sxs-lookup"><span data-stu-id="c015e-162">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="c015e-163">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="c015e-163">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




