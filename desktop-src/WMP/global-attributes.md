---
title: Attributs globaux (Windows Media Player SDK)
description: Attributs globaux
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- Apparences du lecteur Windows Media, attributs globaux
- apparences, attributs globaux
- informations de référence sur les apparences, les attributs globaux
- attributs globaux
- attributs, globaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c3f7a605b5c277b3207cefbbeaaa641f81f026
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104381109"
---
# <a name="global-attributes"></a><span data-ttu-id="998f8-108">Attributs globaux</span><span class="sxs-lookup"><span data-stu-id="998f8-108">Global Attributes</span></span>

<span data-ttu-id="998f8-109">Les attributs globaux sont des attributs qui permettent d’accéder facilement à certains éléments ou objets de joueur depuis n’importe quel emplacement d’une apparence.</span><span class="sxs-lookup"><span data-stu-id="998f8-109">Global attributes are attributes that provide easy access to certain player elements or objects from anywhere within a skin.</span></span>

<span data-ttu-id="998f8-110">L’attribut global **Player** est une référence à l’objet [Player](player-object.md) et est utilisé pour accéder aux fonctionnalités principales du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="998f8-110">The **player** global attribute is a reference to the [Player](player-object.md) object, and is used to access the primary functionality of Windows Media Player.</span></span> <span data-ttu-id="998f8-111">L’exemple suivant utilise **Player** pour commencer la lecture des médias numériques.</span><span class="sxs-lookup"><span data-stu-id="998f8-111">The following example uses **player** to begin digital media playback.</span></span>


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



<span data-ttu-id="998f8-112">L’attribut global **Theme** est une référence à l’élément [Theme](theme-element.md) .</span><span class="sxs-lookup"><span data-stu-id="998f8-112">The **theme** global attribute is a reference to the [THEME](theme-element.md) element.</span></span> <span data-ttu-id="998f8-113">Il s’agit de la méthode appropriée pour accéder aux attributs de **thème** , plutôt que de spécifier un ID au sein de l’élément de **thème** .</span><span class="sxs-lookup"><span data-stu-id="998f8-113">This is the proper way to access **THEME** attributes, rather than by specifying an ID within the **THEME** element.</span></span> <span data-ttu-id="998f8-114">L’exemple suivant utilise **Theme** pour ouvrir un nouvel affichage.</span><span class="sxs-lookup"><span data-stu-id="998f8-114">The following example uses **theme** to open a new view.</span></span>


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



<span data-ttu-id="998f8-115">L’attribut global de **vue** est une référence à la [vue](view-element.md)actuelle.</span><span class="sxs-lookup"><span data-stu-id="998f8-115">The **view** global attribute is a reference to the current [VIEW](view-element.md).</span></span> <span data-ttu-id="998f8-116">Il peut être utilisé à la place de l’ID spécifié dans les différents éléments de la **vue** .</span><span class="sxs-lookup"><span data-stu-id="998f8-116">This can be used instead of the ID specified within the various **VIEW** elements.</span></span> <span data-ttu-id="998f8-117">L’exemple suivant utilise la **vue** pour fermer l’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="998f8-117">The following example uses **view** to close the current view.</span></span>


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



<span data-ttu-id="998f8-118">L’attribut global d' **événement** est utilisé pour accéder aux attributs d’événements ambiants à partir des gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="998f8-118">The **event** global attribute is used to access ambient event attributes from within event handlers.</span></span> <span data-ttu-id="998f8-119">L’exemple suivant utilise l' **événement** pour déterminer si la touche Alt est enfoncée lorsque l’utilisateur clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="998f8-119">The following example uses **event** to determine whether the ALT key is pressed when a button is clicked.</span></span>


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



<span data-ttu-id="998f8-120">L’attribut global **playerApplication** est une référence à l’objet [playerApplication](playerapplication-object.md) et est utilisé par les fichiers d’apparence fournis en tant qu’interfaces utilisateur personnalisées pour les contrôles de lecteur distants.</span><span class="sxs-lookup"><span data-stu-id="998f8-120">The **playerApplication** global attribute is a reference to the [PlayerApplication](playerapplication-object.md) object, and is used by skin files provided as custom user interfaces for remoted Player controls.</span></span> <span data-ttu-id="998f8-121">Le contrôle de lecteur peut être incorporé en mode distant uniquement dans les programmes C++ qui implémentent l’interface **IWMPRemoteMediaServices** .</span><span class="sxs-lookup"><span data-stu-id="998f8-121">The Player control can be embedded in remote mode only in C++ programs that implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="998f8-122">L’exemple suivant utilise **playerApplication** pour basculer vers le mode complet du lecteur.</span><span class="sxs-lookup"><span data-stu-id="998f8-122">The following example uses **playerApplication** to switch to the full mode of the Player.</span></span>


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



<span data-ttu-id="998f8-123">Pour plus d’informations, consultez [attributs d’événement ambiant](ambient-event-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="998f8-123">For more information, see [Ambient Event Attributes](ambient-event-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="998f8-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="998f8-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="998f8-125">**Divers**</span><span class="sxs-lookup"><span data-stu-id="998f8-125">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




