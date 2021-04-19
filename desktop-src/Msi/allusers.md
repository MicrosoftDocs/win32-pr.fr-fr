---
Description: La propriété ALLUSERS configure le contexte d’installation du package.
ms.assetid: 942e7764-a80f-4880-9559-72174f1827f7
title: ALLUSERS, propriété
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: f4e490216a16b6ef36cdb90efebbbf24a7b1b9cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543892"
---
# <a name="allusers-property"></a><span data-ttu-id="db062-103">ALLUSERS, propriété</span><span class="sxs-lookup"><span data-stu-id="db062-103">ALLUSERS property</span></span>

<span data-ttu-id="db062-104">La propriété **ALLUSERS** configure le contexte d’installation du package.</span><span class="sxs-lookup"><span data-stu-id="db062-104">The **ALLUSERS** property configures the installation context of the package.</span></span> <span data-ttu-id="db062-105">L’Windows Installer effectue une installation par utilisateur ou une installation par ordinateur en fonction des privilèges d’accès de l’utilisateur, si des privilèges élevés sont requis pour installer l’application, la valeur de la propriété **ALLUSERS** , la valeur de la propriété [**MSIINSTALLPERUSER**](msiinstallperuser.md) et la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="db062-105">The Windows Installer performs a per-user installation or per-machine installation depending on the access privileges of the user, whether elevated privileges are required to install the application, the value of the **ALLUSERS** property, the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property and the version of the operating system.</span></span>

<span data-ttu-id="db062-106">La valeur de la propriété **ALLUSERS** , au moment de l’installation, détermine le [contexte d’installation](installation-context.md).</span><span class="sxs-lookup"><span data-stu-id="db062-106">The value of the **ALLUSERS** property, at installation time, determines the [installation context](installation-context.md).</span></span>

-   <span data-ttu-id="db062-107">La valeur 1 de la propriété **ALLUSERS** spécifie le contexte d’installation par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="db062-107">An **ALLUSERS** property value of 1 specifies the per-machine installation context.</span></span>
-   <span data-ttu-id="db062-108">Une valeur de propriété **ALLUSERS** d’une chaîne vide ("") spécifie le contexte d’installation par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db062-108">An **ALLUSERS** property value of an empty string ("") specifies the per-user installation context.</span></span>
-   <span data-ttu-id="db062-109">Si la valeur de la propriété **ALLUSERS** est définie sur 2, la Windows Installer rétablit toujours la valeur 1 pour la propriété **ALLUSERS** et effectue une installation par ordinateur ou réinitialise la valeur de la propriété **ALLUSERS** sur une chaîne vide ("") et effectue une installation par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db062-109">If the value of the **ALLUSERS** property is set to 2, the Windows Installer always resets the value of the **ALLUSERS** property to 1 and performs a per-machine installation or it resets the value of the **ALLUSERS** property to an empty string ("") and performs a per-user installation.</span></span> <span data-ttu-id="db062-110">La valeur ALLUSERS = 2 permet au système de réinitialiser la valeur de **ALLUSERS** et le contexte d’installation, en fonction des privilèges de l’utilisateur et de la version de Windows.</span><span class="sxs-lookup"><span data-stu-id="db062-110">The value ALLUSERS=2 enables the system to reset the value of **ALLUSERS**, and the installation context, dependent upon the user's privileges and the version of Windows.</span></span>

    <span data-ttu-id="db062-111">**Windows 7 :** Affectez à la propriété **ALLUSERS** la valeur 2 pour utiliser la propriété [**MSIINSTALLPERUSER**](msiinstallperuser.md) afin de spécifier le contexte d’installation.</span><span class="sxs-lookup"><span data-stu-id="db062-111">**Windows 7:** Set the **ALLUSERS** property to 2 to use the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property to specify the installation context.</span></span> <span data-ttu-id="db062-112">Définissez la propriété **MSIINSTALLPERUSER** sur une chaîne vide ("") pour une installation par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="db062-112">Set the **MSIINSTALLPERUSER** property to an empty string ("") for a per-machine installation.</span></span> <span data-ttu-id="db062-113">Affectez la valeur 1 à la propriété **MSIINSTALLPERUSER** pour une installation par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db062-113">Set the **MSIINSTALLPERUSER** property to 1 for a per-user installation.</span></span> <span data-ttu-id="db062-114">Si le package a été écrit conformément aux instructions de développement décrites dans [création de package unique](single-package-authoring.md), les utilisateurs disposant d’un accès utilisateur peuvent installer dans le contexte par utilisateur sans avoir à fournir des informations d’identification UAC.</span><span class="sxs-lookup"><span data-stu-id="db062-114">If the package has been written following the development guidelines described in [Single Package Authoring](single-package-authoring.md), users having user access can install into the per-user context without having to provide UAC credentials.</span></span> <span data-ttu-id="db062-115">Si l’utilisateur dispose de privilèges d’accès d’utilisateur, le programme d’installation effectue une installation par ordinateur uniquement si les informations d’identification d’administrateur sont fournies à la boîte de dialogue UAC.</span><span class="sxs-lookup"><span data-stu-id="db062-115">If the user has user access privileges, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span>

    <span data-ttu-id="db062-116">**Windows Vista :** Affectez à la propriété **ALLUSERS** la valeur 2 et Windows Installer est conforme au [*contrôle de compte d’utilisateur*](u-gly.md) (UAC).</span><span class="sxs-lookup"><span data-stu-id="db062-116">**Windows Vista:** Set the **ALLUSERS** property to 2 and Windows Installer complies with [*User Account Control*](u-gly.md) (UAC).</span></span> <span data-ttu-id="db062-117">Si l’utilisateur dispose de privilèges d’accès utilisateur et ALLUSERS = 2, le programme d’installation effectue une installation par ordinateur uniquement si les informations d’identification d’administrateur sont fournies à la boîte de dialogue UAC.</span><span class="sxs-lookup"><span data-stu-id="db062-117">If the user has user access privileges, and ALLUSERS=2, the installer performs a per-machine installation only if Admin credentials are provided to the UAC dialog box.</span></span> <span data-ttu-id="db062-118">Si le contrôle de compte d’utilisateur est activé et que les informations d’identification d’administrateur appropriées ne sont pas fournies, l’installation échoue avec une erreur indiquant que des privilèges d’administrateur sont nécessaires.</span><span class="sxs-lookup"><span data-stu-id="db062-118">If UAC is enabled and the correct Admin credentials are not provided, the installation fails with an error stating that administrator privileges are required.</span></span> <span data-ttu-id="db062-119">Si le contrôle de compte d’utilisateur est désactivé par la clé de Registre, la stratégie de groupe ou le panneau de configuration, la boîte de dialogue contrôle de compte d’utilisateur ne s’affiche pas et l’installation échoue avec une erreur indiquant que des privilèges d’administrateur sont requis.</span><span class="sxs-lookup"><span data-stu-id="db062-119">If UAC is disabled by the registry key, group policy, or the control panel, the UAC dialog box is not displayed and the installation fails with an error stating that administrator privileges are required.</span></span>

    <span data-ttu-id="db062-120">**Windows XP :** Affectez à la propriété **ALLUSERS** la valeur 2 et Windows Installer effectue une installation par utilisateur si l’utilisateur dispose de privilèges d’accès utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db062-120">**Windows XP:** Set the **ALLUSERS** property to 2 and Windows Installer performs a per-user installation if the user has user access privileges.</span></span>

