---
title: Écoute des attributs
description: Écoute des attributs
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Apparences du lecteur Windows Media, écoute des attributs
- apparences, attributs d’écoute
- informations de référence sur les apparences, les attributs d’écoute
- écoute des attributs
- attributs, écoute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349a549966f7fba5ea152f8f0bb002a92f6dfb8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507174"
---
# <a name="listening-attributes"></a><span data-ttu-id="2db9b-108">Écoute des attributs</span><span class="sxs-lookup"><span data-stu-id="2db9b-108">Listening Attributes</span></span>

<span data-ttu-id="2db9b-109">Un attribut d’écoute est utilisé pour connecter un attribut à un autre afin que sa valeur change chaque fois que la valeur de l’autre attribut change.</span><span class="sxs-lookup"><span data-stu-id="2db9b-109">A listening attribute is used to connect one attribute to another so that its value changes every time the value of the other attribute changes.</span></span>

<span data-ttu-id="2db9b-110">L’attribut Listening **wmpprop :** est le plus utile.</span><span class="sxs-lookup"><span data-stu-id="2db9b-110">The listening attribute **wmpprop:** is the most useful.</span></span> <span data-ttu-id="2db9b-111">Si la valeur d’un attribut est spécifiée comme étant le **wmpprop :** d’un deuxième attribut, la première valeur est automatiquement mise à jour pour refléter la deuxième valeur chaque fois que la deuxième valeur change.</span><span class="sxs-lookup"><span data-stu-id="2db9b-111">If the value of one attribute is specified to be the **wmpprop:** of a second attribute, the first value will be automatically updated to reflect the second value each time the second value changes.</span></span>

<span data-ttu-id="2db9b-112">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="2db9b-112">**Example:**</span></span>


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



<span data-ttu-id="2db9b-113">De cette façon, la valeur de mySlider, indiquée par la position du contrôle Slider, peut également être affichée sous la forme d’un nombre dans une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="2db9b-113">In this way, the value of mySlider, shown by the position of the slider control, can also be shown as a number within a text box.</span></span>

<span data-ttu-id="2db9b-114">Les deux autres attributs d’écoute, **wmpenabled** et **wmpdisabled :**, peuvent être utilisés pour modifier l’attribut **Enabled** d’un contrôle selon que ses fonctionnalités sont actuellement disponibles dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="2db9b-114">The two other listening attributes, **wmpenabled:** and **wmpdisabled:**, can be used to change the **enabled** attribute of a control depending on whether its functionality is currently available in the player.</span></span> <span data-ttu-id="2db9b-115">Ces attributs peuvent écouter uniquement les méthodes de l’objet **contrôles** .</span><span class="sxs-lookup"><span data-stu-id="2db9b-115">These attributes can listen only to methods of the **Controls** object.</span></span>

<span data-ttu-id="2db9b-116">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="2db9b-116">**Example:**</span></span>


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a><span data-ttu-id="2db9b-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2db9b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2db9b-118">**Divers**</span><span class="sxs-lookup"><span data-stu-id="2db9b-118">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




