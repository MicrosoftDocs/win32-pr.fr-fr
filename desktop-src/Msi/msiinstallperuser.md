---
description: Les propriétés MSIINSTALLPERUSER et ALLUSERS peuvent être définies par l’utilisateur au moment de l’installation, par le biais de l’interface utilisateur ou sur une ligne de commande, pour demander que le Windows Installer installer un package à double usage pour l’utilisateur actuel ou tous les utilisateurs de l’ordinateur.
ms.assetid: 17eb24e4-8464-4724-9768-4b58446ee4bc
title: Propriété MSIINSTALLPERUSER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3fa54026c859b5f4f610fd54aec2df3ca518ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522778"
---
# <a name="msiinstallperuser-property"></a><span data-ttu-id="fd36c-103">Propriété MSIINSTALLPERUSER</span><span class="sxs-lookup"><span data-stu-id="fd36c-103">MSIINSTALLPERUSER property</span></span>

<span data-ttu-id="fd36c-104">Les propriétés **MSIINSTALLPERUSER** et [**ALLUSERS**](allusers.md) peuvent être définies par l’utilisateur au moment de l’installation, par le biais de l’interface utilisateur ou sur une ligne de commande, pour demander que le Windows Installer installer un package à double usage pour l’utilisateur actuel ou tous les utilisateurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fd36c-104">The **MSIINSTALLPERUSER** and the [**ALLUSERS**](allusers.md) properties can be set by the user at installation time, through the user interface or on a command line, to request that the Windows Installer install a dual-purpose package for the current user or all users of the computer.</span></span> <span data-ttu-id="fd36c-105">Pour utiliser la propriété **MSIINSTALLPERUSER** , la valeur de la propriété [**ALLUSERS**](allusers.md) doit être 2 et le package doit avoir été créé pour pouvoir être installé dans le contexte par utilisateur ou par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fd36c-105">To use the **MSIINSTALLPERUSER** property, the value of the [**ALLUSERS**](allusers.md) property must be 2 and the package has to have been authored to be capable of installation into either the per-user or a per-machine context.</span></span> <span data-ttu-id="fd36c-106">Pour plus d’informations sur la création d’un package à double usage, consultez [création de package unique](single-package-authoring.md).</span><span class="sxs-lookup"><span data-stu-id="fd36c-106">For information about authoring a dual-purpose package, see [Single Package Authoring](single-package-authoring.md).</span></span> <span data-ttu-id="fd36c-107">Si la valeur de la propriété **ALLUSERS** n’est pas égale à 2, la valeur de la propriété **MSIINSTALLPERUSER** est ignorée et n’a aucun effet sur l’installation.</span><span class="sxs-lookup"><span data-stu-id="fd36c-107">If the value of the **ALLUSERS** property does not equal 2, the value of the **MSIINSTALLPERUSER** property is ignored and has no effect on the installation.</span></span> <span data-ttu-id="fd36c-108">La valeur de la propriété **MSIINSTALLPERUSER** est ignorée lors de l’installation du package à l’aide de Windows Installer 4,5 ou version antérieure.</span><span class="sxs-lookup"><span data-stu-id="fd36c-108">The value of **MSIINSTALLPERUSER** property is ignored when installing the package using Windows Installer 4.5 or earlier.</span></span>

