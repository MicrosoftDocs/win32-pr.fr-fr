---
description: En savoir plus sur les concepts de Windows Installer qui commencent par la lettre E, tels que les fichiers sources élevés et externes.
ms.assetid: 8f180e2c-06f4-41d5-b167-52525f4a9985
title: E (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2c65c50427b1f8271be838971a387388ea53db
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011093"
---
# <a name="e-windows-installer"></a><span data-ttu-id="8224c-103">E (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="8224c-103">E (Windows Installer)</span></span>

<span data-ttu-id="8224c-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) e [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="8224c-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="8224c-105"><span id="_msi_elevated_gly"></span><span id="_MSI_ELEVATED_GLY"></span>**avec élévation**</span><span class="sxs-lookup"><span data-stu-id="8224c-105"><span id="_msi_elevated_gly"></span><span id="_MSI_ELEVATED_GLY"></span>**elevated**</span></span>
</dt> <dd>

<span data-ttu-id="8224c-106">Les actions effectuées avec des privilèges système sont appelées avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="8224c-106">Actions performed with system privileges are called elevated.</span></span>

</dd> <dt>

<span data-ttu-id="8224c-107"><span id="_msi_execution_phase_gly"></span><span id="_MSI_EXECUTION_PHASE_GLY"></span>**phase d’exécution**</span><span class="sxs-lookup"><span data-stu-id="8224c-107"><span id="_msi_execution_phase_gly"></span><span id="_MSI_EXECUTION_PHASE_GLY"></span>**execution phase**</span></span>
</dt> <dd>

<span data-ttu-id="8224c-108">Quand le programme d’installation exécute un script des actions du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="8224c-108">When the installer executes a script of installer actions.</span></span> <span data-ttu-id="8224c-109">Dans Microsoft Windows 2000, ce processus est effectué par le service d’installation.</span><span class="sxs-lookup"><span data-stu-id="8224c-109">In Microsoft Windows 2000, this process is performed by the installer service.</span></span> <span data-ttu-id="8224c-110">Dans une application managée, le script est exécuté avec des privilèges système.</span><span class="sxs-lookup"><span data-stu-id="8224c-110">In a managed application, the script is executed with system privileges.</span></span> <span data-ttu-id="8224c-111">Pour plus d’informations, consultez [mécanisme d’installation](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="8224c-111">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="8224c-112"><span id="_msi_execution_script_gly"></span><span id="_MSI_EXECUTION_SCRIPT_GLY"></span>**script d’exécution**</span><span class="sxs-lookup"><span data-stu-id="8224c-112"><span id="_msi_execution_script_gly"></span><span id="_MSI_EXECUTION_SCRIPT_GLY"></span>**execution script**</span></span>
</dt> <dd>

<span data-ttu-id="8224c-113">Actions du programme d’installation pour une installation.</span><span class="sxs-lookup"><span data-stu-id="8224c-113">Installer actions for an installation.</span></span> <span data-ttu-id="8224c-114">Le script d’exécution est généré pendant la [*phase d’acquisition*](a-gly.md) de l’installation et exécuté pendant la phase d' [*exécution*](/windows).</span><span class="sxs-lookup"><span data-stu-id="8224c-114">The execution script is generated during the [*acquisition phase*](a-gly.md) of installation and executed during the [*execution phase*](/windows).</span></span> <span data-ttu-id="8224c-115">Pour plus d’informations, consultez [mécanisme d’installation](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="8224c-115">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span>

</dd> <dt>

<span data-ttu-id="8224c-116"><span id="_msi_external_source_files_gly"></span><span id="_MSI_EXTERNAL_SOURCE_FILES_GLY"></span>**fichiers sources externes**</span><span class="sxs-lookup"><span data-stu-id="8224c-116"><span id="_msi_external_source_files_gly"></span><span id="_MSI_EXTERNAL_SOURCE_FILES_GLY"></span>**external source files**</span></span>
</dt> <dd>

<span data-ttu-id="8224c-117">Fichiers sources de l’application en cours d’installation qui sont stockés en dehors du [*fichier.msi*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8224c-117">Source files of the application being installed that are stored outside of the [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="8224c-118">Plusieurs fichiers sources externes peuvent être compressés et stockés ensemble à l’intérieur d’un [*fichier CAB*](c-gly.md) inclus dans le [*package*](p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8224c-118">Multiple external source files can be compressed and stored together inside of a [*cabinet file*](c-gly.md) included in the [*package*](p-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="8224c-119"><span id="_msi_external_user_interface_gly"></span><span id="_MSI_EXTERNAL_USER_INTERFACE_GLY"></span>**interface utilisateur externe**</span><span class="sxs-lookup"><span data-stu-id="8224c-119"><span id="_msi_external_user_interface_gly"></span><span id="_MSI_EXTERNAL_USER_INTERFACE_GLY"></span>**external user interface**</span></span>
</dt> <dd>

<span data-ttu-id="8224c-120">Interface utilisateur fournie par l’auteur d’un package d’installation.</span><span class="sxs-lookup"><span data-stu-id="8224c-120">UI provided by the author of an installation package.</span></span> <span data-ttu-id="8224c-121">Elle n’utilise pas les fonctionnalités internes de l’interface utilisateur du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="8224c-121">It does not use the internal UI capabilities of the installer.</span></span> <span data-ttu-id="8224c-122">Pour plus d’informations, consultez [à propos de l’interface utilisateur](about-the-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="8224c-122">For more information, see [About the User Interface](about-the-user-interface.md).</span></span>

</dd> </dl>

 

 
