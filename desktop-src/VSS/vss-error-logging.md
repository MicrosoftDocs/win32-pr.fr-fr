---
description: 'Les informations d’erreur et d’état VSS suivantes sont écrites dans le journal des événements de l’application :'
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: Journalisation des erreurs VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9822035f36f56162fb6836bf7ad4c09cdd31b777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113182"
---
# <a name="vss-error-logging"></a><span data-ttu-id="72b2b-103">Journalisation des erreurs VSS</span><span class="sxs-lookup"><span data-stu-id="72b2b-103">VSS Error Logging</span></span>

<span data-ttu-id="72b2b-104">Les informations d’erreur et d’état VSS suivantes sont écrites dans le journal des événements de l’application :</span><span class="sxs-lookup"><span data-stu-id="72b2b-104">The following VSS error and state information is written to the Application Event Log:</span></span>

-   <span data-ttu-id="72b2b-105">Erreurs de demandeur produites à l’aide de l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)</span><span class="sxs-lookup"><span data-stu-id="72b2b-105">Requester errors produced using the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface</span></span>
-   <span data-ttu-id="72b2b-106">Erreurs d’écriture produites dans à l’aide de la classe [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) , y compris les méthodes de substitution</span><span class="sxs-lookup"><span data-stu-id="72b2b-106">Writer errors produced in using the [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) class, including overriding methods</span></span>
-   <span data-ttu-id="72b2b-107">Erreurs générées par le fournisseur par défaut</span><span class="sxs-lookup"><span data-stu-id="72b2b-107">Default-provider-generated errors</span></span>
-   <span data-ttu-id="72b2b-108">Erreurs de service VSS générées dans le fournisseur de coordination, l’enregistreur et l’activité du demandeur (par exemple, la génération d’événements)</span><span class="sxs-lookup"><span data-stu-id="72b2b-108">VSS service errors generated in coordinating provider, writer, and requester activity (such as the generation of events)</span></span>

<span data-ttu-id="72b2b-109">Ces erreurs peuvent avoir plusieurs causes, y compris une erreur de programmation dans du code tiers ou des erreurs de configuration liées à VSS.</span><span class="sxs-lookup"><span data-stu-id="72b2b-109">These errors might have a number of causes, including a programming error in third-party code or VSS-related configuration errors.</span></span>

<span data-ttu-id="72b2b-110">Les pilotes VSS et les fonctionnalités d’implémentation de niveau inférieur écrivent des erreurs dans le journal système.</span><span class="sxs-lookup"><span data-stu-id="72b2b-110">VSS drivers and lower-level implementation functionality write errors to the System Log.</span></span> <span data-ttu-id="72b2b-111">Les logiciels tiers (demandeur, fournisseur, rédacteur) peuvent choisir le journal des applications, le journal système, ou les deux, pour écrire les entrées du journal des erreurs.</span><span class="sxs-lookup"><span data-stu-id="72b2b-111">Third-party software (requester, provider, writer) can choose the Application Log, the System Log, or both, to write error log entries.</span></span>

<span data-ttu-id="72b2b-112">Il est recommandé que les applications de haut niveau (telles que le code en mode utilisateur) utilisent le journal des applications.</span><span class="sxs-lookup"><span data-stu-id="72b2b-112">It is recommended that high-level applications (such as user-mode code) use the Application Log.</span></span> <span data-ttu-id="72b2b-113">Les applications de niveau inférieur, telles que les interfaces et les pilotes matériels, doivent utiliser le journal système.</span><span class="sxs-lookup"><span data-stu-id="72b2b-113">Lower-level applications, such as hardware interfaces and drivers, should use the System Log.</span></span>

 

 



