---
description: L’architecture de la DLL de l’analyseur doit fournir les fonctionnalités présentées dans l’illustration suivante.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Architecture des DLL de l’analyseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7852029a892d8b74c954cbc2d7341fcaf29032fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485856"
---
# <a name="parser-dll-architecture"></a><span data-ttu-id="27530-103">Architecture des DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="27530-103">Parser DLL Architecture</span></span>

<span data-ttu-id="27530-104">L’architecture de la DLL de l’analyseur doit fournir les fonctionnalités présentées dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="27530-104">The architecture of the parser DLL must provide the features shown in the following illustration.</span></span> <span data-ttu-id="27530-105">N’oubliez pas que certaines fonctionnalités nécessitent l’implémentation d’un seul point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="27530-105">Be aware that some features require the implementation of only one entry point.</span></span> <span data-ttu-id="27530-106">Toutefois, si votre DLL de l’analyseur prend en charge plusieurs protocoles, la fonctionnalité nécessite l’implémentation de plusieurs points d’entrée.</span><span class="sxs-lookup"><span data-stu-id="27530-106">However, if your parser DLL supports multiple protocols, then the feature requires the implementation of multiple entry points.</span></span>

![fonctionnalités dll de l’analyseur](images/parserarchitecture1.png)



| <span data-ttu-id="27530-108">Pour obtenir des informations sur</span><span class="sxs-lookup"><span data-stu-id="27530-108">For information about</span></span>                                                  | <span data-ttu-id="27530-109">Consultez</span><span class="sxs-lookup"><span data-stu-id="27530-109">See</span></span>                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="27530-110">Comment implémenter les fonctions d’exportation de DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="27530-110">How to implement parser DLL export functions.</span></span>                          | [<span data-ttu-id="27530-111">Écriture d’un analyseur de protocole</span><span class="sxs-lookup"><span data-stu-id="27530-111">Writing a Protocol Parser</span></span>](writing-a-protocol-parser.md)             |
| <span data-ttu-id="27530-112">Fonctions et structures spécifiques utilisées par les analyseurs : rubriques de référence.</span><span class="sxs-lookup"><span data-stu-id="27530-112">Specific functions and structures that parsers use — reference topics.</span></span> | [<span data-ttu-id="27530-113">Structures et fonctions de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="27530-113">Parser Functions and Structures</span></span>](parser-functions-and-structures.md) |



 

 

 



