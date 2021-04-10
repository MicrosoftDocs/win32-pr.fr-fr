---
description: Les fonctions suivantes sont les points d’entrée pour les dll d’experts et les appels du système d’exploitation et Moniteur réseau.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Fonctions d’exportation de DLL d’experts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923611521b98619b357eb2de93ee2269caf9c838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950978"
---
# <a name="expert-dll-export-functions"></a><span data-ttu-id="f0110-103">Fonctions d’exportation de DLL d’experts</span><span class="sxs-lookup"><span data-stu-id="f0110-103">Expert DLL Export Functions</span></span>

<span data-ttu-id="f0110-104">Les fonctions suivantes sont les points d’entrée pour les dll d’experts et les appels du système d’exploitation et Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="f0110-104">The following functions are the entry points for expert DLLs and for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="f0110-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="f0110-105">Function</span></span>                                   | <span data-ttu-id="f0110-106">Description</span><span class="sxs-lookup"><span data-stu-id="f0110-106">Description</span></span>                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0110-107">**Expert DllMain**</span><span class="sxs-lookup"><span data-stu-id="f0110-107">**DllMain Expert**</span></span>](dllmain-expert.md)   | <span data-ttu-id="f0110-108">Indique que la DLL d’expert a été chargée ou déchargée.</span><span class="sxs-lookup"><span data-stu-id="f0110-108">Indicates that the expert DLL has been loaded or unloaded.</span></span> <span data-ttu-id="f0110-109">Lorsqu’un processus charge ou décharge la DLL, le système d’exploitation appelle la fonction [**DllMain**](/windows/desktop/Dlls/dllmain) .</span><span class="sxs-lookup"><span data-stu-id="f0110-109">When a process loads or unloads the DLL, the operating system calls the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> |
| [<span data-ttu-id="f0110-110">**Inscrire un expert**</span><span class="sxs-lookup"><span data-stu-id="f0110-110">**Register Expert**</span></span>](register-expert.md) | <span data-ttu-id="f0110-111">Détermine les informations de base sur l’expert au sein de la DLL.</span><span class="sxs-lookup"><span data-stu-id="f0110-111">Determines basic information about the expert within the DLL.</span></span> <span data-ttu-id="f0110-112">Moniteur réseau appelle la fonction **Register** .</span><span class="sxs-lookup"><span data-stu-id="f0110-112">Network Monitor calls the **Register** function.</span></span>                                                           |
| [<span data-ttu-id="f0110-113">**Configurer**</span><span class="sxs-lookup"><span data-stu-id="f0110-113">**Configure**</span></span>](configure.md)             | <span data-ttu-id="f0110-114">Configure l’expert dans la DLL.</span><span class="sxs-lookup"><span data-stu-id="f0110-114">Configures the expert within the DLL.</span></span> <span data-ttu-id="f0110-115">Moniteur réseau appelle la fonction de [**configuration**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="f0110-115">Network Monitor calls the [**Configure**](configure.md) function.</span></span>                                                                 |
| [<span data-ttu-id="f0110-116">**Utilisez**</span><span class="sxs-lookup"><span data-stu-id="f0110-116">**Run**</span></span>](run.md)                         | <span data-ttu-id="f0110-117">Démarre l’expert dans la DLL.</span><span class="sxs-lookup"><span data-stu-id="f0110-117">Starts the expert within the DLL.</span></span> <span data-ttu-id="f0110-118">Moniteur réseau appelle la fonction [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="f0110-118">Network Monitor calls the [**Run**](run.md) function.</span></span>                                                                                 |



 

<span data-ttu-id="f0110-119">Moniteur réseau fournit également des structures, des énumérations et des fonctions d’assistance que l’expert peut appeler.</span><span class="sxs-lookup"><span data-stu-id="f0110-119">Network Monitor also provides structures, enumerations, and helper functions that the expert can call.</span></span>



| <span data-ttu-id="f0110-120">Pour obtenir des informations sur</span><span class="sxs-lookup"><span data-stu-id="f0110-120">For information about</span></span>                                      | <span data-ttu-id="f0110-121">Consultez</span><span class="sxs-lookup"><span data-stu-id="f0110-121">See</span></span>                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f0110-122">Fonctions d’assistance qui peuvent être appelées par des experts et des analyseurs</span><span class="sxs-lookup"><span data-stu-id="f0110-122">Helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="f0110-123">Fonctions courantes des experts et de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="f0110-123">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="f0110-124">Fonctions d’assistance appelées uniquement par des experts</span><span class="sxs-lookup"><span data-stu-id="f0110-124">Helper functions that are called only by experts</span></span>           | [<span data-ttu-id="f0110-125">Fonctions d’experts</span><span class="sxs-lookup"><span data-stu-id="f0110-125">Expert Functions</span></span>](expert-functions.md)                                     |
| <span data-ttu-id="f0110-126">Structures utilisées par les fonctions d’experts</span><span class="sxs-lookup"><span data-stu-id="f0110-126">Structures that are used by expert functions</span></span>               | [<span data-ttu-id="f0110-127">Structures d’experts</span><span class="sxs-lookup"><span data-stu-id="f0110-127">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="f0110-128">Énumérations utilisées par les structures et fonctions d’experts</span><span class="sxs-lookup"><span data-stu-id="f0110-128">Enumerations used by expert structures and functions</span></span>       | [<span data-ttu-id="f0110-129">Énumérations d’experts</span><span class="sxs-lookup"><span data-stu-id="f0110-129">Expert Enumerations</span></span>](expert-enumerations.md)                               |



 

 

 
