---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: C (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1970c8e9063657701183c91ff337d06d169914fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202545"
---
# <a name="c-windows-installer"></a><span data-ttu-id="fb58b-103">C (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="fb58b-103">C (Windows Installer)</span></span>

<span data-ttu-id="fb58b-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [e](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="fb58b-104">[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="fb58b-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**fichier CAB**</span><span class="sxs-lookup"><span data-stu-id="fb58b-105"><span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**cabinet file**</span></span>
</dt> <dd>

<span data-ttu-id="fb58b-106">Fichier unique, généralement avec une extension. cab, qui stocke les fichiers compressés dans une bibliothèque de fichiers.</span><span class="sxs-lookup"><span data-stu-id="fb58b-106">Single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="fb58b-107">Le format cab est un moyen efficace d’empaqueter plusieurs fichiers, car la compression est effectuée à travers les limites de fichiers, ce qui améliore considérablement le taux de compression.</span><span class="sxs-lookup"><span data-stu-id="fb58b-107">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, significantly improving compression ratio.</span></span> <span data-ttu-id="fb58b-108">Pour plus d’informations sur la création d’armoires, consultez [fichiers CAB](cabinet-files.md).</span><span class="sxs-lookup"><span data-stu-id="fb58b-108">For information about creating cabinets, see [Cabinet Files](cabinet-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb58b-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**EEPROM**</span><span class="sxs-lookup"><span data-stu-id="fb58b-109"><span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**checksum**</span></span>
</dt> <dd>

<span data-ttu-id="fb58b-110">Valeur calculée qui dépend du contenu d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="fb58b-110">Computed value that depends on the contents of a file.</span></span> <span data-ttu-id="fb58b-111">Il est stocké avec les données pour détecter les fichiers endommagés.</span><span class="sxs-lookup"><span data-stu-id="fb58b-111">It is stored with data to detect file corruption.</span></span> <span data-ttu-id="fb58b-112">Le système vérifie cette valeur pour s’assurer que les données ne sont pas endommagées.</span><span class="sxs-lookup"><span data-stu-id="fb58b-112">The system checks this value to ensure that the data is uncorrupted.</span></span>

</dd> <dt>

<span data-ttu-id="fb58b-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**-**</span><span class="sxs-lookup"><span data-stu-id="fb58b-113"><span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="fb58b-114">Plus petite partie d’une installation gérée par le programme d’installation, également un bloc de construction d’une application ou d’une fonctionnalité du point de vue du programmeur.</span><span class="sxs-lookup"><span data-stu-id="fb58b-114">Smallest piece of an installation handled by the installer, also a building-block of an application or feature from the programmer's perspective.</span></span> <span data-ttu-id="fb58b-115">Les exemples de composants sont un groupe de fichiers associés, un objet COM ou une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="fb58b-115">Examples of components are a group of related files, a COM object, or a library.</span></span> <span data-ttu-id="fb58b-116">Pour plus d’informations, consultez [composants et fonctionnalités](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="fb58b-116">For more information, see [Components and Features](components-and-features.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb58b-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**validation des bases de données**</span><span class="sxs-lookup"><span data-stu-id="fb58b-117"><span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**committing databases**</span></span>
</dt> <dd>

<span data-ttu-id="fb58b-118">Modifications accumulées effectuées dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="fb58b-118">Accumulated changes made in a database.</span></span> <span data-ttu-id="fb58b-119">Les modifications ne sont pas reflétées dans la base de données réelle tant que la base de données n’est pas validée.</span><span class="sxs-lookup"><span data-stu-id="fb58b-119">The changes are not reflected in the actual database until the database is committed.</span></span> <span data-ttu-id="fb58b-120">Pour plus d’informations, consultez [validation des bases de données](committing-databases.md).</span><span class="sxs-lookup"><span data-stu-id="fb58b-120">For more information, see [Committing Databases](committing-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb58b-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent,**</span><span class="sxs-lookup"><span data-stu-id="fb58b-121"><span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**</span></span>
</dt> <dd>

<span data-ttu-id="fb58b-122">Aspect des fonctionnalités de l’interface utilisateur du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="fb58b-122">Aspect of functionality of the installer's user interface.</span></span> <span data-ttu-id="fb58b-123">Un ControlEvent, classique déclenche une action par le programme d’installation lors de l’activation d’un contrôle de boîte de dialogue ou d’un autre événement.</span><span class="sxs-lookup"><span data-stu-id="fb58b-123">A typical ControlEvent triggers some action by the installer upon the activation of a dialog box control or other event.</span></span> <span data-ttu-id="fb58b-124">Pour plus d’informations, consultez [vue d’ensemble de ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fb58b-124">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb58b-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**coûts**</span><span class="sxs-lookup"><span data-stu-id="fb58b-125"><span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**costing**</span></span>
</dt> <dd>

<span data-ttu-id="fb58b-126">Méthode utilisée par le programme d’installation pour déterminer l’espace disque requis pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="fb58b-126">Method used by the installer to determine disk space requirements for installation.</span></span> <span data-ttu-id="fb58b-127">Le coût prend en compte des facteurs tels que la nécessité ou non de remplacer les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="fb58b-127">Costing takes into account factors such as whether existing files need to be overwritten.</span></span> <span data-ttu-id="fb58b-128">Pour plus d’informations, consultez [coûts des fichiers](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="fb58b-128">For more information, see [File Costing](file-costing.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb58b-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**fichier. CUB**</span><span class="sxs-lookup"><span data-stu-id="fb58b-129"><span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**.cub file**</span></span>
</dt> <dd>

<span data-ttu-id="fb58b-130">Module de validation qui stocke et fournit l’accès aux actions personnalisées ICE.</span><span class="sxs-lookup"><span data-stu-id="fb58b-130">Validation module that stores and provides access to ICE custom actions.</span></span> <span data-ttu-id="fb58b-131">Pour plus d’informations, consultez [exemple de fichier. CUB](sample--cub-file.md).</span><span class="sxs-lookup"><span data-stu-id="fb58b-131">For more information, see [Sample .cub File](sample--cub-file.md).</span></span> <span data-ttu-id="fb58b-132">Pour plus d’informations, consultez également [Windows Installer extensions de fichier](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="fb58b-132">For more information, see also [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb58b-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**action personnalisée**</span><span class="sxs-lookup"><span data-stu-id="fb58b-133"><span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**custom action**</span></span>
</dt> <dd>

<span data-ttu-id="fb58b-134">Écrit par l’auteur du [*package*](p-gly.md) , mais n’est pas intégré au programme d’installation comme action standard.</span><span class="sxs-lookup"><span data-stu-id="fb58b-134">Written by the author of the [*package*](p-gly.md) but not built into the installer as a standard action.</span></span> <span data-ttu-id="fb58b-135">Pour plus d’informations, consultez [actions personnalisées](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="fb58b-135">For more information, see [Custom Actions](custom-actions.md).</span></span>

</dd> </dl>

 

 