<span data-ttu-id="fd36c-109">Pour demander que le Windows Installer installer le package à double usage dans le [contexte d’installation](installation-context.md)par ordinateur, l’utilisateur peut définir la valeur de la propriété **MSIINSTALLPERUSER** sur une chaîne vide ("") et la valeur de la propriété [**ALLUSERS**](allusers.md) sur 2 à l’aide d’une interface utilisateur créée ou d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="fd36c-109">To request that the Windows Installer install the dual-purpose package in the per-machine [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to an empty string ("") and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="fd36c-110">Pour demander que le Windows Installer installer le package à double usage dans le [contexte d’installation](installation-context.md)par utilisateur, l’utilisateur peut définir la valeur de la propriété **MSIINSTALLPERUSER** sur 1 et la valeur de la propriété [**ALLUSERS**](allusers.md) sur 2 à l’aide d’une interface utilisateur créée ou d’une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="fd36c-110">To request that the Windows Installer install the dual-purpose package in the per-user [installation context](installation-context.md), the user can set the value of the **MSIINSTALLPERUSER** property to 1 and the value of the [**ALLUSERS**](allusers.md) property to 2 using an authored user interface or a command line.</span></span>

<span data-ttu-id="fd36c-111">Si la valeur de la propriété [**ALLUSERS**](allusers.md) n’est pas égale à 2, le Windows Installer ignore la valeur de la propriété **MSIINSTALLPERUSER** .</span><span class="sxs-lookup"><span data-stu-id="fd36c-111">If the value of the [**ALLUSERS**](allusers.md) property does not equal 2, the Windows Installer ignores the value of the **MSIINSTALLPERUSER** property.</span></span> <span data-ttu-id="fd36c-112">Si Windows Installer installe l’application dans le contexte par ordinateur, il réinitialise la valeur de la propriété **ALLUSERS** sur 1.</span><span class="sxs-lookup"><span data-stu-id="fd36c-112">If Windows Installer installs the application in the per-machine context, it resets the value of the **ALLUSERS** property to 1.</span></span> <span data-ttu-id="fd36c-113">Si Windows Installer installe l’application dans le contexte par utilisateur, il réinitialise la valeur de la propriété **ALLUSERS** sur une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="fd36c-113">If Windows Installer installs the application in the per-user context, it resets the value of the **ALLUSERS** property to an empty string ("").</span></span> <span data-ttu-id="fd36c-114">Les applications qui ont été installées par utilisateur reçoivent par conséquent toutes les mises à jour ou réparations par utilisateur, ainsi que les mises à jour ou les réparations de réception par ordinateur installées par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fd36c-114">Applications that have been installed per-user therefore receive all updates or repairs on a per-user basis and applications installed per-machine receive updates or repairs on a per-machine basis.</span></span>

<span data-ttu-id="fd36c-115">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** la propriété **MSIINSTALLPERUSER** est ignorée par les versions antérieures à Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="fd36c-115">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** The **MSIINSTALLPERUSER** property is ignored by versions earlier than Windows Installer 5.0.</span></span>

## <a name="default-value"></a><span data-ttu-id="fd36c-116">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="fd36c-116">Default Value</span></span>

<span data-ttu-id="fd36c-117">Le contexte d’installation par défaut recommandé est par utilisateur pour un package à double usage.</span><span class="sxs-lookup"><span data-stu-id="fd36c-117">The recommended default installation context is per-user for a dual-purpose package.</span></span> <span data-ttu-id="fd36c-118">Créez MSIINSTALLPERUSER = 1 et ALLUSERS = 2 dans la [table des propriétés](property-table.md) du package à double usage pour spécifier par utilisateur comme contexte d’installation par défaut.</span><span class="sxs-lookup"><span data-stu-id="fd36c-118">Author MSIINSTALLPERUSER=1 and ALLUSERS=2 in the [Property table](property-table.md) of the dual-purpose package to specify per-user as the default installation context.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd36c-119">Notes</span><span class="sxs-lookup"><span data-stu-id="fd36c-119">Remarks</span></span>

<span data-ttu-id="fd36c-120">Vous pouvez vous assurer que la propriété **MSIINSTALLPERUSER** n’a pas été définie en définissant sa valeur sur une chaîne vide (""), MSIINSTALLPERUSER = "".</span><span class="sxs-lookup"><span data-stu-id="fd36c-120">You can ensure the **MSIINSTALLPERUSER** property has not been set by setting its value to an empty string (""), MSIINSTALLPERUSER="".</span></span>

<span data-ttu-id="fd36c-121">Le contexte d’installation détermine les valeurs des propriétés [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**startupfolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md)et [**CommonFiles64Folder**](commonfiles64folder.md) .</span><span class="sxs-lookup"><span data-stu-id="fd36c-121">The installation context determines the values of the [**DesktopFolder**](desktopfolder.md), [**ProgramMenuFolder**](programmenufolder.md), [**StartMenuFolder**](startmenufolder.md), [**StartupFolder**](startupfolder.md), [**TemplateFolder**](templatefolder.md), [**AdminToolsFolder**](admintoolsfolder.md), [**ProgramFilesFolder**](programfilesfolder.md), [**CommonFilesFolder**](commonfilesfolder.md), [**ProgramFiles64Folder**](programfiles64folder.md), and [**CommonFiles64Folder**](commonfiles64folder.md) properties.</span></span> <span data-ttu-id="fd36c-122">Le contexte d’installation détermine les parties du registre où les entrées de la [table du Registre](registry-table.md) et de la [table RemoveRegistry](removeregistry-table.md), avec-1 dans la colonne racine, sont écrites ou supprimées.</span><span class="sxs-lookup"><span data-stu-id="fd36c-122">The installation context determines the parts of the registry where entries in the [Registry table](registry-table.md) and [RemoveRegistry table](removeregistry-table.md), with -1 in the Root column, are written or removed.</span></span> <span data-ttu-id="fd36c-123">Pour plus d’informations sur le contexte d’installation, consultez [contexte d’installation](installation-context.md).</span><span class="sxs-lookup"><span data-stu-id="fd36c-123">For information about the installation context, see [Installation Context](installation-context.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd36c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd36c-124">Requirements</span></span>



| <span data-ttu-id="fd36c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd36c-125">Requirement</span></span> | <span data-ttu-id="fd36c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd36c-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd36c-127">Version</span><span class="sxs-lookup"><span data-stu-id="fd36c-127">Version</span></span><br/> | <span data-ttu-id="fd36c-128">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fd36c-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fd36c-129">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="fd36c-129">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd36c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd36c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd36c-131">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fd36c-131">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="fd36c-132">**ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="fd36c-132">**ALLUSERS**</span></span>](allusers.md)
</dt> <dt>

[<span data-ttu-id="fd36c-133">Contexte d’installation</span><span class="sxs-lookup"><span data-stu-id="fd36c-133">Installation Context</span></span>](installation-context.md)
</dt> <dt>

[<span data-ttu-id="fd36c-134">Création d’un package unique</span><span class="sxs-lookup"><span data-stu-id="fd36c-134">Single Package Authoring</span></span>](single-package-authoring.md)
</dt> </dl>

 

 




