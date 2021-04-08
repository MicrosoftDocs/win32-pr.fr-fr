---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca95a473f648ca9e1a08773d93f47bd198df11e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866306"
---
# <a name="i-windows-installer"></a><span data-ttu-id="8eb6e-103">I (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="8eb6e-103">I (Windows Installer)</span></span>

<span data-ttu-id="8eb6e-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="8eb6e-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="8eb6e-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**fichier. IDT**</span><span class="sxs-lookup"><span data-stu-id="8eb6e-105"><span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**.idt file**</span></span>
</dt> <dd>

<span data-ttu-id="8eb6e-106">Table de base de données du programme d’installation exporté.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-106">Exported installer database table.</span></span> <span data-ttu-id="8eb6e-107">Pour plus d’informations, consultez [importation et exportation](importing-and-exporting.md) et [Windows Installer des extensions de fichier](windows-installer-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="8eb6e-107">For more information, see [Importing and Exporting](importing-and-exporting.md) and [Windows Installer File Extensions](windows-installer-file-extensions.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eb6e-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Table des adresses d’importation (IAT)**</span><span class="sxs-lookup"><span data-stu-id="8eb6e-108"><span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Import Address table (IAT)**</span></span>
</dt> <dd>

<span data-ttu-id="8eb6e-109">Où l’adresse virtuelle calculée est enregistrée à partir de chaque fonction importée à partir de toutes les dll.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-109">Where the computed virtual address is saved from each function imported from all DLLs.</span></span>

</dd> <dt>

<span data-ttu-id="8eb6e-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**interface utilisateur interne**</span><span class="sxs-lookup"><span data-stu-id="8eb6e-110"><span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**internal user interface**</span></span>
</dt> <dd>

