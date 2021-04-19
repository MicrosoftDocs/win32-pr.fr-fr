---
description: La méthode ProvideAssembly de l’objet installer retourne le chemin d’accès installé d’un assembly.
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: Programme d’installation ::P méthode rovideAssembly
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f81c9ab9b43b814307242cc828326b2b7e7d79fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542727"
---
# <a name="installerprovideassembly-method"></a><span data-ttu-id="d2db6-103">Programme d’installation ::P méthode rovideAssembly</span><span class="sxs-lookup"><span data-stu-id="d2db6-103">Installer::ProvideAssembly method</span></span>

<span data-ttu-id="d2db6-104">La méthode **ProvideAssembly** de l’objet [**installer**](installer-object.md) retourne le chemin d’accès installé d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="d2db6-104">The **ProvideAssembly** method of the [**Installer**](installer-object.md) object returns the installed path of an assembly.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2db6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2db6-105">Syntax</span></span>


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a><span data-ttu-id="d2db6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2db6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2db6-107">*assembly*</span><span class="sxs-lookup"><span data-stu-id="d2db6-107">*assembly*</span></span> 
</dt> <dd>

<span data-ttu-id="d2db6-108">Nom fort de l’assembly installé à interroger.</span><span class="sxs-lookup"><span data-stu-id="d2db6-108">The strong name of installed assembly that is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="d2db6-109">*appContext*</span><span class="sxs-lookup"><span data-stu-id="d2db6-109">*appContext*</span></span> 
</dt> <dd>

<span data-ttu-id="d2db6-110">Affectez la valeur null pour les assemblys globaux.</span><span class="sxs-lookup"><span data-stu-id="d2db6-110">Set to null for global assemblies.</span></span> <span data-ttu-id="d2db6-111">Pour les assemblys privés, définissez *appContext* sur le chemin d’accès complet du fichier de configuration de l’application ou sur le chemin d’accès complet du fichier exécutable de l’application dans laquelle l’assembly a été rendu privé.</span><span class="sxs-lookup"><span data-stu-id="d2db6-111">For private assemblies, set *appContext* to the full path of the application configuration file or to the full path of the executable file of the application to which the assembly has been made private.</span></span>

</dd> <dt>

<span data-ttu-id="d2db6-112">*installMode*</span><span class="sxs-lookup"><span data-stu-id="d2db6-112">*installMode*</span></span> 
</dt> <dd>

<span data-ttu-id="d2db6-113">Définit le mode d’installation.</span><span class="sxs-lookup"><span data-stu-id="d2db6-113">Defines the installation mode.</span></span> <span data-ttu-id="d2db6-114">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2db6-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="d2db6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2db6-115">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="d2db6-116">Signification</span><span class="sxs-lookup"><span data-stu-id="d2db6-116">Meaning</span></span>                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <span data-ttu-id="d2db6-117"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d2db6-117"><dt>**msiInstallModeDefault**</dt> <dt>0</dt></span></span> </dl>                                                                                                | <span data-ttu-id="d2db6-118">Fournissez le composant et effectuez toute installation nécessaire pour fournir le composant.</span><span class="sxs-lookup"><span data-stu-id="d2db6-118">Provide the component and perform any installation necessary to provide the component.</span></span> <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <span data-ttu-id="d2db6-119"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="d2db6-119"><dt>**msiInstallModeExisting**</dt> <dt>-1</dt></span></span> </dl>                                                                                           | <span data-ttu-id="d2db6-120">Fournissez le composant uniquement si la fonctionnalité existe.</span><span class="sxs-lookup"><span data-stu-id="d2db6-120">Provide the component only if the feature exists.</span></span> <span data-ttu-id="d2db6-121">Cette option permet de vérifier l’existence de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="d2db6-121">This option will verify that the assembly exists.</span></span><br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <span data-ttu-id="d2db6-122"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span><span class="sxs-lookup"><span data-stu-id="d2db6-122"><dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt></span></span> </dl>                                                                               | <span data-ttu-id="d2db6-123">Fournissez le composant uniquement si la fonctionnalité existe.</span><span class="sxs-lookup"><span data-stu-id="d2db6-123">Provide the component only if the feature exists.</span></span> <span data-ttu-id="d2db6-124">Cette option ne vérifie pas l’existence de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="d2db6-124">This option does not verify that the assembly exists.</span></span><br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <span data-ttu-id="d2db6-125"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span><span class="sxs-lookup"><span data-stu-id="d2db6-125"><dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt></span></span> </dl>                                                   | <span data-ttu-id="d2db6-126">Fournit l’assembly uniquement si l’assembly est installé en local.</span><span class="sxs-lookup"><span data-stu-id="d2db6-126">Provides the assembly only if the assembly is installed local.</span></span><br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <span data-ttu-id="d2db6-127"><dt>**Combinaison des indicateurs utilisés par [ **ReinstallFeature**](installer-reinstallfeature.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="d2db6-127"><dt>**Combination of the flags used by [**ReinstallFeature**](installer-reinstallfeature.md)**</dt></span></span> </dl> | <span data-ttu-id="d2db6-128">Appelle la méthode [**ReinstallFeature**](installer-reinstallfeature.md) pour réinstaller la fonctionnalité à l’aide de ce paramètre pour *ReinstallMode*, puis retourne le chemin d’accès de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="d2db6-128">Calls the [**ReinstallFeature**](installer-reinstallfeature.md) method to reinstall the feature using this parameter for *ReinstallMode*, and then returns the assembly path.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d2db6-129">*assemblyInfo*</span><span class="sxs-lookup"><span data-stu-id="d2db6-129">*assemblyInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="d2db6-130">Informations d’assembly et type d’assembly.</span><span class="sxs-lookup"><span data-stu-id="d2db6-130">Assembly information and assembly type.</span></span> <span data-ttu-id="d2db6-131">Définissez l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d2db6-131">Set to one of the following values.</span></span>



