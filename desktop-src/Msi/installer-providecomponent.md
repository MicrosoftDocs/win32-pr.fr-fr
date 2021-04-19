---
description: La méthode ProvideComponent de l’objet installer retourne le chemin d’accès complet au composant et effectue toute installation nécessaire.
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: Installer. ProvideComponent, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e383c532d496ed217bdb7743b8171d732d61b2d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537748"
---
# <a name="installerprovidecomponent-method"></a><span data-ttu-id="6ab92-103">Installer. ProvideComponent, méthode</span><span class="sxs-lookup"><span data-stu-id="6ab92-103">Installer.ProvideComponent method</span></span>

<span data-ttu-id="6ab92-104">La méthode **ProvideComponent** de l’objet [**installer**](installer-object.md) retourne le chemin d’accès complet au composant et effectue toute installation nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6ab92-104">The **ProvideComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="6ab92-105">Si nécessaire, la méthode **ProvideComponent** de l’objet [**installer**](installer-object.md) demande la source et incrémente le nombre d’utilisations de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6ab92-105">If necessary, the **ProvideComponent** method of the [**Installer**](installer-object.md) object prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ab92-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ab92-106">Syntax</span></span>


```JScript
Installer.ProvideComponent(
  Product,
  Feature,
  Component,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="6ab92-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ab92-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ab92-108">*Produit*</span><span class="sxs-lookup"><span data-stu-id="6ab92-108">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="6ab92-109">Spécifie le code de produit du produit.</span><span class="sxs-lookup"><span data-stu-id="6ab92-109">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="6ab92-110">*Fonctionnalité*</span><span class="sxs-lookup"><span data-stu-id="6ab92-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="6ab92-111">Spécifie l’ID de fonctionnalité de la fonctionnalité qui contient le composant.</span><span class="sxs-lookup"><span data-stu-id="6ab92-111">Specifies the feature ID of the feature containing the component.</span></span>

</dd> <dt>

<span data-ttu-id="6ab92-112">*Composant*</span><span class="sxs-lookup"><span data-stu-id="6ab92-112">*Component*</span></span> 
</dt> <dd>

<span data-ttu-id="6ab92-113">Spécifie le code du composant.</span><span class="sxs-lookup"><span data-stu-id="6ab92-113">Specifies the component code.</span></span>

</dd> <dt>

<span data-ttu-id="6ab92-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="6ab92-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="6ab92-115">Définit le mode d’installation.</span><span class="sxs-lookup"><span data-stu-id="6ab92-115">Defines the installation mode.</span></span> <span data-ttu-id="6ab92-116">Ce paramètre peut avoir l’une des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6ab92-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="6ab92-117">Nom</span><span class="sxs-lookup"><span data-stu-id="6ab92-117">Name</span></span>                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="6ab92-118">Signification</span><span class="sxs-lookup"><span data-stu-id="6ab92-118">Meaning</span></span>                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="6ab92-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6ab92-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                | <span data-ttu-id="6ab92-120">Fournit le chemin d’accès du composant, en effectuant n’importe quelle installation, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6ab92-120">Provides the component path, performing any installation, if necessary.</span></span><br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="6ab92-121"><dt>**msiInstallModeExisting**</dt> <dt>– 1</dt></span><span class="sxs-lookup"><span data-stu-id="6ab92-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                           | <span data-ttu-id="6ab92-122">Fournit le chemin d’accès du composant uniquement si la fonctionnalité existe ; Sinon, retourne une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="6ab92-122">Provides the component path only if the feature exists; otherwise, returns an empty string.</span></span> <span data-ttu-id="6ab92-123">Ce mode vérifie l’existence du fichier de clé du composant.</span><span class="sxs-lookup"><span data-stu-id="6ab92-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="6ab92-124"><dt>**msiInstallModeNoDetection**</dt> <dt>– 2</dt></span><span class="sxs-lookup"><span data-stu-id="6ab92-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                               | <span data-ttu-id="6ab92-125">Fournit le chemin d’accès du composant uniquement si la fonctionnalité existe.</span><span class="sxs-lookup"><span data-stu-id="6ab92-125">Provides the component path only if the feature exists.</span></span> <span data-ttu-id="6ab92-126">Sinon, retourne une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="6ab92-126">Otherwise, returns an empty string.</span></span> <span data-ttu-id="6ab92-127">Ce mode vérifie l’inscription du composant, mais ne vérifie pas l’existence du fichier de clé du composant.</span><span class="sxs-lookup"><span data-stu-id="6ab92-127">This mode checks the component's registration but does not verify the existence of the component's key file.</span></span><br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="6ab92-128"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>– 3</dt></span><span class="sxs-lookup"><span data-stu-id="6ab92-128"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                   | <span data-ttu-id="6ab92-129">Fournit le chemin d’accès du composant uniquement si la fonctionnalité existe avec un paramètre InstallState de *msiInstallStateLocal*.</span><span class="sxs-lookup"><span data-stu-id="6ab92-129">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="6ab92-130">Cela vérifie l’inscription du composant, mais ne vérifie pas l’existence du fichier de clé du composant.</span><span class="sxs-lookup"><span data-stu-id="6ab92-130">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="6ab92-131"><dt>**combinaison des indicateurs msiReinstallMode**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="6ab92-131"><dt>**combination of the msiReinstallMode flags**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="6ab92-132">Appelle [**ReinstallFeature**](installer-reinstallfeature.md) pour réinstaller la fonctionnalité à l’aide de ce paramètre pour le paramètre *ReinstallMode* , puis fournit le composant.</span><span class="sxs-lookup"><span data-stu-id="6ab92-132">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ab92-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6ab92-133">Return value</span></span>

<span data-ttu-id="6ab92-134">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6ab92-134">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ab92-135">Notes</span><span class="sxs-lookup"><span data-stu-id="6ab92-135">Remarks</span></span>

<span data-ttu-id="6ab92-136">La méthode **ProvideComponent** combine les fonctionnalités de [**UseFeature**](installer-usefeature.md), [**ConfigureFeature**](installer-configurefeature.md)et [**ComponentPath**](installer-componentpath.md).</span><span class="sxs-lookup"><span data-stu-id="6ab92-136">The **ProvideComponent** method combines the functionality of [**UseFeature**](installer-usefeature.md), [**ConfigureFeature**](installer-configurefeature.md), and [**ComponentPath**](installer-componentpath.md).</span></span> <span data-ttu-id="6ab92-137">La méthode **ProvideComponent** simplifie la séquence d’appel, mais incrémente également le nombre d’utilisations et doit être utilisée avec précaution afin d’éviter des nombres d’utilisations inexacts.</span><span class="sxs-lookup"><span data-stu-id="6ab92-137">The **ProvideComponent** method simplifies the calling sequence, but it also increments the usage count and should be used with caution to prevent inaccurate usage counts.</span></span> <span data-ttu-id="6ab92-138">La méthode **ProvideComponent** offre également moins de flexibilité qu’une série d’appels individuels aux méthodes et propriétés mentionnées précédemment.</span><span class="sxs-lookup"><span data-stu-id="6ab92-138">The **ProvideComponent** method also provides less flexibility than a series of individual calls to the methods and properties previously mentioned.</span></span>

<span data-ttu-id="6ab92-139">Si l’application est en cours de récupération à la suite d’une situation inattendue, l’application a probablement déjà appelé [**UseFeature**](installer-usefeature.md) et incrémenté le nombre d’utilisations.</span><span class="sxs-lookup"><span data-stu-id="6ab92-139">If the application is recovering from an unexpected situation, the application has probably already called [**UseFeature**](installer-usefeature.md) and incremented the usage count.</span></span> <span data-ttu-id="6ab92-140">Dans ce cas, l’application doit éviter d’incrémenter le nombre d’utilisations en appelant la méthode [**ConfigureFeature**](installer-configurefeature.md) au lieu de la méthode **ProvideComponent** .</span><span class="sxs-lookup"><span data-stu-id="6ab92-140">In this case, the application should avoid incrementing the usage count by calling the [**ConfigureFeature**](installer-configurefeature.md) method instead of the **ProvideComponent** method.</span></span>

<span data-ttu-id="6ab92-141">L’option msiInstallModeExisting ne peut pas être utilisée en association avec les indicateurs msiReinstallMode.</span><span class="sxs-lookup"><span data-stu-id="6ab92-141">The msiInstallModeExisting option cannot be used in combination with msiReinstallMode flags.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ab92-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ab92-142">Requirements</span></span>



| <span data-ttu-id="6ab92-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ab92-143">Requirement</span></span> | <span data-ttu-id="6ab92-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ab92-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab92-145">Version</span><span class="sxs-lookup"><span data-stu-id="6ab92-145">Version</span></span><br/> | <span data-ttu-id="6ab92-146">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6ab92-146">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6ab92-147">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6ab92-147">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6ab92-148">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="6ab92-148">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="6ab92-149">DLL</span><span class="sxs-lookup"><span data-stu-id="6ab92-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="6ab92-150"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ab92-150"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="6ab92-151">IID</span><span class="sxs-lookup"><span data-stu-id="6ab92-151">IID</span></span><br/>     | <span data-ttu-id="6ab92-152">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6ab92-152">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="6ab92-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ab92-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ab92-154">**MsiProvideComponent**</span><span class="sxs-lookup"><span data-stu-id="6ab92-154">**MsiProvideComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




