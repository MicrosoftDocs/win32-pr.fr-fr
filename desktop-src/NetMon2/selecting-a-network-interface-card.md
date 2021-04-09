---
description: Moniteur réseau fournit trois fonctions de sélection d’une carte d’interface réseau (NIC). Ces fonctions offrent trois façons d’énumérer un ensemble de cartes réseau et de sélectionner celle que vous souhaitez utiliser. Le tableau suivant répertorie ces fonctions.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Sélection d’une carte d’interface réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8315a97cc8457d86614fc25c87c39b1b9794c7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115075"
---
# <a name="selecting-a-network-interface-card"></a><span data-ttu-id="46dcb-105">Sélection d’une carte d’interface réseau</span><span class="sxs-lookup"><span data-stu-id="46dcb-105">Selecting a Network Interface Card</span></span>

<span data-ttu-id="46dcb-106">Moniteur réseau fournit trois fonctions de sélection d’une carte d’interface réseau (NIC).</span><span class="sxs-lookup"><span data-stu-id="46dcb-106">Network Monitor provides three functions for selecting a network interface card (NIC).</span></span> <span data-ttu-id="46dcb-107">Ces fonctions offrent trois façons d’énumérer un ensemble de cartes réseau et de sélectionner celle que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="46dcb-107">These functions provide three ways to enumerate a set of NICs and select the one you want to use.</span></span> <span data-ttu-id="46dcb-108">Le tableau suivant répertorie ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="46dcb-108">The following table lists these functions.</span></span>



| <span data-ttu-id="46dcb-109">Fonction</span><span class="sxs-lookup"><span data-stu-id="46dcb-109">Function</span></span>                                                 | <span data-ttu-id="46dcb-110">Description</span><span class="sxs-lookup"><span data-stu-id="46dcb-110">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46dcb-111">**GetNPPBlobFromUI**</span><span class="sxs-lookup"><span data-stu-id="46dcb-111">**GetNPPBlobFromUI**</span></span>](getnppblobfromui.md)             | <span data-ttu-id="46dcb-112">Utilise l’interface utilisateur Moniteur réseau pour afficher les cartes réseau enregistrées et retourne l’objet BLOB NPP qui représente la carte réseau qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="46dcb-112">Uses the Network Monitor UI to display the registered NICs and returns the NPP BLOB that represents the NIC you are interested in.</span></span>           |
| [<span data-ttu-id="46dcb-113">**GetNPPBlobTable**</span><span class="sxs-lookup"><span data-stu-id="46dcb-113">**GetNPPBlobTable**</span></span>](getnppblobtable.md)               | <span data-ttu-id="46dcb-114">Retourne une table d’objets BLOB.</span><span class="sxs-lookup"><span data-stu-id="46dcb-114">Returns a BLOB table.</span></span> <span data-ttu-id="46dcb-115">L’application doit énumérer la table et sélectionner un objet BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="46dcb-115">The application must enumerate the table and select an NPP BLOB.</span></span>                                                       |
| [<span data-ttu-id="46dcb-116">**SelectNPPBlobFromTable**</span><span class="sxs-lookup"><span data-stu-id="46dcb-116">**SelectNPPBlobFromTable**</span></span>](selectnppblobfromtable.md) | <span data-ttu-id="46dcb-117">Utilise l’interface Moniteur réseau pour afficher les objets BLOB NPP fournis et retourne l’objet BLOB NPP qui représente la carte réseau qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="46dcb-117">Uses the Network Monitor interface to display the supplied NPP BLOBs and returns the NPP BLOB that represents the NIC you are interested in.</span></span> |



 

<span data-ttu-id="46dcb-118">Chaque carte d’interface réseau est représentée par un objet BLOB (Binary Large Object) NPP.</span><span class="sxs-lookup"><span data-stu-id="46dcb-118">Each NIC is represented by an NPP binary large object (BLOB).</span></span> <span data-ttu-id="46dcb-119">Ces fonctions peuvent retourner un seul objet BLOB NPP à partir de ceux inscrits sur l’ordinateur, un seul objet BLOB NPP à partir d’une table d’objets BLOB NPP fournie, ou une table d’objets BLOB NPP que l’appelant doit ensuite utiliser pour sélectionner un objet BLOB spécifique.</span><span class="sxs-lookup"><span data-stu-id="46dcb-119">These functions can return a single NPP BLOB from those registered on the computer, a single NPP BLOB from a supplied NPP BLOB table, or a table of NPP BLOBs that the caller must then use to select a specific BLOB.</span></span> <span data-ttu-id="46dcb-120">Dans les deux premiers cas, lors de la sélection à partir des cartes réseau inscrites ou d’une table d’objets BLOB NPP fournie, l’interface utilisateur Moniteur réseau affiche les cartes réseau que vous pouvez sélectionner.</span><span class="sxs-lookup"><span data-stu-id="46dcb-120">In the first two cases, when selecting from the registered NICs or from a supplied NPP BLOB table, the Network Monitor UI displays the NICs you can select.</span></span>

> [!Note]  
> <span data-ttu-id="46dcb-121">Moniteur réseau utilise une fonctionnalité appelée « NPP Finder » pour énumérer les cartes réseau inscrites sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="46dcb-121">Network Monitor uses a feature called the NPP Finder to enumerate the NICs registered on the local computer.</span></span> <span data-ttu-id="46dcb-122">Le Finder NPP est un composant de Npptools.dll.</span><span class="sxs-lookup"><span data-stu-id="46dcb-122">The NPP Finder is a component of Npptools.dll.</span></span>

 



| <span data-ttu-id="46dcb-123">Pour obtenir des informations sur</span><span class="sxs-lookup"><span data-stu-id="46dcb-123">For information about</span></span>                            | <span data-ttu-id="46dcb-124">Consultez</span><span class="sxs-lookup"><span data-stu-id="46dcb-124">See</span></span>                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46dcb-125">Sélection d’une carte d’interface réseau inscrite sur l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="46dcb-125">Selecting a NIC registered on the local computer</span></span> | [<span data-ttu-id="46dcb-126">Sélection d’une carte réseau enregistrée</span><span class="sxs-lookup"><span data-stu-id="46dcb-126">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="46dcb-127">Sélection d’une carte d’interface réseau à partir d’une table d’objets BLOB NPP fournie</span><span class="sxs-lookup"><span data-stu-id="46dcb-127">Selecting a NIC from a supplied NPP BLOB table</span></span>   | [<span data-ttu-id="46dcb-128">Sélection d’une carte d’interface réseau à partir d’une table d’objets BLOB NPP fournie</span><span class="sxs-lookup"><span data-stu-id="46dcb-128">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| <span data-ttu-id="46dcb-129">Récupération d’une table d’objets BLOB NPP</span><span class="sxs-lookup"><span data-stu-id="46dcb-129">Retrieving an NPP BLOB table</span></span>                     | [<span data-ttu-id="46dcb-130">Sélection d’une carte d’interface réseau à partir d’une table BLOB NPP retournée</span><span class="sxs-lookup"><span data-stu-id="46dcb-130">Selecting a NIC from a Returned NPP BLOB table</span></span>](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



