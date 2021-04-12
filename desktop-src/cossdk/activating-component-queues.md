---
description: Activation des files d’attente de composants
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: Activation des files d’attente de composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13dadad287facd5555b4e1ed84fee9f764b1c32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393052"
---
# <a name="activating-component-queues"></a><span data-ttu-id="43163-103">Activation des files d’attente de composants</span><span class="sxs-lookup"><span data-stu-id="43163-103">Activating Component Queues</span></span>

<span data-ttu-id="43163-104">Le fait d’appeler des méthodes sur un composant en file d’attente n’exécute pas directement la méthode.</span><span class="sxs-lookup"><span data-stu-id="43163-104">Making method calls on a queued component does not directly execute the method.</span></span> <span data-ttu-id="43163-105">Au lieu de cela, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) marshale et stocke les appels de méthode et les paramètres dans une file d’attente où ils sont récupérés et exécutés ultérieurement par le composant mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="43163-105">Rather, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) marshals and stores method calls and parameters in a queue where they are later retrieved and executed by the queued component.</span></span> <span data-ttu-id="43163-106">Contrairement à l’activation d’un objet DCOM distant, le composant mis en file d’attente n’est pas instancié quand une méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="43163-106">Unlike activating a remote DCOM object, the queued component is not instantiated when a method is called.</span></span> <span data-ttu-id="43163-107">Il s’agit de l’idée de base de l’utilisation des composants en file d’attente : les composants en file d’attente n’ont pas besoin d’être instanciés en même temps que l’application appelante.</span><span class="sxs-lookup"><span data-stu-id="43163-107">This is the basic idea behind using queued components—queued components need not be instantiated at the same time as the calling application.</span></span>

> [!Note]  
> <span data-ttu-id="43163-108">Les descriptions d’activation d’une application en file d’attente supposent que l’application est marquée comme étant en file d’attente et que la case à cocher écouteur est activée.</span><span class="sxs-lookup"><span data-stu-id="43163-108">The descriptions for activating a queued application assume that the application is marked as queued and that the listener check box is enabled.</span></span>

 

<span data-ttu-id="43163-109">Vous pouvez utiliser des scripts pour démarrer et arrêter une application en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="43163-109">You can use scripting to start and stop a queued application.</span></span> <span data-ttu-id="43163-110">Vous pouvez placer le script sous le contrôle du planificateur de tâches pour l’exécuter en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="43163-110">You can put the script under the control of the task scheduler to run it as required.</span></span> <span data-ttu-id="43163-111">Par exemple, le script peut être exécuté lors du redémarrage du système si les applications doivent être disponibles de manière permanente.</span><span class="sxs-lookup"><span data-stu-id="43163-111">For example, the script can be run on system reboot if the applications are to be permanently available.</span></span> <span data-ttu-id="43163-112">Si l’application doit traiter les transactions en mode batch, le script peut être exécuté à une heure donnée chaque jour conjointement à un script d’arrêt pour s’assurer que le traitement par lots s’arrête à un moment précis.</span><span class="sxs-lookup"><span data-stu-id="43163-112">If the application is to process transactions in batch mode, the script can be run at a certain time each day in conjunction with a shutdown script to be sure the batch processing stops at a specific time.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="43163-113">Outil d’administration Services de composants</span><span class="sxs-lookup"><span data-stu-id="43163-113">Component Services Administrative Tool</span></span>

<span data-ttu-id="43163-114">Pour démarrer une application en file d’attente, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="43163-114">To start a queued application, use the following steps:</span></span>

1.  <span data-ttu-id="43163-115">Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier **applications com+** associé à l’ordinateur que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="43163-115">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="43163-116">Cliquez avec le bouton droit sur l’application dont vous souhaitez activer la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="43163-116">Right-click the application whose queue you want to activate.</span></span>

3.  <span data-ttu-id="43163-117">Cliquez sur **Start**.</span><span class="sxs-lookup"><span data-stu-id="43163-117">Click **Start**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="43163-118">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="43163-118">Visual Basic</span></span>

<span data-ttu-id="43163-119">Consultez l’exemple COMAdminCatalog. StartApplication.</span><span class="sxs-lookup"><span data-stu-id="43163-119">See the COMAdminCatalog.StartApplication example.</span></span>

## <a name="cc"></a><span data-ttu-id="43163-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="43163-120">C/C++</span></span>

<span data-ttu-id="43163-121">Consultez l’exemple [**ICOMAdminCatalog :: StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) .</span><span class="sxs-lookup"><span data-stu-id="43163-121">See the [**ICOMAdminCatalog::StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43163-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="43163-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43163-123">Utilisation du moniker de la file d’attente</span><span class="sxs-lookup"><span data-stu-id="43163-123">Using the Queue Moniker</span></span>](using-the-queue-moniker.md)
</dt> </dl>

 

 



