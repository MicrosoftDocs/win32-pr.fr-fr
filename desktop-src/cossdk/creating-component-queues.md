---
description: Une application qui contient au moins un composant peut être marquée comme en file d’attente à l’aide de l’outil d’administration Services de composants.
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Création de files d’attente de composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc6f6731144a1744a7648d2d3d2bd5c3c4b217b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516375"
---
# <a name="creating-component-queues"></a><span data-ttu-id="3c145-103">Création de files d’attente de composants</span><span class="sxs-lookup"><span data-stu-id="3c145-103">Creating Component Queues</span></span>

<span data-ttu-id="3c145-104">Une application qui contient au moins un composant peut être marquée comme en file d’attente à l’aide de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="3c145-104">An application that contains at least one queuable component can be marked as queued using the component services administrative tool.</span></span>

<span data-ttu-id="3c145-105">Lorsqu’une application est marquée comme en file d’attente, COM+ crée automatiquement une file d’attente Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="3c145-105">When an application is marked as queued, COM+ automatically creates a message queuing queue for it.</span></span> <span data-ttu-id="3c145-106">Le nom de la file d’attente est le nom de l’application ; Si le nom de la file d’attente correspond au nom d’une file d’attente existante, COM+ utilise la file d’attente existante.</span><span class="sxs-lookup"><span data-stu-id="3c145-106">The queue name is the name of the application; if the queue name matches the name of an existing queue, COM+ will use the existing queue.</span></span>

> [!Note]  
> <span data-ttu-id="3c145-107">Le paramètre Message Queuing *pathname* est une combinaison du nom de serveur distant (RSN) et du nom de l’application com+.</span><span class="sxs-lookup"><span data-stu-id="3c145-107">The Message Queuing *PathName* parameter is a combination of the Remote Server Name (RSN) and the COM+ application name.</span></span> <span data-ttu-id="3c145-108">Le RSN fait référence à la cible d’une activation à distance.</span><span class="sxs-lookup"><span data-stu-id="3c145-108">The RSN refers to the target of a remote activation.</span></span> <span data-ttu-id="3c145-109">Vous spécifiez un RSN lors de l’installation d’une application cliente exportable sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="3c145-109">You specify an RSN during the installation of a client exportable application on a client computer.</span></span> <span data-ttu-id="3c145-110">La procédure d’installation utilise le RSN pour diriger l’activation vers un ordinateur client spécifié.</span><span class="sxs-lookup"><span data-stu-id="3c145-110">The installation procedure uses the RSN to direct activation to a specified client computer.</span></span> <span data-ttu-id="3c145-111">Pour plus d’informations sur les noms de files d’attente, reportez-vous à la table de paramètres dans la section « paramètres de moniker de la file d’attente » dans [utilisation du moniker de la file d’attente](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="3c145-111">For more information about queue names, refer to the table of parameters in the "Queue Moniker Parameters" section in [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="3c145-112">Outil d’administration Services de composants</span><span class="sxs-lookup"><span data-stu-id="3c145-112">Component Services Administrative Tool</span></span>

<span data-ttu-id="3c145-113">Pour spécifier une application COM+ en file d’attente, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3c145-113">To specify a COM+ application as queued, use the following steps:</span></span>

1.  <span data-ttu-id="3c145-114">Dans l’arborescence de la console de l’outil d’administration Services de composants, sous **services de composants**, ouvrez le dossier **applications com+** associé à l’ordinateur que vous souhaitez gérer.</span><span class="sxs-lookup"><span data-stu-id="3c145-114">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="3c145-115">Cliquez avec le bouton droit sur l’application pour laquelle vous souhaitez créer une file d’attente, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="3c145-115">Right-click the application for which you wish to create a queue, and then click **Properties**.</span></span>

3.  <span data-ttu-id="3c145-116">Sélectionnez l’onglet mise en **file d’attente** dans la boîte de dialogue Propriétés.</span><span class="sxs-lookup"><span data-stu-id="3c145-116">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="3c145-117">Activez la case à cocher **en attente : cette application est accessible par les files d’attente MSMQ**.</span><span class="sxs-lookup"><span data-stu-id="3c145-117">Activate the check box labeled **Queued – This application can be reached by MSMQ queues**.</span></span>

    > [!Note]  
    > <span data-ttu-id="3c145-118">Si la case à cocher en attente est grisée, l’application ne contient aucun composant de la mise en **file d’attente** .</span><span class="sxs-lookup"><span data-stu-id="3c145-118">If the **Queued** check box is grayed out, the application contains no queuable components.</span></span>

     

5.  <span data-ttu-id="3c145-119">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c145-119">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="3c145-120">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3c145-120">Visual Basic</span></span>

<span data-ttu-id="3c145-121">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="3c145-121">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="3c145-122">C/C++</span><span class="sxs-lookup"><span data-stu-id="3c145-122">C/C++</span></span>

<span data-ttu-id="3c145-123">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="3c145-123">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c145-124">Notes</span><span class="sxs-lookup"><span data-stu-id="3c145-124">Remarks</span></span>

<span data-ttu-id="3c145-125">Les files d’attente créées par la bibliothèque d’administration COM+ ou l’outil d’administration Services de composants sont marquées avec l’attribut transactionnel Message Queuing.</span><span class="sxs-lookup"><span data-stu-id="3c145-125">Queues created by the COM+ Administration Library or the Component Services administrative tool are marked with the Message Queuing transactional attribute.</span></span>

<span data-ttu-id="3c145-126">Une fois qu’une application en file d’attente est installée sur le serveur, elle peut être mise à la disposition des clients en exportant l’application, puis en important l’application sur chaque client.</span><span class="sxs-lookup"><span data-stu-id="3c145-126">After a queued application is installed at the server, it can be made available to clients by exporting the application and then importing the application at each client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c145-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3c145-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c145-128">Création de composants de mise en file d’attente</span><span class="sxs-lookup"><span data-stu-id="3c145-128">Creating Queuable Components</span></span>](creating-queuable-components.md)
</dt> <dt>

[<span data-ttu-id="3c145-129">Architecture des composants en file d’attente</span><span class="sxs-lookup"><span data-stu-id="3c145-129">Queued Components Architecture</span></span>](queued-components-architecture.md)
</dt> </dl>

 

 



