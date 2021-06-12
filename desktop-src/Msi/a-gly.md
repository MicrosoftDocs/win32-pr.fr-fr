---
description: En savoir plus sur les concepts de Windows Installer qui commencent par la lettre A, tels que l’accessibilité et la phase d’acquisition.
ms.assetid: 541fd08c-c21a-4a51-aa1c-d65cc0f5da75
title: A (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eea91c044553ec374f28309a86002a386961d2c9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011122"
---
# <a name="a-windows-installer"></a><span data-ttu-id="f14a7-103">A (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="f14a7-103">A (Windows Installer)</span></span>

<span data-ttu-id="f14a7-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="f14a7-104">A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="f14a7-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**aux**</span><span class="sxs-lookup"><span data-stu-id="f14a7-105"><span id="_msi_accessibility_using_windows_installer_gly"></span><span id="_MSI_ACCESSIBILITY_USING_WINDOWS_INSTALLER_GLY"></span>**accessibility**</span></span>
</dt> <dd>

<span data-ttu-id="f14a7-106">Implémentation de la conception pour rendre l’interface utilisateur du programme d’installation accessible à tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f14a7-106">Design implementation for making the installer's user interface accessible to all users.</span></span> <span data-ttu-id="f14a7-107">Pour plus d’informations sur l’accessibilité, consultez la rubrique de vue d’ensemble : [accessibilité](accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="f14a7-107">For more information about accessibility, see the overview topic: [Accessibility](accessibility.md).</span></span>

</dd> <dt>

<span data-ttu-id="f14a7-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**phase d’acquisition**</span><span class="sxs-lookup"><span data-stu-id="f14a7-108"><span id="_msi_acquisition_phase_gly"></span><span id="_MSI_ACQUISITION_PHASE_GLY"></span>**acquisition phase**</span></span>
</dt> <dd>

<span data-ttu-id="f14a7-109">Phase d’installation pendant laquelle le programme d’installation détermine la procédure.</span><span class="sxs-lookup"><span data-stu-id="f14a7-109">Phase of installation during which the installer determines procedure.</span></span> <span data-ttu-id="f14a7-110">La phase d’acquisition commence quand une application ou un utilisateur demande à [*Windows Installer*](m-gly.md) d’installer une application ou une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="f14a7-110">Acquisition phase begins when an application or user instructs [*Windows Installer*](m-gly.md) to install an application or feature.</span></span> <span data-ttu-id="f14a7-111">Le programme d’installation interroge ensuite la [*base de données*](i-gly.md) à la recherche d’informations lors de la génération du [*script d’exécution*](e-gly.md) de l’installation.</span><span class="sxs-lookup"><span data-stu-id="f14a7-111">The installer then queries the [*database*](i-gly.md) for information as it generates the [*execution script*](e-gly.md) for the installation.</span></span> <span data-ttu-id="f14a7-112">Pour plus d’informations sur les phases d’une installation, consultez [mécanisme d’installation](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="f14a7-112">For more information about the phases of an installation, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="f14a7-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**transactionnel**</span><span class="sxs-lookup"><span data-stu-id="f14a7-113"><span id="_msi_action_gly"></span><span id="_MSI_ACTION_GLY"></span>**action**</span></span>
</dt> <dd>

<span data-ttu-id="f14a7-114">La plupart des fonctions effectuées par Windows Installer sont encapsulées dans des actions.</span><span class="sxs-lookup"><span data-stu-id="f14a7-114">Many of the functions performed by Windows Installer are encapsulated into actions.</span></span> <span data-ttu-id="f14a7-115">Chaque action spécifie l’exécution d’une fonction particulière et le déroulement total des procédures de l’installation est déterminé par la séquence d’actions dans les [*tables de séquence*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f14a7-115">Each action specifies the execution of a particular function and the total procedural flow of the installation is prescribed by the sequence of actions in the [*Sequence tables*](s-gly.md).</span></span> <span data-ttu-id="f14a7-116">Les [*actions standard*](s-gly.md) sont intégrées à Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f14a7-116">[*Standard actions*](s-gly.md) are built into Windows Installer.</span></span> <span data-ttu-id="f14a7-117">Les [*actions personnalisées*](c-gly.md) sont écrites par l’auteur du [*package*](p-gly.md)d’installation.</span><span class="sxs-lookup"><span data-stu-id="f14a7-117">[*Custom actions*](c-gly.md) are written by the author of the installation [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="f14a7-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Mode d’approbation Administrateur**</span><span class="sxs-lookup"><span data-stu-id="f14a7-118"><span id="_msi_admin_approval_mode_gly"></span><span id="_MSI_ADMIN_APPROVAL_MODE_GLY"></span>**Admin Approval Mode**</span></span>
</dt> <dd>

<span data-ttu-id="f14a7-119">État d’approbation activé par la protection de compte d’utilisateur (UAC) qui exécute tous les utilisateurs avec des privilèges minimum, y compris les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="f14a7-119">The approval state enabled by User Account Protection (UAC) that runs all users with least privilege, including administrators.</span></span> <span data-ttu-id="f14a7-120">Les utilisateurs doivent donner leur consentement pour élever les installations qui requièrent des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="f14a7-120">Users are required to provide consent to elevate installations that require administrator privileges.</span></span>

</dd> <dt>

<span data-ttu-id="f14a7-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**supports**</span><span class="sxs-lookup"><span data-stu-id="f14a7-121"><span id="_msi_advertising_gly"></span><span id="_MSI_ADVERTISING_GLY"></span>**advertising**</span></span>
</dt> <dd>

<span data-ttu-id="f14a7-122">Capacité à rendre les interfaces nécessaires au chargement et à rendre une application disponible sans installer l’application.</span><span class="sxs-lookup"><span data-stu-id="f14a7-122">Capability to make the interfaces required for loading and to make an application available without installing the application.</span></span> <span data-ttu-id="f14a7-123">Lorsqu’un utilisateur ou une application active une interface publiée, le programme d’installation continue à installer les composants nécessaires.</span><span class="sxs-lookup"><span data-stu-id="f14a7-123">When a user or application activates an advertised interface, the installer then proceeds to install the necessary components.</span></span> <span data-ttu-id="f14a7-124">Les deux types de publicité sont l' [*attribution*](/windows) et la [*publication*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f14a7-124">The two types of advertising are [*assigning*](/windows) and [*publishing*](p-gly.md).</span></span> <span data-ttu-id="f14a7-125">Pour plus d’informations, consultez également [*Install-on-demand*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f14a7-125">For more information, see also [*install-on-demand*](i-gly.md).</span></span> <span data-ttu-id="f14a7-126">Pour plus d’informations sur la façon dont le programme d’installation publie des applications, consultez [publication](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="f14a7-126">For more information about how the installer advertises applications, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f14a7-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Service d’informations d’application (AIS)**</span><span class="sxs-lookup"><span data-stu-id="f14a7-127"><span id="_msi_application_information_service_gly"></span><span id="_MSI_APPLICATION_INFORMATION_SERVICE_GLY"></span>**Application Information Service (AIS)**</span></span>
</dt> <dd>

<span data-ttu-id="f14a7-128">Service système de Windows Vista qui facilite le démarrage des installations nécessitant des privilèges élevés pour s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="f14a7-128">A system service of Windows Vista that facilitates starting installations that require elevated privileges to run.</span></span> <span data-ttu-id="f14a7-129">Fournit l’interface utilisateur de consentement utilisée par le contrôle de compte d’utilisateur pour inviter un utilisateur à autoriser l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="f14a7-129">Provides the Consent UI used by User Account Control to prompt a user for administrator authorization.</span></span>

</dd> <dt>

<span data-ttu-id="f14a7-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**affectation**</span><span class="sxs-lookup"><span data-stu-id="f14a7-130"><span id="_msi_assigning_gly"></span><span id="_MSI_ASSIGNING_GLY"></span>**assigning**</span></span>
</dt> <dd>

<span data-ttu-id="f14a7-131">Rend une application disponible et la fait apparaître comme si elle avait été installée pour un utilisateur, sans l’installer réellement.</span><span class="sxs-lookup"><span data-stu-id="f14a7-131">Makes an application available, and makes it appear as if it has been installed to a user, without actually installing it.</span></span> <span data-ttu-id="f14a7-132">L’attribution d’ajouter des raccourcis et des icônes au menu **Démarrer** , associe les fichiers appropriés et écrit les entrées de registre de l’application.</span><span class="sxs-lookup"><span data-stu-id="f14a7-132">Assigning adds shortcuts and icons to the **Start** menu, associates appropriate files, and writes registry entries for the application.</span></span> <span data-ttu-id="f14a7-133">Quand un utilisateur tente d’ouvrir une application affectée, le programme d’installation installe l’application.</span><span class="sxs-lookup"><span data-stu-id="f14a7-133">When a user tries to open an assigned application, then the installer installs the application.</span></span> <span data-ttu-id="f14a7-134">L’attribution et la [*publication*](p-gly.md) sont deux méthodes de [*publicité*](/windows).</span><span class="sxs-lookup"><span data-stu-id="f14a7-134">Assigning and [*publishing*](p-gly.md) are two methods of [*advertising*](/windows).</span></span> <span data-ttu-id="f14a7-135">Pour plus d’informations, consultez [publication](advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="f14a7-135">For more information, see [Advertisement](advertisement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f14a7-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**exécution asynchrone**</span><span class="sxs-lookup"><span data-stu-id="f14a7-136"><span id="_msi_asynchronous_execution_using_windows_installer_gly"></span><span id="_MSI_ASYNCHRONOUS_EXECUTION_USING_WINDOWS_INSTALLER_GLY"></span>**asynchronous execution**</span></span>
</dt> <dd>

<span data-ttu-id="f14a7-137">[*Action personnalisée*](c-gly.md) pendant laquelle le programme d’installation exécute simultanément des threads distincts de l’action personnalisée et de l’installation actuelle.</span><span class="sxs-lookup"><span data-stu-id="f14a7-137">[*Custom action*](c-gly.md) during which the installer runs separate threads of the custom action and the current installation simultaneously.</span></span> <span data-ttu-id="f14a7-138">Pour plus d’informations, consultez [actions personnalisées synchrones et asynchrones](synchronous-and-asynchronous-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="f14a7-138">For more information, see [Synchronous and Asynchronous Custom Actions](synchronous-and-asynchronous-custom-actions.md).</span></span>

</dd> </dl>

 

 
