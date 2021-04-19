---
description: Vous fournissez l’espace de noms LDAP (Lightweight Directory Access Protocol) et les chemins d’accès de l’interface Active Directory Services (ADSI) lors de l’appel du fournisseur Active Directory via WMI.
ms.assetid: 55733fba-2170-4400-a516-896f6bf9525a
ms.tgt_platform: multiple
title: Utilisation de la syntaxe de Active Directory appropriée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e321d6919c48103be930226cf11c4b3e82dcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536995"
---
# <a name="using-the-proper-active-directory-syntax"></a><span data-ttu-id="3e9d2-103">Utilisation de la syntaxe de Active Directory appropriée</span><span class="sxs-lookup"><span data-stu-id="3e9d2-103">Using the Proper Active Directory Syntax</span></span>

<span data-ttu-id="3e9d2-104">Vous fournissez l’espace de noms LDAP (Lightweight Directory Access Protocol) et les chemins d’accès de l’interface Active Directory Services (ADSI) lors de l’appel du [fournisseur Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider) via WMI.</span><span class="sxs-lookup"><span data-stu-id="3e9d2-104">You supply the Lightweight Directory Access Protocol (LDAP) namespace and Active Directory Services Interface (ADSI) paths when calling the [Active Directory Provider](/previous-versions/windows/desktop/dsprov/active-directory-provider) through WMI.</span></span>

<span data-ttu-id="3e9d2-105">Les rubriques suivantes décrivent l’espace de noms LDAP et le chemin d’accès ADSI :</span><span class="sxs-lookup"><span data-stu-id="3e9d2-105">The following topics describe the LDAP namespace and the ADSI path:</span></span>

-   [<span data-ttu-id="3e9d2-106">Description de l’espace de noms LDAP</span><span class="sxs-lookup"><span data-stu-id="3e9d2-106">Describing the LDAP Namespace</span></span>](describing-the-ldap-namespace.md)

    <span data-ttu-id="3e9d2-107">Un chemin d’accès d’espace de noms décrit l’emplacement d’un espace de noms distant.</span><span class="sxs-lookup"><span data-stu-id="3e9d2-107">A namespace path describes the location of a remote namespace.</span></span> <span data-ttu-id="3e9d2-108">Utilisez le chemin d’accès de l’espace de noms pour vous connecter à distance à un espace de noms Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3e9d2-108">Use the namespace path to connect remotely to an Active Directory namespace.</span></span>

-   [<span data-ttu-id="3e9d2-109">Description du chemin d’accès ADSI</span><span class="sxs-lookup"><span data-stu-id="3e9d2-109">Describing the ADSI Path</span></span>](describing-the-adsi-path.md)

    <span data-ttu-id="3e9d2-110">Le chemin d’accès ADSI décrit l’emplacement d’un objet à l’aide de l’API ADSI.</span><span class="sxs-lookup"><span data-stu-id="3e9d2-110">The ADSI path describes the location of an object using the ADSI API.</span></span> <span data-ttu-id="3e9d2-111">Utilisez le chemin d’accès ADSI dans les paramètres que le fournisseur passe sur Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3e9d2-111">Use the ADSI path in parameters that the provider passes onto Active Directory.</span></span>

> [!Note]  
> <span data-ttu-id="3e9d2-112">Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="3e9d2-112">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 
