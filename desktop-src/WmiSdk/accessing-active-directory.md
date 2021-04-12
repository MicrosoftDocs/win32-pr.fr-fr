---
description: Active Directory est le service d’annuaire pour Windows et constitue la base des réseaux distribués Windows.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Accès Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbad433f1f189d68c8a7ab2f312cbb678b15ee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210217"
---
# <a name="accessing-active-directory"></a><span data-ttu-id="37773-103">Accès Active Directory</span><span class="sxs-lookup"><span data-stu-id="37773-103">Accessing Active Directory</span></span>

<span data-ttu-id="37773-104">Active Directory est le service d’annuaire pour Windows et constitue la base des réseaux distribués Windows.</span><span class="sxs-lookup"><span data-stu-id="37773-104">Active Directory is the directory service for Windows and is the foundation of Windows distributed networks.</span></span> <span data-ttu-id="37773-105">Vous pouvez utiliser Active Directory pour localiser des objets dans un domaine réseau d’ordinateurs, tels que des utilisateurs, des stratégies de sécurité, des imprimantes, des composants distribués et d’autres ressources.</span><span class="sxs-lookup"><span data-stu-id="37773-105">You can use Active Directory to locate objects in a computer network domain, such as users, security policies, printers, distributed components, and other resources.</span></span> <span data-ttu-id="37773-106">Le nom Active Directory fait référence à la fois au service d’annuaire et au répertoire lui-même.</span><span class="sxs-lookup"><span data-stu-id="37773-106">The name Active Directory refers both to the directory service and the directory itself.</span></span>

> [!Note]  
> <span data-ttu-id="37773-107">Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="37773-107">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="37773-108">Windows rend Active Directory accessible via WMI en créant un ensemble de références à chaque classe et objet contenu dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="37773-108">Windows makes Active Directory accessible through WMI by creating a set of references to every class and object contained in Active Directory.</span></span> <span data-ttu-id="37773-109">En accédant au fournisseur de services d’annuaire par le biais de WMI, vous pouvez créer des applications compatibles WMI qui peuvent accéder à la richesse des informations contenues dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="37773-109">By accessing the Directory Services provider through WMI, you can create WMI-enabled applications that can access the wealth of information contained in Active Directory.</span></span>

<span data-ttu-id="37773-110">Avec ces interfaces, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="37773-110">With these interfaces, you can:</span></span>

-   <span data-ttu-id="37773-111">Récupérer des classes et des instances.</span><span class="sxs-lookup"><span data-stu-id="37773-111">Retrieve classes and instances.</span></span>
-   <span data-ttu-id="37773-112">Énumérez les classes et les instances.</span><span class="sxs-lookup"><span data-stu-id="37773-112">Enumerate classes and instances.</span></span>
-   <span data-ttu-id="37773-113">Créer des instances.</span><span class="sxs-lookup"><span data-stu-id="37773-113">Create new instances.</span></span>
-   <span data-ttu-id="37773-114">Modifiez des instances existantes.</span><span class="sxs-lookup"><span data-stu-id="37773-114">Modify existing instances.</span></span>
-   <span data-ttu-id="37773-115">Supprimer des instances existantes.</span><span class="sxs-lookup"><span data-stu-id="37773-115">Delete existing instances.</span></span>
-   <span data-ttu-id="37773-116">Active Directory de requête.</span><span class="sxs-lookup"><span data-stu-id="37773-116">Query Active Directory.</span></span>

<span data-ttu-id="37773-117">Les rubriques suivantes peuvent vous aider à utiliser Active Directory avec WMI :</span><span class="sxs-lookup"><span data-stu-id="37773-117">The following topics can assist you in using Active Directory with WMI:</span></span>

-   [<span data-ttu-id="37773-118">Utilisation de la syntaxe de Active Directory appropriée</span><span class="sxs-lookup"><span data-stu-id="37773-118">Using the Proper Active Directory Syntax</span></span>](using-the-proper-active-directory-syntax.md)
-   [<span data-ttu-id="37773-119">Mappage de Active Directory à WMI</span><span class="sxs-lookup"><span data-stu-id="37773-119">Mapping Active Directory to WMI</span></span>](mapping-active-directory-to-wmi.md)

 

 



