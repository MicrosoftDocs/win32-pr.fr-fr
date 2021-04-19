---
description: La dernière étape de la création d’une page de référence des événements consiste à la tester.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Test d’une page de référence d’événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6afaaec279403922abde578b9e73931e607680f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531669"
---
# <a name="testing-an-event-reference-page"></a><span data-ttu-id="ffb50-103">Test d’une page de référence d’événement</span><span class="sxs-lookup"><span data-stu-id="ffb50-103">Testing an Event Reference Page</span></span>

<span data-ttu-id="ffb50-104">La dernière étape de la création d’une page de référence des événements consiste à la tester.</span><span class="sxs-lookup"><span data-stu-id="ffb50-104">The final step of creating an event reference page (ERP) is to test it.</span></span> <span data-ttu-id="ffb50-105">Vous pouvez tester un ERP en consultant le fichier dans un navigateur HTML, tel que Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ffb50-105">You can test an ERP by viewing the file in an HTML browser such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="ffb50-106">Vous pouvez installer l’ERP et sa DLL d’expert pour le tester pour l’appel d’événement et l’afficher dans le observateur d’événements Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="ffb50-106">Or, you can install the ERP and its expert DLL to test it for event invocation and display it in the Network Monitor Event Viewer.</span></span>

## <a name="viewing-erps-that-have-no-dll"></a><span data-ttu-id="ffb50-107">Affichage des vos solutions ERP qui n’ont pas de DLL</span><span class="sxs-lookup"><span data-stu-id="ffb50-107">Viewing ERPs that Have No DLL</span></span>

<span data-ttu-id="ffb50-108">Pour afficher l’ERP terminé sans DLL d’expert installée, ouvrez le fichier avec une visionneuse HTML qui prend en charge vos sources incorporées.</span><span class="sxs-lookup"><span data-stu-id="ffb50-108">To view the completed ERP without an installed expert DLL, open the file with an HTML viewer that supports your embedded sources.</span></span> <span data-ttu-id="ffb50-109">L’illustration suivante montre l’exemple de fichier ERP décrit dans [écriture d’une ERP](writing-an-event-reference-page.md) telle qu’elle est affichée à l’aide de Microsoft Internet Explorer version 4,01.</span><span class="sxs-lookup"><span data-stu-id="ffb50-109">The following illustration shows the sample ERP file described in [Writing an ERP](writing-an-event-reference-page.md) as it is displayed using Microsoft Internet Explorer Version 4.01.</span></span>

![exemple de fichier ERP](images/ie-erp.png)

<span data-ttu-id="ffb50-111">Test des vos solutions ERP qui ont une DLL</span><span class="sxs-lookup"><span data-stu-id="ffb50-111">Testing ERPs that Have a DLL</span></span>

<span data-ttu-id="ffb50-112">Une fois les fichiers ERP et la dll d' [**expert**](experts.md) créés, vous pouvez tester la fonctionnalité complète de votre vos solutions erp avec moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="ffb50-112">After the ERP files and the [**expert**](experts.md) DLL is created, you can test the complete functionality of your ERPs with Network Monitor.</span></span> <span data-ttu-id="ffb50-113">Il est supposé que la DLL est déboguée et peut générer des événements valides.</span><span class="sxs-lookup"><span data-stu-id="ffb50-113">It is assumed that the DLL is debugged and can generate valid events.</span></span>

<span data-ttu-id="ffb50-114">**Pour tester des vos solutions ERP qui ont une DLL**</span><span class="sxs-lookup"><span data-stu-id="ffb50-114">**To test ERPs that have a DLL**</span></span>

1.  <span data-ttu-id="ffb50-115">Vérifiez que la DLL d’expert appropriée est installée dans le répertoire approprié.</span><span class="sxs-lookup"><span data-stu-id="ffb50-115">Verify that the correct expert DLL is installed in the appropriate directory.</span></span> <span data-ttu-id="ffb50-116">Pour plus d’informations, consultez [installation d’un expert sur Moniteur réseau 2,1](installing-an-expert-to-network-monitor-2-1.md).</span><span class="sxs-lookup"><span data-stu-id="ffb50-116">For more information, see [Installing an Expert to Network Monitor 2.1](installing-an-expert-to-network-monitor-2-1.md).</span></span>
2.  <span data-ttu-id="ffb50-117">Vérifiez le [nom correct](naming-an-event-reference-page.md) du fichier ERP.</span><span class="sxs-lookup"><span data-stu-id="ffb50-117">Verify the [correct name](naming-an-event-reference-page.md) of the ERP file.</span></span>
3.  <span data-ttu-id="ffb50-118">Vérifiez l' [emplacement correct](installing-existing-erps-to-network-monitor-2-1.md) du vos solutions ERP dans le répertoire Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="ffb50-118">Verify the [correct location](installing-existing-erps-to-network-monitor-2-1.md) of the ERPs in the Network Monitor directory.</span></span>
4.  <span data-ttu-id="ffb50-119">Test d’expert vos solutions ERP dans l’interface utilisateur Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="ffb50-119">Test expert ERPs in the Network Monitor UI.</span></span>
5.  <span data-ttu-id="ffb50-120">Générez un événement de test.</span><span class="sxs-lookup"><span data-stu-id="ffb50-120">Generate a test event.</span></span>
6.  <span data-ttu-id="ffb50-121">Vérifiez que l’ERP s’affiche dans le observateur d’événements Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="ffb50-121">Verify that the ERP appears in the Network Monitor Event Viewer.</span></span>

<span data-ttu-id="ffb50-122">Pour plus d’informations sur la création d’une ERP, consultez :</span><span class="sxs-lookup"><span data-stu-id="ffb50-122">For more information about creating an ERP, see:</span></span>

-   [<span data-ttu-id="ffb50-123">Création d’un expert et surveillance des pages de référence des événements</span><span class="sxs-lookup"><span data-stu-id="ffb50-123">Creating Expert and Monitor Event Reference Pages</span></span>](creating-expert-and-monitor-event-reference-pages.md)
-   [<span data-ttu-id="ffb50-124">Écriture d’une page de référence d’événement</span><span class="sxs-lookup"><span data-stu-id="ffb50-124">Writing an Event Reference Page</span></span>](writing-an-event-reference-page.md)
-   [<span data-ttu-id="ffb50-125">Attribution d’un nom à une page de référence d’événement</span><span class="sxs-lookup"><span data-stu-id="ffb50-125">Naming an Event Reference Page</span></span>](naming-an-event-reference-page.md)

 

 