| <span data-ttu-id="d2db6-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2db6-132">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="d2db6-133">Signification</span><span class="sxs-lookup"><span data-stu-id="d2db6-133">Meaning</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <span data-ttu-id="d2db6-134"><dt>**msiProvideAssemblyNet**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d2db6-134"><dt>**msiProvideAssemblyNet**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="d2db6-135">Assembly .NET.</span><span class="sxs-lookup"><span data-stu-id="d2db6-135">A .NET assembly.</span></span><br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <span data-ttu-id="d2db6-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d2db6-136"><dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="d2db6-137">Assembly côte à côte Win32.</span><span class="sxs-lookup"><span data-stu-id="d2db6-137">A Win32 side-by-side assembly.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2db6-138">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2db6-138">Return value</span></span>

<span data-ttu-id="d2db6-139">Chemin d’accès à l’assembly installé.</span><span class="sxs-lookup"><span data-stu-id="d2db6-139">The path to the installed assembly.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2db6-140">Notes</span><span class="sxs-lookup"><span data-stu-id="d2db6-140">Remarks</span></span>

<span data-ttu-id="d2db6-141">La méthode **ProvideAssembly** utilise la fonction [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) .</span><span class="sxs-lookup"><span data-stu-id="d2db6-141">The **ProvideAssembly** method uses the [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya) function.</span></span>

## <a name="examples"></a><span data-ttu-id="d2db6-142">Exemples</span><span class="sxs-lookup"><span data-stu-id="d2db6-142">Examples</span></span>

<span data-ttu-id="d2db6-143">L’exemple de script suivant illustre l’utilisation de la méthode ProvideAssembly.</span><span class="sxs-lookup"><span data-stu-id="d2db6-143">The following sample script demonstrates the use of the ProvideAssembly method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
```



## <a name="requirements"></a><span data-ttu-id="d2db6-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2db6-144">Requirements</span></span>



| <span data-ttu-id="d2db6-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2db6-145">Requirement</span></span> | <span data-ttu-id="d2db6-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2db6-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2db6-147">Version</span><span class="sxs-lookup"><span data-stu-id="d2db6-147">Version</span></span><br/> | <span data-ttu-id="d2db6-148">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d2db6-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d2db6-149">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d2db6-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d2db6-150">Windows Installer 4,5 sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2db6-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="d2db6-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d2db6-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="d2db6-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2db6-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="d2db6-153">IID</span><span class="sxs-lookup"><span data-stu-id="d2db6-153">IID</span></span><br/>     | <span data-ttu-id="d2db6-154">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d2db6-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="d2db6-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2db6-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2db6-156">**Programme d’installation**</span><span class="sxs-lookup"><span data-stu-id="d2db6-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="d2db6-157">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="d2db6-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




