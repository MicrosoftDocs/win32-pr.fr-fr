---
title: attributs globaux (kit de développement logiciel Lecteur Windows Media)
description: Attributs globaux
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- apparences de Lecteur Windows Media, attributs globaux
- apparences, attributs globaux
- informations de référence sur les apparences, les attributs globaux
- attributs globaux
- attributs, globaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c2d52b6489a28eff20e3a7e5c7180fc9e2db9309c0fe42880bfc779a23f563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648079"
---
# <a name="global-attributes"></a>Attributs globaux

Les attributs globaux sont des attributs qui permettent d’accéder facilement à certains éléments ou objets de joueur depuis n’importe quel emplacement d’une apparence.

l’attribut global **player** est une référence à l’objet [player](player-object.md) et est utilisé pour accéder aux fonctionnalités principales de Lecteur Windows Media. L’exemple suivant utilise **Player** pour commencer la lecture des médias numériques.


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



L’attribut global **Theme** est une référence à l’élément [Theme](theme-element.md) . Il s’agit de la méthode appropriée pour accéder aux attributs de **thème** , plutôt que de spécifier un ID au sein de l’élément de **thème** . L’exemple suivant utilise **Theme** pour ouvrir un nouvel affichage.


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



L’attribut global de **vue** est une référence à la [vue](view-element.md)actuelle. Il peut être utilisé à la place de l’ID spécifié dans les différents éléments de la **vue** . L’exemple suivant utilise la **vue** pour fermer l’affichage actuel.


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



L’attribut global d' **événement** est utilisé pour accéder aux attributs d’événements ambiants à partir des gestionnaires d’événements. L’exemple suivant utilise l' **événement** pour déterminer si la touche Alt est enfoncée lorsque l’utilisateur clique sur un bouton.


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



L’attribut global **playerApplication** est une référence à l’objet [playerApplication](playerapplication-object.md) et est utilisé par les fichiers d’apparence fournis en tant qu’interfaces utilisateur personnalisées pour les contrôles de lecteur distants. Le contrôle de lecteur peut être incorporé en mode distant uniquement dans les programmes C++ qui implémentent l’interface **IWMPRemoteMediaServices** . L’exemple suivant utilise **playerApplication** pour basculer vers le mode complet du lecteur.


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



Pour plus d’informations, consultez [attributs d’événement ambiant](ambient-event-attributes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Divers**](miscellaneous.md)
</dt> </dl>

 

 




