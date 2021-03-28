---
description: Illustre la clé de Registre qui doit être définie pour empêcher l’exécution automatique.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Comment empêcher l’exécution automatique d’un composant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebe03473ce7c5eb441ec428cbe4d060dc62f042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973138"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a><span data-ttu-id="a23f2-103">Comment empêcher l’exécution automatique d’un composant</span><span class="sxs-lookup"><span data-stu-id="a23f2-103">How to Prevent AutoPlay for a Component</span></span>

<span data-ttu-id="a23f2-104">Illustre la clé de Registre qui doit être définie pour empêcher l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="a23f2-104">Illustrates which registry key must be set to prevent AutoPlay.</span></span>

## <a name="instructions"></a><span data-ttu-id="a23f2-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="a23f2-105">Instructions</span></span>


<span data-ttu-id="a23f2-106">Pour empêcher le lancement de l’exécution automatique en réponse à un événement, ajoutez la valeur **reg \_ SZ** suivante, comme illustré dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="a23f2-106">To prevent AutoPlay from launching in response to an event, add the following **REG\_SZ** value, as shown in this example.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     CancelAutoplay
                        CLSID
                           00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="a23f2-107">La valeur correspond à l’identificateur de classe (CLSID) que le composant qui génère l’événement est connu dans la table ROT (Running Object Table).</span><span class="sxs-lookup"><span data-stu-id="a23f2-107">The value is the class identifier (CLSID) that the component that is generating the event is known by in the running object table (ROT).</span></span> <span data-ttu-id="a23f2-108">La valeur n’a pas de données.</span><span class="sxs-lookup"><span data-stu-id="a23f2-108">The value has no data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a23f2-109">Sous cette clé, les CLSID ne sont pas mis entre accolades ( {} ).</span><span class="sxs-lookup"><span data-stu-id="a23f2-109">Under this key, the CLSIDs are not enclosed in braces ( {} ).</span></span>

 

 

 



