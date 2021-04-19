---
description: La méthode ProvideQualifiedComponent de l’objet installer retourne le chemin d’accès complet au composant et effectue toute installation nécessaire. Si nécessaire, cette méthode vous invite à entrer la source et incrémente le nombre d’utilisations de la fonctionnalité.
ms.assetid: 4f9a5094-1556-4d86-8b51-c8c3ce1cbed4
title: Installer. ProvideQualifiedComponent, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideQualifiedComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 73c830610b49976e3625dd333c57f39e43d4be14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545933"
---
# <a name="installerprovidequalifiedcomponent-method"></a><span data-ttu-id="685b7-104">Installer. ProvideQualifiedComponent, méthode</span><span class="sxs-lookup"><span data-stu-id="685b7-104">Installer.ProvideQualifiedComponent method</span></span>

<span data-ttu-id="685b7-105">La méthode **ProvideQualifiedComponent** de l’objet [**installer**](installer-object.md) retourne le chemin d’accès complet au composant et effectue toute installation nécessaire.</span><span class="sxs-lookup"><span data-stu-id="685b7-105">The **ProvideQualifiedComponent** method of the [**Installer**](installer-object.md) object returns the full component path and performs any necessary installation.</span></span> <span data-ttu-id="685b7-106">Si nécessaire, cette méthode vous invite à entrer la source et incrémente le nombre d’utilisations de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="685b7-106">If necessary, this method prompts for the source and increments the usage count for the feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="685b7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="685b7-107">Syntax</span></span>


```JScript
Installer.ProvideQualifiedComponent(
  Category,
  Qualifier,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="685b7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="685b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="685b7-109">*Catégorie*</span><span class="sxs-lookup"><span data-stu-id="685b7-109">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="685b7-110">Spécifie l’ID de composant pour le composant demandé.</span><span class="sxs-lookup"><span data-stu-id="685b7-110">Specifies the component ID for the requested component.</span></span> <span data-ttu-id="685b7-111">Ce n’est peut-être pas le GUID du composant lui-même, mais plutôt un serveur qui fournit les fonctionnalités correctes, comme dans la colonne ComponentId de la [table PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="685b7-111">This may not be the GUID for the component itself but rather a server that provides the correct functionality, as in the ComponentId column of the [PublishComponent table](publishcomponent-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="685b7-112">*Qualificateur*</span><span class="sxs-lookup"><span data-stu-id="685b7-112">*Qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="685b7-113">Spécifie un qualificateur dans une liste de composants de publicité (à partir de la [table PublishComponent](publishcomponent-table.md)).</span><span class="sxs-lookup"><span data-stu-id="685b7-113">Specifies a qualifier into a list of advertising components (from [PublishComponent table](publishcomponent-table.md)).</span></span>

</dd> <dt>

<span data-ttu-id="685b7-114">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="685b7-114">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="685b7-115">Définit le mode d’installation.</span><span class="sxs-lookup"><span data-stu-id="685b7-115">Defines the installation mode.</span></span> <span data-ttu-id="685b7-116">Ce paramètre peut avoir l’une des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="685b7-116">This parameter can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="685b7-117">InstallMode</span><span class="sxs-lookup"><span data-stu-id="685b7-117">InstallMode</span></span>                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="685b7-118">Signification</span><span class="sxs-lookup"><span data-stu-id="685b7-118">Meaning</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="685b7-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="685b7-119"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                 | <span data-ttu-id="685b7-120">Fournit le composant, en effectuant toutes les installations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="685b7-120">Provides the component, performing any necessary installation.</span></span><br/>                                                                                                                                                           |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="685b7-121"><dt>**msiInstallModeExisting**</dt> <dt>– 1</dt></span><span class="sxs-lookup"><span data-stu-id="685b7-121"><dt>**msiInstallModeExisting**</dt> <dt>–1</dt></span></span> </dl>                                                                            | <span data-ttu-id="685b7-122">Fournit le composant uniquement si la fonctionnalité existe ; Sinon, retourne une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="685b7-122">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="685b7-123">Ce mode vérifie l’existence du fichier de clé du composant.</span><span class="sxs-lookup"><span data-stu-id="685b7-123">This mode verifies the existence of the component's key file.</span></span><br/>                                                                      |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="685b7-124"><dt>**msiInstallModeNoDetection**</dt> <dt>– 2</dt></span><span class="sxs-lookup"><span data-stu-id="685b7-124"><dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt></span></span> </dl>                                                                | <span data-ttu-id="685b7-125">Fournit le composant uniquement si la fonctionnalité existe ; Sinon, retourne une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="685b7-125">Provides the component only if the feature exists; otherwise returns an empty string.</span></span> <span data-ttu-id="685b7-126">Ce mode vérifie uniquement que le composant est inscrit, mais ne vérifie pas l’existence du fichier de clé du composant.</span><span class="sxs-lookup"><span data-stu-id="685b7-126">This mode only checks that the component is registered but does not verify the existence of the component's key file.</span></span><br/>              |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="685b7-127"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>– 3</dt></span><span class="sxs-lookup"><span data-stu-id="685b7-127"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt></span></span> </dl>                                    | <span data-ttu-id="685b7-128">Fournit le chemin d’accès du composant uniquement si la fonctionnalité existe avec un paramètre InstallState de *msiInstallStateLocal*.</span><span class="sxs-lookup"><span data-stu-id="685b7-128">Provides the component path only if the feature exists with an InstallState parameter of *msiInstallStateLocal*.</span></span> <span data-ttu-id="685b7-129">Cela vérifie l’inscription du composant, mais ne vérifie pas l’existence du fichier de clé du composant.</span><span class="sxs-lookup"><span data-stu-id="685b7-129">This checks the component's registration but does not verify the existence of the component's key file.</span></span><br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <span data-ttu-id="685b7-130"><dt>**combinaison des indicateurs msiReinstallMode**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="685b7-130"><dt>**combination of the msiReinstallMode flags**</dt> <dt> </dt></span></span> </dl> | <span data-ttu-id="685b7-131">Appelle [**ReinstallFeature**](installer-reinstallfeature.md) pour réinstaller la fonctionnalité à l’aide de ce paramètre pour le paramètre *ReinstallMode* , puis fournit le composant.</span><span class="sxs-lookup"><span data-stu-id="685b7-131">Calls [**ReinstallFeature**](installer-reinstallfeature.md) to reinstall the feature using this parameter for the *ReinstallMode* parameter, and then provides the component.</span></span><br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="685b7-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="685b7-132">Return value</span></span>

<span data-ttu-id="685b7-133">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="685b7-133">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="685b7-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="685b7-134">Requirements</span></span>



| <span data-ttu-id="685b7-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="685b7-135">Requirement</span></span> | <span data-ttu-id="685b7-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="685b7-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="685b7-137">Version</span><span class="sxs-lookup"><span data-stu-id="685b7-137">Version</span></span><br/> | <span data-ttu-id="685b7-138">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="685b7-138">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="685b7-139">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="685b7-139">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="685b7-140">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="685b7-140">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="685b7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="685b7-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="685b7-142"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="685b7-142"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="685b7-143">IID</span><span class="sxs-lookup"><span data-stu-id="685b7-143">IID</span></span><br/>     | <span data-ttu-id="685b7-144">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="685b7-144">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="685b7-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="685b7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="685b7-146">**MsiProvideQualifiedComponent**</span><span class="sxs-lookup"><span data-stu-id="685b7-146">**MsiProvideQualifiedComponent**</span></span>](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta)
</dt> </dl>

 

 




