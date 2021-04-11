---
title: À propos de la mise en réseau Windows
description: Les applications peuvent utiliser les fonctions WNet pour ajouter et annuler des connexions réseau et récupérer des informations sur la configuration actuelle du réseau.
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- Mise en réseau Windows WNet, Description
- WNet WNet, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91f7c8f58d4e44439bac18a2b7d7b850b21f955
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029816"
---
# <a name="about-windows-networking"></a><span data-ttu-id="d2e04-105">À propos de la mise en réseau Windows</span><span class="sxs-lookup"><span data-stu-id="d2e04-105">About Windows Networking</span></span>

<span data-ttu-id="d2e04-106">Les applications peuvent utiliser les fonctions WNet pour ajouter et annuler des connexions réseau et récupérer des informations sur la configuration actuelle du réseau.</span><span class="sxs-lookup"><span data-stu-id="d2e04-106">Applications can use the WNet functions to add and cancel network connections and to retrieve information about the current configuration of the network.</span></span>

<span data-ttu-id="d2e04-107">L’illustration suivante montre la structure d’un réseau classique.</span><span class="sxs-lookup"><span data-stu-id="d2e04-107">The following figure shows the structure of a typical network.</span></span>

![structure de réseau classique](images/csnet-01.png)

<span data-ttu-id="d2e04-109">Dans la figure précédente, la hiérarchie pour les ressources du serveur Windows NT Server/Windows 2000 est fournie en détail en tant que fournisseur réseau \# 1.</span><span class="sxs-lookup"><span data-stu-id="d2e04-109">In the preceding figure, the hierarchy for Windows NT Server/Windows 2000 Server resources is given in detail as Network provider \#1.</span></span> <span data-ttu-id="d2e04-110">Les ressources réseau d’autres fournisseurs ont des systèmes hiérarchiques différents.</span><span class="sxs-lookup"><span data-stu-id="d2e04-110">Network resources from other providers have different hierarchical systems.</span></span> <span data-ttu-id="d2e04-111">Une application n’a pas besoin d’informations sur la hiérarchie avant de commencer à travailler sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="d2e04-111">An application does not need information about the hierarchy before it begins to work with a network.</span></span> <span data-ttu-id="d2e04-112">Elle peut être exécutée à partir de la racine du réseau (autrement dit, la ressource conteneur la plus grande) et récupérer des informations sur les ressources du réseau, car les informations sont requises.</span><span class="sxs-lookup"><span data-stu-id="d2e04-112">It can proceed from the network root (that is, the topmost container resource) and retrieve information about the network's resources as the information is required.</span></span>

<span data-ttu-id="d2e04-113">Les ressources réseau qui contiennent d’autres ressources sont appelées *conteneurs*.</span><span class="sxs-lookup"><span data-stu-id="d2e04-113">Network resources that contain other resources are called *containers*.</span></span> <span data-ttu-id="d2e04-114">Les ressources de conteneur se trouvent dans les champs de la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="d2e04-114">Container resources are in boxes in the preceding figure.</span></span>

<span data-ttu-id="d2e04-115">Les ressources qui ne contiennent pas d’autres ressources sont appelées *objets*.</span><span class="sxs-lookup"><span data-stu-id="d2e04-115">Resources that do not contain other resources are called *objects*.</span></span> <span data-ttu-id="d2e04-116">Dans la figure précédente, SharePoint \# 1 et SharePoint \# 2 sont des objets.</span><span class="sxs-lookup"><span data-stu-id="d2e04-116">In the preceding figure, Sharepoint \#1 and Sharepoint \#2 are objects.</span></span> <span data-ttu-id="d2e04-117">*SharePoint* est un objet accessible sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="d2e04-117">A *sharepoint* is an object that is accessible across the network.</span></span> <span data-ttu-id="d2e04-118">Les imprimantes et les répertoires partagés sont des exemples de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d2e04-118">Examples of sharepoints include printers and shared directories.</span></span>

 

 