-   <span data-ttu-id="db062-121">Si la valeur de la propriété **ALLUSERS** n’est pas égale à 2, le Windows Installer ignore la valeur de la propriété [**MSIINSTALLPERUSER**](msiinstallperuser.md) .</span><span class="sxs-lookup"><span data-stu-id="db062-121">If the value of the **ALLUSERS** property does not equal 2, the Windows Installer ignores the value of the [**MSIINSTALLPERUSER**](msiinstallperuser.md) property.</span></span>

## <a name="example"></a><span data-ttu-id="db062-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="db062-122">Example</span></span>

```xml
  <!-- Disallow user from installing for all users -->
    <Property Id="ALLUSERS" Secure="yes"/>
    <Condition Message="Setting the ALLUSERS property is not allowed because [ProductName] is a per-user application. Setup will now exit.">
      NOT ALLUSERS
    </Condition>
```

<span data-ttu-id="db062-123">Exemple tiré d' [exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="db062-123">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/DesktopToasts/CPP/Product.wxs) on GitHub.</span></span>

## <a name="default-value"></a><span data-ttu-id="db062-124">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="db062-124">Default Value</span></span>

<span data-ttu-id="db062-125">Le contexte d’installation par défaut recommandé est par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db062-125">The recommended default installation context is per-user.</span></span> <span data-ttu-id="db062-126">Si **ALLUSERS** n’est pas défini, le programme d’installation effectue une installation par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db062-126">If **ALLUSERS** is not set, the installer does a per-user installation.</span></span> <span data-ttu-id="db062-127">Vous pouvez vous assurer que la propriété **ALLUSERS** n’a pas été définie en définissant sa valeur sur une chaîne vide (""), ALLUSERS = "".</span><span class="sxs-lookup"><span data-stu-id="db062-127">You can ensure the **ALLUSERS** property has not been set by setting its value to an empty string (""), ALLUSERS="".</span></span>

## <a name="remarks"></a><span data-ttu-id="db062-128">Notes</span><span class="sxs-lookup"><span data-stu-id="db062-128">Remarks</span></span>

<span data-ttu-id="db062-129">Le [contexte d’installation](installation-context.md) détermine les valeurs des propriétés [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)et [**CommonFiles64Folder**](commonfiles64folder.md) .</span><span class="sxs-lookup"><span data-stu-id="db062-129">The [installation context](installation-context.md) determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="db062-130">Le contexte d’installation détermine les parties du registre où les entrées de la [table du Registre](registry-table.md) et de la [table RemoveRegistry](removeregistry-table.md), avec-1 dans la colonne racine, sont écrites ou supprimées.</span><span class="sxs-lookup"><span data-stu-id="db062-130">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="db062-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db062-131">Requirements</span></span>



| <span data-ttu-id="db062-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db062-132">Requirement</span></span> | <span data-ttu-id="db062-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="db062-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db062-134">Version</span><span class="sxs-lookup"><span data-stu-id="db062-134">Version</span></span><br/> | <span data-ttu-id="db062-135">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="db062-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="db062-136">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="db062-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="db062-137">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="db062-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="db062-138">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="db062-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db062-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db062-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db062-140">Propriétés</span><span class="sxs-lookup"><span data-stu-id="db062-140">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="db062-141">**MSIINSTALLPERUSER**</span><span class="sxs-lookup"><span data-stu-id="db062-141">**MSIINSTALLPERUSER**</span></span>](msiinstallperuser.md)
</dt> <dt>

[<span data-ttu-id="db062-142">Contexte d’installation</span><span class="sxs-lookup"><span data-stu-id="db062-142">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="db062-143">Création d’un package unique</span><span class="sxs-lookup"><span data-stu-id="db062-143">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




