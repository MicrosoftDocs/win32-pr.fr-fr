---
description: Windows Installer est intégré à la stratégie de restriction logicielle dans Microsoft Windows XP.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Installer et stratégie de restriction logicielle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b080a1ed9a1396f4ac212e73d1fda6e2719bf40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533958"
---
# <a name="windows-installer-and-software-restriction-policy"></a><span data-ttu-id="eb733-103">Windows Installer et stratégie de restriction logicielle</span><span class="sxs-lookup"><span data-stu-id="eb733-103">Windows Installer and Software Restriction Policy</span></span>

<span data-ttu-id="eb733-104">Windows Installer est intégré à la stratégie de restriction logicielle dans Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="eb733-104">Windows Installer is integrated with Software Restriction Policy in Microsoft Windows XP.</span></span> <span data-ttu-id="eb733-105">La stratégie de restriction logicielle est configurable via la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="eb733-105">Software Restriction Policy is configurable through group policy.</span></span> <span data-ttu-id="eb733-106">La stratégie de restriction logicielle permet à un administrateur de limiter les administrateurs et les non-administrateurs à l’exécution de fichiers en fonction du chemin d’accès, de la zone d’URL, du hachage ou des critères du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="eb733-106">Software Restriction Policy allows an administrator to restrict both administrators and nonadministrators from running files based upon the path, URL zone, hash, or publisher criteria.</span></span> <span data-ttu-id="eb733-107">La stratégie de restriction logicielle a deux niveaux : non restreint et interdit.</span><span class="sxs-lookup"><span data-stu-id="eb733-107">Software Restriction Policy has two levels: unrestricted and disallowed.</span></span> <span data-ttu-id="eb733-108">Le Windows Installer installe uniquement les packages autorisés à s’exécuter au niveau non restreint.</span><span class="sxs-lookup"><span data-stu-id="eb733-108">The Windows Installer only installs packages allowed to run at the unrestricted level.</span></span>

<span data-ttu-id="eb733-109">Les correctifs ou les transformations doivent également être autorisés à s’exécuter au niveau non restreint.</span><span class="sxs-lookup"><span data-stu-id="eb733-109">Patches or transforms must also be allowed to run at the unrestricted level.</span></span> <span data-ttu-id="eb733-110">Si un package, un correctif ou une transformation est configuré pour s’exécuter à un niveau différent de non restreint, le Windows Installer affiche un message d’erreur et enregistre une entrée dans le journal des événements de l’application.</span><span class="sxs-lookup"><span data-stu-id="eb733-110">If a package, patch, or transform is configured to run at a level different from unrestricted, the Windows Installer displays an error message and logs an entry in the application event log.</span></span> <span data-ttu-id="eb733-111">La stratégie de restriction logicielle est évaluée lors de la première installation d’une application, lors de l’application d’un nouveau correctif, et lors de la remise en cache du package d’installation.</span><span class="sxs-lookup"><span data-stu-id="eb733-111">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="eb733-112">Si un package, un correctif ou une transformation est limité, le Windows Installer affiche un message d’erreur et écrit une entrée de [journalisation des événements](event-logging.md) dans le journal des événements de l’application.</span><span class="sxs-lookup"><span data-stu-id="eb733-112">If a package, patch, or transform is restricted, the Windows Installer displays an error message and writes an [Event Logging](event-logging.md) entry in the application event log.</span></span> <span data-ttu-id="eb733-113">La stratégie de restriction logicielle est évaluée lors de la première installation d’une application, lors de l’application d’un nouveau correctif, et lors de la remise en cache du package d’installation.</span><span class="sxs-lookup"><span data-stu-id="eb733-113">Software restriction policy is evaluated the first time an application is installed, when a new patch is applied, and when the installation package is re-cached.</span></span>

<span data-ttu-id="eb733-114">Pour plus d’informations sur la stratégie de restriction logicielle, consultez la documentation du produit et [recherchez sur le site TechNet](https://www.microsoft.com/technet/sitemap.mspx).</span><span class="sxs-lookup"><span data-stu-id="eb733-114">For more information on software restriction policy, consult the product documentation and [search the TechNet Site](https://www.microsoft.com/technet/sitemap.mspx).</span></span>

 

 



