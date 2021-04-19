---
description: Les Windows Installer fonctions, les tables et les propriétés répertoriées sur cette page ne sont pas prises en charge par Windows Installer&\# 160 ; 3.0 et versions antérieures.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Non pris en charge dans Windows Installer 3,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521512"
---
# <a name="not-supported-in-windows-installer-30"></a><span data-ttu-id="dcd0e-103">Non pris en charge dans Windows Installer 3,0</span><span class="sxs-lookup"><span data-stu-id="dcd0e-103">Not Supported in Windows Installer 3.0</span></span>

<span data-ttu-id="dcd0e-104">Les fonctions Windows Installer, les tables et les propriétés répertoriées sur cette page ne sont pas prises en charge par Windows Installer 3,0 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="dcd0e-104">The Windows Installer functions, tables, and properties listed on this page are not supported by Windows Installer 3.0 and earlier versions.</span></span> <span data-ttu-id="dcd0e-105">L’absence d’une fonctionnalité dans cette liste ne garantit pas que la fonctionnalité est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dcd0e-105">The absence of a feature from this list does not guarantee that the feature is supported.</span></span> <span data-ttu-id="dcd0e-106">Consultez la documentation principale pour déterminer quelle version de Windows Installer est requise pour une fonctionnalité particulière.</span><span class="sxs-lookup"><span data-stu-id="dcd0e-106">See the main documentation to determine which Windows Installer version is required for a particular feature.</span></span> <span data-ttu-id="dcd0e-107">Pour plus d’informations sur les autres versions [de Windows Installer, consultez Nouveautés de Windows Installer](what-s-new-in-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="dcd0e-107">For information about other Windows Installer versions see [What's New in Windows Installer](what-s-new-in-windows-installer.md).</span></span>

<span data-ttu-id="dcd0e-108">Windows Installer 3,0 est disponible pour Windows Server 2003, Windows XP ou Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="dcd0e-108">Windows Installer 3.0 is available for Windows Server 2003, Windows XP, or Windows 2000.</span></span> <span data-ttu-id="dcd0e-109">Pour obtenir la liste de toutes les versions de Windows Installer et des fichiers redistribuables, consultez [versions publiées de Windows Installer](released-versions-of-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="dcd0e-109">For a list of all Windows Installer versions and redistributables, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

<span data-ttu-id="dcd0e-110">Les fonctionnalités suivantes ne sont pas prises en charge dans Windows Installer 3,0 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="dcd0e-110">The following features are not supported in Windows Installer 3.0 and earlier versions.</span></span>

[<span data-ttu-id="dcd0e-111">Fonctions du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="dcd0e-111">Installer Functions</span></span>](installer-functions.md)

-   [<span data-ttu-id="dcd0e-112">**MsiSetExternalUIRecord**</span><span class="sxs-lookup"><span data-stu-id="dcd0e-112">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="dcd0e-113">**MsiNotifySidChange**</span><span class="sxs-lookup"><span data-stu-id="dcd0e-113">**MsiNotifySidChange**</span></span>](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

<span data-ttu-id="dcd0e-114">Prototype de fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="dcd0e-114">Callback Function Prototype</span></span>

-   [<span data-ttu-id="dcd0e-115">**\_enregistrement du gestionnaire INSTALLUI \_**</span><span class="sxs-lookup"><span data-stu-id="dcd0e-115">**INSTALLUI\_HANDLER\_RECORD**</span></span>](/windows/win32/api/msi/nc-msi-installui_handler_record)

[<span data-ttu-id="dcd0e-116">Tables de base de données</span><span class="sxs-lookup"><span data-stu-id="dcd0e-116">Database Tables</span></span>](database-tables.md)

-   <span data-ttu-id="dcd0e-117">La colonne value de la [table MsiPatchMetadata](msipatchmetadata-table.md) accepte **OptimizedInstallMode** et **MinorUpdateTargetRTM**.</span><span class="sxs-lookup"><span data-stu-id="dcd0e-117">The Value column of the [MsiPatchMetadata Table](msipatchmetadata-table.md) accepts **OptimizedInstallMode** and **MinorUpdateTargetRTM**.</span></span>

[<span data-ttu-id="dcd0e-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dcd0e-118">Properties</span></span>](properties.md)

-   [<span data-ttu-id="dcd0e-119">**Propriété Msix64**</span><span class="sxs-lookup"><span data-stu-id="dcd0e-119">**Msix64 Property**</span></span>](msix64.md)

[<span data-ttu-id="dcd0e-120">Windows Installer sur les systèmes d’exploitation 64 bits</span><span class="sxs-lookup"><span data-stu-id="dcd0e-120">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)

-   <span data-ttu-id="dcd0e-121">La [**propriété Résumé du modèle**](template-summary.md) accepte la valeur x64.</span><span class="sxs-lookup"><span data-stu-id="dcd0e-121">The [**Template Summary Property**](template-summary.md) accepts the value x64.</span></span>

[<span data-ttu-id="dcd0e-122">Évaluateurs de cohérence internes-CIEM</span><span class="sxs-lookup"><span data-stu-id="dcd0e-122">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

-   [<span data-ttu-id="dcd0e-123">ICE99</span><span class="sxs-lookup"><span data-stu-id="dcd0e-123">ICE99</span></span>](ice99.md)

 

 
