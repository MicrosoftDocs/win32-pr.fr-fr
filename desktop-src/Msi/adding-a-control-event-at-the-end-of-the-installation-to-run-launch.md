---
description: Le programme d’installation exécute la séquence de l’Assistant Installation de l’exemple uniquement si le niveau d’interface utilisateur complet est utilisé pour installer l’application.
ms.assetid: 323d62ae-333b-49fd-96a1-55b228c8ab2c
title: Ajout d’un événement de contrôle à la fin de l’installation pour exécuter le lancement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545901c4cfd0936f63078d5ad56586022fb4ec4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951797"
---
# <a name="adding-a-control-event-at-the-end-of-the-installation-to-run-launch"></a><span data-ttu-id="71c9d-103">Ajout d’un événement de contrôle à la fin de l’installation pour exécuter le lancement</span><span class="sxs-lookup"><span data-stu-id="71c9d-103">Adding a Control Event at the End of the Installation to Run Launch</span></span>

<span data-ttu-id="71c9d-104">Le programme d’installation exécute la séquence de l’Assistant Installation de l’exemple uniquement si le niveau d' [*interface utilisateur complet*](f-gly.md) est utilisé pour installer l’application.</span><span class="sxs-lookup"><span data-stu-id="71c9d-104">The installer runs the sample's installation wizard sequence only if the [*full UI*](f-gly.md) level is used to install the application.</span></span> <span data-ttu-id="71c9d-105">La dernière boîte de dialogue de la séquence de dialogue d’exemple est une [boîte de dialogue de sortie](exit-dialog.md) nommée ExitDialog.</span><span class="sxs-lookup"><span data-stu-id="71c9d-105">The last dialog box of the sample dialog sequence is an [Exit Dialog](exit-dialog.md) named ExitDialog.</span></span> <span data-ttu-id="71c9d-106">Lorsqu’un utilisateur interagit avec le bouton OK sur ExitDialog, il publie d’abord un [ControlEvent, EndDialog](enddialog-controlevent.md) qui retourne le contrôle au programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="71c9d-106">When a user interacts with the OK button on ExitDialog, this first publishes an [EndDialog ControlEvent](enddialog-controlevent.md) that returns control to the installer.</span></span> <span data-ttu-id="71c9d-107">Le contrôle publie ensuite un [ControlEvent, de script](doaction-controlevent.md) qui exécute l’action personnalisée Launch.</span><span class="sxs-lookup"><span data-stu-id="71c9d-107">The control then publishes a [DoAction ControlEvent](doaction-controlevent.md) that runs the Launch custom action.</span></span> <span data-ttu-id="71c9d-108">Chaque événement de contrôle requiert un enregistrement dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="71c9d-108">Each control event requires a record in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="71c9d-109">Consultez [vue d’ensemble de ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="71c9d-109">See [ControlEvent Overview](controlevent-overview.md).</span></span>

[<span data-ttu-id="71c9d-110">Table ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="71c9d-110">ControlEvent Table</span></span>](controlevent-table.md)



| <span data-ttu-id="71c9d-111">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="71c9d-111">Dialog</span></span>     | <span data-ttu-id="71c9d-112">contrôle\_</span><span class="sxs-lookup"><span data-stu-id="71c9d-112">Control\_</span></span> | <span data-ttu-id="71c9d-113">Événement</span><span class="sxs-lookup"><span data-stu-id="71c9d-113">Event</span></span>     | <span data-ttu-id="71c9d-114">Argument</span><span class="sxs-lookup"><span data-stu-id="71c9d-114">Argument</span></span> | <span data-ttu-id="71c9d-115">Condition</span><span class="sxs-lookup"><span data-stu-id="71c9d-115">Condition</span></span>                     | <span data-ttu-id="71c9d-116">Classement</span><span class="sxs-lookup"><span data-stu-id="71c9d-116">Ordering</span></span> |
|------------|-----------|-----------|----------|-------------------------------|----------|
| <span data-ttu-id="71c9d-117">ExitDialog</span><span class="sxs-lookup"><span data-stu-id="71c9d-117">ExitDialog</span></span> | <span data-ttu-id="71c9d-118">Ok</span><span class="sxs-lookup"><span data-stu-id="71c9d-118">OK</span></span>        | <span data-ttu-id="71c9d-119">EndDialog</span><span class="sxs-lookup"><span data-stu-id="71c9d-119">EndDialog</span></span> | <span data-ttu-id="71c9d-120">Renvoie</span><span class="sxs-lookup"><span data-stu-id="71c9d-120">Return</span></span>   | <span data-ttu-id="71c9d-121">1</span><span class="sxs-lookup"><span data-stu-id="71c9d-121">1</span></span>                             | <span data-ttu-id="71c9d-122">1</span><span class="sxs-lookup"><span data-stu-id="71c9d-122">1</span></span>        |
| <span data-ttu-id="71c9d-123">ExitDialog</span><span class="sxs-lookup"><span data-stu-id="71c9d-123">ExitDialog</span></span> | <span data-ttu-id="71c9d-124">Ok</span><span class="sxs-lookup"><span data-stu-id="71c9d-124">OK</span></span>        | <span data-ttu-id="71c9d-125">Action</span><span class="sxs-lookup"><span data-stu-id="71c9d-125">DoAction</span></span>  | <span data-ttu-id="71c9d-126">Lancer</span><span class="sxs-lookup"><span data-stu-id="71c9d-126">Launch</span></span>   | <span data-ttu-id="71c9d-127">NON installé et $Tutorial = 3</span><span class="sxs-lookup"><span data-stu-id="71c9d-127">NOT Installed AND $Tutorial=3</span></span> | <span data-ttu-id="71c9d-128">2</span><span class="sxs-lookup"><span data-stu-id="71c9d-128">2</span></span>        |



 

<span data-ttu-id="71c9d-129">La condition sur le contrôle de script s’assure que l’action personnalisée s’exécute uniquement lors de la première installation de l’application et qu’elle est installée localement.</span><span class="sxs-lookup"><span data-stu-id="71c9d-129">The condition on the DoAction control ensures the custom action only runs during the first installation of the application and that it is being installed locally.</span></span> <span data-ttu-id="71c9d-130">L’expression $Tutorial = 3 signifie que l’état de l’action du composant didacticiel est défini sur local.</span><span class="sxs-lookup"><span data-stu-id="71c9d-130">The phrase $Tutorial=3 means the action state of the Tutorial component is set to local.</span></span> <span data-ttu-id="71c9d-131">Consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="71c9d-131">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="71c9d-132">Cela termine l’exemple.</span><span class="sxs-lookup"><span data-stu-id="71c9d-132">This completes the sample.</span></span>

 

 



