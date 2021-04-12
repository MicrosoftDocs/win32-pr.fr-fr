---
description: Les fonctions, répertoriées dans le tableau suivant, sont des points d’entrée pour les dll de l’analyseur. Les fonctions sont les points d’entrée pour les appels du système d’exploitation et Moniteur réseau.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Fonctions d’exportation de DLL de l’analyseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929541a1eda60740fe219352fee285a5a34a89df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393407"
---
# <a name="parser-dll-export-functions"></a><span data-ttu-id="6212e-104">Fonctions d’exportation de DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="6212e-104">Parser DLL Export Functions</span></span>

<span data-ttu-id="6212e-105">Les fonctions, répertoriées dans le tableau suivant, sont des points d’entrée pour les dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="6212e-105">The functions, listed in the following table, are entry points for parser DLLs.</span></span> <span data-ttu-id="6212e-106">Les fonctions sont les points d’entrée pour les appels du système d’exploitation et Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="6212e-106">The functions are the entry points for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="6212e-107">Fonction</span><span class="sxs-lookup"><span data-stu-id="6212e-107">Function</span></span>                                           | <span data-ttu-id="6212e-108">Description</span><span class="sxs-lookup"><span data-stu-id="6212e-108">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6212e-109">Analyseur DllMain</span><span class="sxs-lookup"><span data-stu-id="6212e-109">DllMain Parser</span></span>](dllmain-parser.md)               | <span data-ttu-id="6212e-110">Indique à la DLL de l’analyseur qu’elle est chargée ou déchargée.</span><span class="sxs-lookup"><span data-stu-id="6212e-110">Indicates to the parser DLL that it is loaded or unloaded.</span></span> <span data-ttu-id="6212e-111">Le système d’exploitation appelle la fonction d' **analyse DllMain** lorsqu’un processus charge ou décharge la dll.</span><span class="sxs-lookup"><span data-stu-id="6212e-111">The operating system calls the **DllMain Parser** function when a process loads or unloads the DLL.</span></span> |
| [<span data-ttu-id="6212e-112">AttachProperties</span><span class="sxs-lookup"><span data-stu-id="6212e-112">AttachProperties</span></span>](attachproperties.md)           | <span data-ttu-id="6212e-113">Indique à l’analyseur d’attacher toutes les propriétés qui existent dans un frame.</span><span class="sxs-lookup"><span data-stu-id="6212e-113">Notifies the parser to attach any properties that exist in a frame.</span></span>                                                                                            |
| [<span data-ttu-id="6212e-114">Désinscrire</span><span class="sxs-lookup"><span data-stu-id="6212e-114">Deregister</span></span>](deregister.md)                       | <span data-ttu-id="6212e-115">Notifie l’analyseur à nettoyer.</span><span class="sxs-lookup"><span data-stu-id="6212e-115">Notifies the parser to clean up.</span></span>                                                                                                                               |
| [<span data-ttu-id="6212e-116">FormatProperties</span><span class="sxs-lookup"><span data-stu-id="6212e-116">FormatProperties</span></span>](formatproperties.md)           | <span data-ttu-id="6212e-117">Indique à l’analyseur de prendre toutes les instances de propriété dans et de générer le membre **szPropertyText** de chaque structure **PROPERTYINST** .</span><span class="sxs-lookup"><span data-stu-id="6212e-117">Notifies the parser to take all of the property instances in and build the **szPropertyText** member of each **PROPERTYINST** structure.</span></span>                       |
| [<span data-ttu-id="6212e-118">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="6212e-118">RecognizeFrame</span></span>](recognizeframe.md)               | <span data-ttu-id="6212e-119">Détermine si l’analyseur peut interpréter les données de frame non traitées avec le protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="6212e-119">Determines whether the parser can interpret the unprocessed frame data with the specified protocol.</span></span>                                                            |
| [<span data-ttu-id="6212e-120">Inscrire l’analyseur</span><span class="sxs-lookup"><span data-stu-id="6212e-120">Register Parser</span></span>](register-parser.md)             | <span data-ttu-id="6212e-121">Détermine les informations de base relatives à l’analyseur dans la DLL.</span><span class="sxs-lookup"><span data-stu-id="6212e-121">Determines basic information about the parser within the DLL.</span></span> <span data-ttu-id="6212e-122">Moniteur réseau appelle la fonction d' **Analyseur de Registre** .</span><span class="sxs-lookup"><span data-stu-id="6212e-122">Network Monitor calls the **Register Parser** function.</span></span>                                          |
| [<span data-ttu-id="6212e-123">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="6212e-123">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md) | <span data-ttu-id="6212e-124">Installe automatiquement un analyseur.</span><span class="sxs-lookup"><span data-stu-id="6212e-124">Installs a parser automatically.</span></span>                                                                                                                               |



 

<span data-ttu-id="6212e-125">Moniteur réseau fournit des structures et des fonctions d’assistance que l’analyseur peut appeler.</span><span class="sxs-lookup"><span data-stu-id="6212e-125">Network Monitor provides structures and helper functions that the parser can call.</span></span>



| <span data-ttu-id="6212e-126">Pour plus d’informations sur l’un des sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="6212e-126">For more information about</span></span>                          | <span data-ttu-id="6212e-127">Consultez</span><span class="sxs-lookup"><span data-stu-id="6212e-127">See</span></span>                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6212e-128">Fonctions d’assistance que les experts et les analyseurs peuvent appeler.</span><span class="sxs-lookup"><span data-stu-id="6212e-128">Helper functions that experts and parsers can call.</span></span> | [<span data-ttu-id="6212e-129">Fonctions courantes des experts et de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="6212e-129">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="6212e-130">Fonctions d’assistance que seuls les analyseurs peuvent appeler.</span><span class="sxs-lookup"><span data-stu-id="6212e-130">Helper functions that only parsers can call.</span></span>        | [<span data-ttu-id="6212e-131">Fonctions de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="6212e-131">Parser Functions</span></span>](parser-functions.md)                                     |
| <span data-ttu-id="6212e-132">Structures utilisées par les fonctions d’analyseur.</span><span class="sxs-lookup"><span data-stu-id="6212e-132">Structures that parser functions use.</span></span>               | [<span data-ttu-id="6212e-133">Structures de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="6212e-133">Parser Structures</span></span>](parser-structures.md)                                   |



 

 

 



