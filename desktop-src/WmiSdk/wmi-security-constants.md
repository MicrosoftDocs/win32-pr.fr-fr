---
description: WMI vérifie les droits d’accès pour les applications et les scripts.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Constantes de sécurité WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d360aa57c12c958db95c4b94f2b06327a3f70dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210413"
---
# <a name="wmi-security-constants"></a><span data-ttu-id="e59c8-103">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="e59c8-103">WMI Security Constants</span></span>

<span data-ttu-id="e59c8-104">WMI vérifie les droits d’accès pour les applications et les scripts pour des objets tels que les espaces de noms WMI, les imprimantes, les services, les applications DCOM, les fichiers, les partages et d’autres objets sécurisables.</span><span class="sxs-lookup"><span data-stu-id="e59c8-104">WMI checks access rights for applications and scripts for objects such as WMI namespaces, printer, services, DCOM applications, files, shares, and other securable objects.</span></span> <span data-ttu-id="e59c8-105">L’accès à ces objets sécurisables est contrôlé par les entrées de contrôle d’accès (ACE).</span><span class="sxs-lookup"><span data-stu-id="e59c8-105">Access to theses securable objects is controlled by access control entries (ACE).</span></span> <span data-ttu-id="e59c8-106">Chaque ACE contient des listes qui désignent les groupes ou utilisateurs qui ont accès.</span><span class="sxs-lookup"><span data-stu-id="e59c8-106">Each ACE contains lists that designate which groups or users have access.</span></span> <span data-ttu-id="e59c8-107">Pour plus d’informations sur la sécurité et les listes de contrôle d’accès (ACL, DACL ou SACL), consultez [listes de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists) et [descripteurs de sécurité](/windows/desktop/SecAuthZ/security-descriptors).</span><span class="sxs-lookup"><span data-stu-id="e59c8-107">For more information about security and access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors).</span></span>

<span data-ttu-id="e59c8-108">De nombreuses méthodes de fournisseur dans WMI qui affectent des objets sécurisables requièrent que l’administrateur Active certains privilèges.</span><span class="sxs-lookup"><span data-stu-id="e59c8-108">Many provider methods in WMI that affect securable objects require the administrator to enable certain privileges.</span></span> <span data-ttu-id="e59c8-109">La version du privilège que vous utilisez dépend du langage de programmation, comme indiqué dans [**constantes de privilège**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e59c8-109">Which version of the privilege you use depends on the programming language, as shown in [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="e59c8-110">Les constantes de sécurité sont définies dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="e59c8-110">The security constants are defined in the following topics:</span></span>

-   [<span data-ttu-id="e59c8-111">**Constantes de sécurité d’événement**</span><span class="sxs-lookup"><span data-stu-id="e59c8-111">**Event Security Constants**</span></span>](event-security-constants.md)
-   [<span data-ttu-id="e59c8-112">**Constantes de droits d’accès aux fichiers et aux répertoires**</span><span class="sxs-lookup"><span data-stu-id="e59c8-112">**File and Directory Access Rights Constants**</span></span>](file-and-directory-access-rights-constants.md)
-   [<span data-ttu-id="e59c8-113">**Constantes de droits d’accès à l’espace de noms**</span><span class="sxs-lookup"><span data-stu-id="e59c8-113">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
-   [<span data-ttu-id="e59c8-114">**Constantes d’indicateur ACE d’espace de noms**</span><span class="sxs-lookup"><span data-stu-id="e59c8-114">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
-   [<span data-ttu-id="e59c8-115">**Constantes de type d’ACE d’espace de noms**</span><span class="sxs-lookup"><span data-stu-id="e59c8-115">**Namespace ACE Type Constants**</span></span>](namespace-ace-type-constants.md)
-   [<span data-ttu-id="e59c8-116">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="e59c8-116">**Privilege Constants**</span></span>](privilege-constants.md)

 

 