<span data-ttu-id="8eb6e-111">Fonctionnalités intégrées du programme d’installation qui peuvent être utilisées pour créer une interface utilisateur graphique pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-111">Built-in capabilities of the installer that can be used to author a graphical UI for installation.</span></span> <span data-ttu-id="8eb6e-112">Un auteur peut choisir une [*interface utilisateur externe*](e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8eb6e-112">An author may choose an [*external user interface*](e-gly.md).</span></span> <span data-ttu-id="8eb6e-113">Pour plus d’informations, consultez [à propos de l’interface utilisateur](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="8eb6e-113">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eb6e-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**niveau d’installation**</span><span class="sxs-lookup"><span data-stu-id="8eb6e-114"><span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**install level**</span></span>
</dt> <dd>

<span data-ttu-id="8eb6e-115">Valeur d’installation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-115">Specified installation value.</span></span> <span data-ttu-id="8eb6e-116">Une application est installée uniquement si son propre niveau est inférieur ou égal au niveau d’installation.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-116">An application is installed only if its own level is less than or equal to the install level.</span></span> <span data-ttu-id="8eb6e-117">L’ensemble des applications choisies pour l’installation peut donc être modifié en modifiant le niveau d’installation.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-117">The set of applications chosen for installation can therefore be changed by altering the install level.</span></span> <span data-ttu-id="8eb6e-118">Pour plus d’informations, consultez [table des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8eb6e-118">For more information, see [Feature Table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eb6e-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installation à la demande**</span><span class="sxs-lookup"><span data-stu-id="8eb6e-119"><span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installation-on-demand**</span></span>
</dt> <dd>

<span data-ttu-id="8eb6e-120">Service qui installe les applications ou les fonctionnalités demandées par l’utilisateur ou une autre application.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-120">Service that installs applications or features as requested by the user or another application.</span></span> <span data-ttu-id="8eb6e-121">La [*publicité*](a-gly.md) rend une fonctionnalité ou une application disponible pour une installation à la demande.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-121">[*Advertising*](a-gly.md) makes a feature or application available for install-on-demand installation.</span></span> <span data-ttu-id="8eb6e-122">Pour plus d’informations, consultez : [installation à la demande](installation-on-demand.md).</span><span class="sxs-lookup"><span data-stu-id="8eb6e-122">For more information, see: [Installation-on-Demand](installation-on-demand.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eb6e-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**contexte d’installation**</span><span class="sxs-lookup"><span data-stu-id="8eb6e-123"><span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**installation context**</span></span>
</dt> <dd>

<span data-ttu-id="8eb6e-124">La combinaison des droits d’installation et des types d’installation produit trois contextes d’installation différents : gérés par utilisateur, géré par utilisateur et par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-124">The combination of installation rights and installation types produces three different installation contexts: per-user non-managed, per-user managed, and per-machine managed.</span></span> <span data-ttu-id="8eb6e-125">Ce n’est pas le cas par ordinateur non géré.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-125">There is no such thing as per-machine non-managed.</span></span>

</dd> <dt>

<span data-ttu-id="8eb6e-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**d'**</span><span class="sxs-lookup"><span data-stu-id="8eb6e-126"><span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**installer**</span></span>
</dt> <dd>

<span data-ttu-id="8eb6e-127">[*Windows Installer*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8eb6e-127">The [*Windows Installer*](m-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eb6e-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**base de données du programme d’installation**</span><span class="sxs-lookup"><span data-stu-id="8eb6e-128"><span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**installer database**</span></span>
</dt> <dd>

<span data-ttu-id="8eb6e-129">Base de données relationnelle contenant les instructions d’installation pour une installation.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-129">Relational database containing setup instructions for an installation.</span></span> <span data-ttu-id="8eb6e-130">La base de données du programme d’installation est stockée dans le [*fichier. msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8eb6e-130">The installer database is stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="8eb6e-131">Pour plus d’informations, consultez [base de données du programme d’installation](installer-database.md).</span><span class="sxs-lookup"><span data-stu-id="8eb6e-131">For more information, see [Installer Database](installer-database.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eb6e-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**fonction installer**</span><span class="sxs-lookup"><span data-stu-id="8eb6e-132"><span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**installer function**</span></span>
</dt> <dd>

<span data-ttu-id="8eb6e-133">Appelée par un utilisateur ou une application pour obtenir les services et les fonctionnalités du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-133">Called by a user or application to obtain installer services and functionality.</span></span> <span data-ttu-id="8eb6e-134">Il s’agit de l’interface de programmation d’applications du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-134">This is the application programming interface of the installer.</span></span> <span data-ttu-id="8eb6e-135">Pour plus d’informations, consultez [référence des fonctions du programme d’installation](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8eb6e-135">For information, see [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="8eb6e-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**outil de création de packages d’installation**</span><span class="sxs-lookup"><span data-stu-id="8eb6e-136"><span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**installer package authoring tool**</span></span>
</dt> <dd>

<span data-ttu-id="8eb6e-137">Logiciel qui permet à un développeur de créer et de modifier un [*fichier. msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8eb6e-137">Software that enables a developer to create and edit an [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="8eb6e-138">Ainsi, tout [*fichier source externe*](e-gly.md) comprend un [*package*](p-gly.md) contenant toutes les informations requises pour une installation.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-138">This together with any [*external source files*](e-gly.md) comprise a [*package*](p-gly.md) containing all the information required for an installation.</span></span>

</dd> <dt>

<span data-ttu-id="8eb6e-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**fichiers sources internes**</span><span class="sxs-lookup"><span data-stu-id="8eb6e-139"><span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**internal source files**</span></span>
</dt> <dd>

<span data-ttu-id="8eb6e-140">Stocké dans le [*fichier. msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8eb6e-140">Stored in the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="8eb6e-141">Plusieurs fichiers sources internes peuvent être compressés et stockés ensemble dans un [*fichier CAB*](c-gly.md) stocké dans un fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="8eb6e-141">Multiple internal source files can be compressed and stored together in a [*cabinet file*](c-gly.md) that is stored within an .msi file.</span></span>

</dd> </dl>

 

 



