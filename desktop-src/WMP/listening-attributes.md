---
title: Écoute des attributs
description: Écoute des attributs
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- apparences de Lecteur Windows Media, attributs d’écoute
- apparences, attributs d’écoute
- informations de référence sur les apparences, les attributs d’écoute
- écoute des attributs
- attributs, écoute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8cceb9a8721995c494b5e4366291353376a2569c045e41eb41c1418e2f4d5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996409"
---
# <a name="listening-attributes"></a>Écoute des attributs

Un attribut d’écoute est utilisé pour connecter un attribut à un autre afin que sa valeur change chaque fois que la valeur de l’autre attribut change.

L’attribut Listening **wmpprop :** est le plus utile. Si la valeur d’un attribut est spécifiée comme étant le **wmpprop :** d’un deuxième attribut, la première valeur est automatiquement mise à jour pour refléter la deuxième valeur chaque fois que la deuxième valeur change.

**Exemple :**


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



De cette façon, la valeur de mySlider, indiquée par la position du contrôle Slider, peut également être affichée sous la forme d’un nombre dans une zone de texte.

Les deux autres attributs d’écoute, **wmpenabled** et **wmpdisabled :**, peuvent être utilisés pour modifier l’attribut **Enabled** d’un contrôle selon que ses fonctionnalités sont actuellement disponibles dans le lecteur. Ces attributs peuvent écouter uniquement les méthodes de l’objet **contrôles** .

**Exemple :**


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Divers**](miscellaneous.md)
</dt> </dl>

 

 




