---
title: Navigation vers d’autres magasins en ligne
description: Navigation vers d’autres magasins en ligne
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Windows Media Player Online stores, navigation
- magasins en ligne, navigation
- tapez 2 magasins en ligne, navigation
- navigation dans les magasins de type 2 en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8456954d5a7197a054098320b35fb38409ba62
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309186"
---
# <a name="navigating-to-other-online-stores"></a><span data-ttu-id="d7714-107">Navigation vers d’autres magasins en ligne</span><span class="sxs-lookup"><span data-stu-id="d7714-107">Navigating to Other Online Stores</span></span>

<span data-ttu-id="d7714-108">Vous pouvez créer des liens vers d’autres magasins en ligne que vous possédez ou un lien croisé vers des magasins en ligne fournis par d’autres.</span><span class="sxs-lookup"><span data-stu-id="d7714-108">You can create links to other online stores you own or cross-link to online stores provided by others.</span></span> <span data-ttu-id="d7714-109">Pour ce faire, vous devez connaître le nom de clé du magasin en ligne auquel vous souhaitez accéder.</span><span class="sxs-lookup"><span data-stu-id="d7714-109">To do this, you need to know the key name for the online store to which you want to navigate.</span></span>

<span data-ttu-id="d7714-110">L’exemple de code suivant montre le code HTML qui crée un lien pour passer de la boutique en ligne Proseware à la fonctionnalité « ServiceTask2 » de la boutique en ligne Southridge Video :</span><span class="sxs-lookup"><span data-stu-id="d7714-110">The following example code shows HTML that creates a link to switch from the Proseware online store to the "ServiceTask2" feature of the Southridge Video online store:</span></span>


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



<span data-ttu-id="d7714-111">Lorsque l’utilisateur clique sur le lien, le lecteur Windows Media lui invite à basculer vers le magasin vidéo Southridge.</span><span class="sxs-lookup"><span data-stu-id="d7714-111">When the user clicks the link, Windows Media Player prompts the user to switch to the Southridge Video store.</span></span> <span data-ttu-id="d7714-112">Si l’utilisateur le permet, le lecteur bascule les magasins et accède au volet de tâches spécifié, en ajoutant les paramètres de chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="d7714-112">If the user permits it, the Player then switches stores and navigates to the specified task pane, appending the query string parameters.</span></span> <span data-ttu-id="d7714-113">Les paramètres de chaîne de requête indiqués dans l’exemple précédent sont des paramètres personnalisés.</span><span class="sxs-lookup"><span data-stu-id="d7714-113">The query string parameters shown in the preceding example are custom parameters.</span></span> <span data-ttu-id="d7714-114">Cela signifie que le magasin en ligne vers lequel vous passez doit s’attendre à ces valeurs et les gérer.</span><span class="sxs-lookup"><span data-stu-id="d7714-114">This means that the online store you switch to must expect these values and handle them.</span></span> <span data-ttu-id="d7714-115">Votre magasin en ligne (et tout magasin vers lequel vous basculez) peut utiliser des paramètres de chaîne de requête comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="d7714-115">Your online store (and any store you switch to) can use query string parameters any way you choose.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7714-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d7714-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7714-117">**Navigation entre les volets des tâches de service**</span><span class="sxs-lookup"><span data-stu-id="d7714-117">**Navigating between Service Task Panes**</span></span>](navigating-between-service-task-panes.md)
</dt> <dt>

[<span data-ttu-id="d7714-118">**Navigation pour les magasins de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="d7714-118">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




