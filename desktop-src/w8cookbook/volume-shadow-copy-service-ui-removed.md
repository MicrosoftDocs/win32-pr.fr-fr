---
title: Interface utilisateur des versions précédentes supprimées pour les volumes locaux
description: Interface utilisateur des versions précédentes supprimées pour les volumes locaux
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25d898be8d079ee713e0fa3e508e552b3cd4009
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104463830"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a><span data-ttu-id="b20cb-103">Interface utilisateur des versions précédentes supprimées pour les volumes locaux</span><span class="sxs-lookup"><span data-stu-id="b20cb-103">Previous versions UI removed for local volumes</span></span>

## <a name="platform"></a><span data-ttu-id="b20cb-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="b20cb-104">Platform</span></span>

<span data-ttu-id="b20cb-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="b20cb-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="b20cb-106">Description</span><span class="sxs-lookup"><span data-stu-id="b20cb-106">Description</span></span>

<span data-ttu-id="b20cb-107">Les versions antérieures de Windows permettaient aux utilisateurs de restaurer des versions précédentes de fichiers individuels à partir de « clichés instantanés » de volumes locaux.</span><span class="sxs-lookup"><span data-stu-id="b20cb-107">Earlier versions of Windows allowed users to restore previous versions of individual files from “shadow copies” of local volumes.</span></span> <span data-ttu-id="b20cb-108">Ces clichés instantanés sont créés par la fonctionnalité « versions précédentes » via le service de cliché instantané des volumes (VSS).</span><span class="sxs-lookup"><span data-stu-id="b20cb-108">These shadow copies are created by the “Previous Versions” feature through Volume Shadow Copy service (VSS).</span></span> <span data-ttu-id="b20cb-109">Dans Windows 7, les utilisateurs pouvaient configurer et planifier des clichés instantanés dans l’interface utilisateur de protection du système disponible via les propriétés système.</span><span class="sxs-lookup"><span data-stu-id="b20cb-109">In Windows 7, users could configure and schedule shadow copies in System Protection UI available through System Properties.</span></span>

<span data-ttu-id="b20cb-110">Toutefois, les versions précédentes étaient rarement utilisées et ont eu un impact négatif sur les performances globales de Windows. par conséquent, la fonctionnalité a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="b20cb-110">However, Previous Versions were rarely used and negatively impacted the overall Windows performance; as a result the feature was removed.</span></span> <span data-ttu-id="b20cb-111">Dans Windows 8, ces fonctionnalités ne sont plus disponibles :</span><span class="sxs-lookup"><span data-stu-id="b20cb-111">In Windows 8, these features are no longer available:</span></span>

-   <span data-ttu-id="b20cb-112">Possibilité de parcourir, de rechercher ou de restaurer des versions précédentes de fichiers par le biais de l’interface utilisateur des versions précédentes</span><span class="sxs-lookup"><span data-stu-id="b20cb-112">The ability to browse, search or restore previous versions of files through Previous Versions UI</span></span>
-   <span data-ttu-id="b20cb-113">Possibilité de configurer ou de planifier des versions précédentes de fichiers par le biais de l’interface utilisateur de la protection du système</span><span class="sxs-lookup"><span data-stu-id="b20cb-113">The ability to configure or schedule previous versions of files through System Protection UI</span></span>

<span data-ttu-id="b20cb-114">Toutefois, les utilisateurs peuvent toujours utiliser l’onglet versions précédentes pour accéder aux partages de fichiers sur un serveur Windows.</span><span class="sxs-lookup"><span data-stu-id="b20cb-114">However, users can still use the Previous Versions tab when accessing file shares on a Windows server.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b20cb-115">Manifestation</span><span class="sxs-lookup"><span data-stu-id="b20cb-115">Manifestation</span></span>

<span data-ttu-id="b20cb-116">L’option versions précédentes n’est plus disponible pour les volumes locaux dans le menu des propriétés de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="b20cb-116">The Previous Versions option is no longer available for local volumes in the Windows Explorer Properties menu.</span></span>

## <a name="solution"></a><span data-ttu-id="b20cb-117">Solution</span><span class="sxs-lookup"><span data-stu-id="b20cb-117">Solution</span></span>

<span data-ttu-id="b20cb-118">Les développeurs qui ont besoin de créer des clichés instantanés de volumes locaux peuvent toujours le faire en appelant des API VSS dans du code personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b20cb-118">Developers who need to create shadow copies of local volumes can still do so by calling VSS APIs in custom code.</span></span>

 

 




