---
description: Cette section décrit comment planifier, développer et tester les pages de référence des événements (vos solutions ERP) et comment les déployer dans un expert ou une analyse. Pour plus d’informations sur les vos solutions ERP et leur utilisation avec Moniteur réseau, consultez la page de référence des événements.
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: Création d’un expert et surveillance des pages de référence des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c84610c7a1088e994fc852c64a7893f73f7909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517062"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a><span data-ttu-id="d4402-104">Création d’un expert et surveillance des pages de référence des événements</span><span class="sxs-lookup"><span data-stu-id="d4402-104">Creating Expert and Monitor Event Reference Pages</span></span>

<span data-ttu-id="d4402-105">Cette section décrit comment planifier, développer et tester les pages de référence des événements (vos solutions ERP) et comment les déployer dans un expert ou une analyse.</span><span class="sxs-lookup"><span data-stu-id="d4402-105">This section describes how to plan, develop, and test event reference pages (ERPs) and how to deploy them in an expert or monitor.</span></span> <span data-ttu-id="d4402-106">Pour plus d’informations sur les vos solutions ERP et leur utilisation avec Moniteur réseau, consultez la [page de référence des événements](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="d4402-106">For information about ERPs and how to use them with Network Monitor, see [Event Reference Page](event-reference-page.md).</span></span>

<span data-ttu-id="d4402-107">Pour développer un nouvel ERP, la première étape consiste à déterminer les événements qui requièrent des vos solutions ERP individuels pour votre [expert](experts.md) ou votre [moniteur](monitors.md)personnalisé.</span><span class="sxs-lookup"><span data-stu-id="d4402-107">To develop a new ERP, the first step is determining the events that require individual ERPs for your custom [expert](experts.md) or [monitor](monitors.md).</span></span> <span data-ttu-id="d4402-108">Vous devez créer des vos solutions ERP distincts pour chaque événement que vous souhaitez afficher dans le observateur d’événements Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="d4402-108">You must create separate ERPs for each event you wish to display in the Network Monitor Event Viewer.</span></span> <span data-ttu-id="d4402-109">Par exemple, supposons que :</span><span class="sxs-lookup"><span data-stu-id="d4402-109">For example, suppose that:</span></span>

-   <span data-ttu-id="d4402-110">Vous développez un moniteur nommé Game Monitor et stock Watcher.</span><span class="sxs-lookup"><span data-stu-id="d4402-110">You develop a monitor named Game Monitor and Stock Watcher.</span></span>
-   <span data-ttu-id="d4402-111">Le moniteur se trouve dans un fichier appelé Gamemon.dll.</span><span class="sxs-lookup"><span data-stu-id="d4402-111">The monitor is located in a file called Gamemon.dll.</span></span>
-   <span data-ttu-id="d4402-112">Le moniteur génère deux événements : le jeu est en cours d’exécution et mes raccourcis d’inventaire Internet.</span><span class="sxs-lookup"><span data-stu-id="d4402-112">The monitor generates two events, Game Running and My Internet Stock Soars.</span></span>
-   <span data-ttu-id="d4402-113">Vous envisagez de développer deux vos solutions ERP, Gamemon1.htm et Gamemon2.htm.</span><span class="sxs-lookup"><span data-stu-id="d4402-113">You plan to develop two ERPs, Gamemon1.htm and Gamemon2.htm.</span></span>

> [!Note]  
> <span data-ttu-id="d4402-114">Il n’est pas nécessaire d’avoir une correspondance un-à-un entre les vos solutions ERP et les événements d’experts.</span><span class="sxs-lookup"><span data-stu-id="d4402-114">It's not necessary to have a one-to-one correspondence of ERPs to monitor or expert events.</span></span>

 

<span data-ttu-id="d4402-115">Une fois que vous avez établi une liste de vos solutions ERP uniques, procédez comme suit pour créer chaque ERP.</span><span class="sxs-lookup"><span data-stu-id="d4402-115">After you have established a list of unique ERPs, follow these steps to create each ERP.</span></span>

-   <span data-ttu-id="d4402-116">[Écrivez le document source HTML](writing-an-event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="d4402-116">[Write the HTML source document](writing-an-event-reference-page.md).</span></span>
-   <span data-ttu-id="d4402-117">[Enregistrez et nommez](naming-an-event-reference-page.md) le fichier source HTML en tant que fichier. htm.</span><span class="sxs-lookup"><span data-stu-id="d4402-117">[Save and name](naming-an-event-reference-page.md) the HTML source file as an .htm file.</span></span>
-   <span data-ttu-id="d4402-118">[Testez l’ERP](testing-an-event-reference-page.md) avec l’expert ou l’analyse terminé.</span><span class="sxs-lookup"><span data-stu-id="d4402-118">[Test the ERP](testing-an-event-reference-page.md) with the completed expert or monitor.</span></span>

 

 



