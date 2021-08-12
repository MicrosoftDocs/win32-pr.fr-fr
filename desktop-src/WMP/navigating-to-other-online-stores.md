---
title: Navigation vers d’autres magasins en ligne
description: Navigation vers d’autres magasins en ligne
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Lecteur Windows Media des magasins en ligne, navigation
- magasins en ligne, navigation
- tapez 2 magasins en ligne, navigation
- navigation dans les magasins de type 2 en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1b2cb120ac161fd92bf8d35826b9dc096c95c37d916f19eb2aeb7362aabe7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574432"
---
# <a name="navigating-to-other-online-stores"></a>Navigation vers d’autres magasins en ligne

Vous pouvez créer des liens vers d’autres magasins en ligne que vous possédez ou un lien croisé vers des magasins en ligne fournis par d’autres. Pour ce faire, vous devez connaître le nom de clé du magasin en ligne auquel vous souhaitez accéder.

L’exemple de code suivant montre le code HTML qui crée un lien pour passer de la boutique en ligne Proseware à la fonctionnalité « ServiceTask2 » de la boutique en ligne Southridge Video :


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



lorsque l’utilisateur clique sur le lien, Lecteur Windows Media invite l’utilisateur à basculer vers le magasin vidéo Southridge. Si l’utilisateur le permet, le lecteur bascule les magasins et accède au volet de tâches spécifié, en ajoutant les paramètres de chaîne de requête. Les paramètres de chaîne de requête indiqués dans l’exemple précédent sont des paramètres personnalisés. Cela signifie que le magasin en ligne vers lequel vous passez doit s’attendre à ces valeurs et les gérer. Votre magasin en ligne (et tout magasin vers lequel vous basculez) peut utiliser des paramètres de chaîne de requête comme vous le souhaitez.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Navigation entre les volets des tâches de service**](navigating-between-service-task-panes.md)
</dt> <dt>

[**Navigation pour les magasins de type 2 en ligne**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




