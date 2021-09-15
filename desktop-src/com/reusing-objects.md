---
title: Réutilisation d’objets
description: Réutilisation d’objets
ms.assetid: 07055fea-bdfe-4c7a-be07-2edcbf609dd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03a830eb539823b0350c9ce41a096cda821bb0cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403952"
---
# <a name="reusing-objects"></a>Réutilisation d’objets

L’un des objectifs importants d’un modèle objet est de permettre aux auteurs d’objets de réutiliser et d’étendre des objets fournis par d’autres en tant qu’éléments de leurs propres implémentations. l’une des façons d’effectuer cette opération dans Microsoft Visual C++ et d’autres langages consiste à utiliser l' *héritage d’implémentation*, qui permet à un objet d’hériter (« sous-classe ») certaines de ses fonctions d’un autre objet tout en remplaçant d’autres fonctions.

Le problème de l’interaction des objets du système à l’aide de l’héritage d’implémentation traditionnel est que le contrat (l’interface) entre les objets d’une hiérarchie d’implémentation n’est pas clairement défini. En fait, elle est implicite et ambiguë. Lorsque l’objet parent ou enfant modifie son implémentation, le comportement des composants associés peut devenir non défini ou INSTABLEMENT implémenté. Dans une application unique, où l’implémentation peut être gérée par une équipe d’ingénierie unique qui met à jour tous les composants en même temps, ce n’est pas toujours un problème majeur. Dans un environnement où les composants d’une équipe sont créés par le biais de la réutilisation de la boîte noire d’autres composants créés par d’autres équipes, ce type d’instabilité met en péril la réutilisation. En outre, l’héritage d’implémentation fonctionne généralement uniquement dans les limites du processus. Cela rend l’héritage d’implémentation traditionnel peu pratique pour les grands systèmes en constante évolution, composés de composants logiciels créés par de nombreuses équipes d’ingénierie.

La clé de la création des composants réutilisables consiste à pouvoir traiter l’objet comme une boîte opaque. Cela signifie que la partie du code qui tente de réutiliser un autre objet ne sait rien et ne doit en savoir rien, à propos de la structure interne ou de l’implémentation du composant utilisé. En d’autres termes, le code qui tente de réutiliser un composant dépend du comportement de l’objet et non de son implémentation exacte.

Pour obtenir une réutilisation de la boîte noire, COM adopte d’autres mécanismes de réutilisation établis, tels que la *relation contenant-contenu* , la délégation et l' *agrégation*.

> [!NOTE]  
> Pour plus de commodité, l’objet qui est réutilisé est appelé l' *objet interne* et l’objet qui utilise cet objet interne est l' *objet externe*.

 

Il est important de se souvenir dans ces deux mécanismes de la façon dont l’objet externe apparaît à ses clients. En ce qui concerne les clients, les deux objets implémentent les interfaces auxquelles le client peut obtenir un pointeur. Le client traite l’objet externe comme un cadre opaque et n’a donc pas besoin de se soucier de la structure interne du objectâ externe. il ne s’intéresse pas non plus au comportement.

Pour plus d'informations, voir les rubriques suivantes :

-   [Imbrication/délégation](containment-delegation.md)
-   [Agrégation](aggregation.md)

 

 




