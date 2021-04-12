---
description: Le Service VSS (VSS) est un ensemble d’API COM et C++ qui permettent d’effectuer des sauvegardes de volume alors que les applications sur le système (appelées rédacteurs) continuent d’écrire sur les volumes.
ms.assetid: 94d9504b-2838-4516-8031-daa7bd9d2fec
title: Informations de référence sur l’API de cliché instantané de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8651c987c01ce67f1383f2ab1a24ca3fea8bbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526295"
---
# <a name="volume-shadow-copy-api-reference"></a><span data-ttu-id="5a0bf-103">Informations de référence sur l’API de cliché instantané de volume</span><span class="sxs-lookup"><span data-stu-id="5a0bf-103">Volume Shadow Copy API Reference</span></span>

<span data-ttu-id="5a0bf-104">Le Service VSS (VSS) est un ensemble d’API COM et C++ qui permettent d’effectuer des sauvegardes de volume alors que les applications sur le système (appelées rédacteurs) continuent d’écrire sur les volumes.</span><span class="sxs-lookup"><span data-stu-id="5a0bf-104">The Volume Shadow Copy Service (VSS) is a set of COM and C++ APIs that enable volume backups to be performed while applications on the system (called writers) continue to write to the volumes.</span></span>

<span data-ttu-id="5a0bf-105">VSS prend en charge ces sauvegardes par le biais de la création de clichés instantanés, un doublon du volume d’origine à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="5a0bf-105">VSS supports these backups through the creation of shadow copies, a duplicate of the original volume at a given point in time.</span></span>

<span data-ttu-id="5a0bf-106">Les développeurs tiers peuvent utiliser l’API VSS pour créer des demandeurs (par exemple, une application de sauvegarde) pour créer et gérer des clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="5a0bf-106">Third-party developers can use the VSS API to create requesters (such as a backup application) to create and manage shadow copies.</span></span>

<span data-ttu-id="5a0bf-107">Le travail réel de création et de représentation des clichés instantanés est effectué par les applications de niveau système appelées fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="5a0bf-107">The actual work of creating and representing shadow copies is conducted by system-level applications known as providers.</span></span>

<span data-ttu-id="5a0bf-108">Les développeurs peuvent également utiliser l’API pour construire des enregistreurs : les applications prenant en charge VSS, capables de coordonner les opérations d’e/s avec la création et la manipulation de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="5a0bf-108">Developers can also use the API to construct writers: VSS-aware applications that are able to coordinate I/O operations with the creation and manipulation of shadow copies.</span></span>

-   [<span data-ttu-id="5a0bf-109">Classes d’API de cliché instantané du volume</span><span class="sxs-lookup"><span data-stu-id="5a0bf-109">Volume Shadow Copy API Classes</span></span>](volume-shadow-copy-api-classes.md)
-   [<span data-ttu-id="5a0bf-110">Types de données de l’API de cliché instantané des volumes</span><span class="sxs-lookup"><span data-stu-id="5a0bf-110">Volume Shadow Copy API Data Types</span></span>](volume-shadow-copy-api-data-types.md)
-   [<span data-ttu-id="5a0bf-111">Énumérations de l’API de cliché instantané du volume</span><span class="sxs-lookup"><span data-stu-id="5a0bf-111">Volume Shadow Copy API Enumerations</span></span>](volume-shadow-copy-api-enumeration-types.md)
-   [<span data-ttu-id="5a0bf-112">Fonctions de l’API de cliché instantané du volume</span><span class="sxs-lookup"><span data-stu-id="5a0bf-112">Volume Shadow Copy API Functions</span></span>](volume-shadow-copy-api-functions.md)
-   [<span data-ttu-id="5a0bf-113">Interfaces API du cliché instantané du volume</span><span class="sxs-lookup"><span data-stu-id="5a0bf-113">Volume Shadow Copy API Interfaces</span></span>](volume-shadow-copy-api-interfaces.md)
-   [<span data-ttu-id="5a0bf-114">Structures de l’API de cliché instantané des volumes</span><span class="sxs-lookup"><span data-stu-id="5a0bf-114">Volume Shadow Copy API Structures</span></span>](volume-shadow-copy-api-structures.md)
-   [<span data-ttu-id="5a0bf-115">Glossaire des clichés instantanés de volume</span><span class="sxs-lookup"><span data-stu-id="5a0bf-115">Volume Shadow Copy Glossary</span></span>](volume-shadow-copy-glossary.md)

<span data-ttu-id="5a0bf-116">Pour plus d’informations sur l’écriture des demandeurs et des writers, consultez [utilisation de l’service VSS](using-the-volume-shadow-copy-service.md).</span><span class="sxs-lookup"><span data-stu-id="5a0bf-116">For more information on writing requesters and writers, see [Using the Volume Shadow Copy Service](using-the-volume-shadow-copy-service.md).</span></span>

 

 



