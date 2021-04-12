---
description: Contrôle qualité par défaut
ms.assetid: 91c4b8cf-3d24-4a11-b19c-b0297734e52b
title: Contrôle qualité par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864cd187df71c56441edcfd00fcd6785d96afe84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033377"
---
# <a name="default-quality-control"></a>Contrôle qualité par défaut

Les [classes de base DirectShow](directshow-base-classes.md) implémentent des comportements par défaut pour le contrôle de la qualité vidéo.

Les messages de qualité démarrent au niveau du convertisseur. La classe de base pour les convertisseurs vidéo est [**CBaseVideoRenderer**](cbasevideorenderer.md), qui a le comportement suivant :

1.  Quand le convertisseur vidéo reçoit un échantillon, il compare l’horodatage de l’échantillon avec le temps de référence actuel.
2.  Le convertisseur vidéo génère un message de qualité. Dans la classe de base, la **proportion** de membres du message de qualité est limitée à une plage de 500 (50%) à 2000 (200%). Les valeurs en dehors de cette plage peuvent entraîner des modifications de qualité brusques.
3.  Par défaut, le convertisseur vidéo envoie le message de qualité à la broche de sortie en amont (le code confidentiel connecté à sa broche d’entrée). Les applications peuvent substituer ce comportement en appelant la méthode **SetSink** .

Ce qui se passe ensuite dépend du filtre en amont. En règle générale, il s’agit d’un filtre de transformation. La classe de base pour les filtres de transformation est [**CTransformFilter**](ctransformfilter.md), qui utilise les classes [**CTransformInputPin**](ctransforminputpin.md) et [**CTransformOutputPin**](ctransformoutputpin.md) pour implémenter les broches d’entrée et de sortie. Ensemble, ces classes ont le comportement suivant :

1.  La méthode [**CTransformOutputPin :: Notify**](ctransformoutputpin-notify.md) appelle [**CTransformFilter :: AlterQuality**](ctransformfilter-alterquality.md), une méthode privée sur la classe de base de filtre.
2.  Les filtres dérivés peuvent remplacer **AlterQuality** pour gérer le message de qualité. Par défaut, **AlterQuality** ignore le message de qualité.
3.  Si **AlterQuality** ne gère pas le message de qualité, la broche de sortie appelle [**CBaseInputPin ::P assnotify**](cbaseinputpin-passnotify.md), une méthode privée sur la broche d’entrée du filtre.
4.  **PassNotify** transmet le message de qualité à l’emplacement approprié (la broche de sortie en amont suivante ou un gestionnaire de qualité personnalisé).

En supposant qu’aucun filtre de transformation ne gère le message de qualité, le message finit par atteindre la broche de sortie sur le filtre source. Dans les classes de base, [**CBasePin :: Notify**](cbasepin-notify.md) retourne E \_ NOTIMPL. La façon dont un filtre source particulier gère les messages de qualité dépend de la nature de la source. Certaines sources, telles que Live Video capture, ne peuvent pas effectuer un contrôle de qualité significatif. D’autres sources peuvent ajuster la vitesse à laquelle elles fournissent des exemples.

Le diagramme suivant illustre le comportement par défaut.

![contrôle de qualité dans les classes de base](images/quality-control.png)

Le convertisseur vidéo de base implémente **IQualityControl :: Notify**, ce qui signifie que vous pouvez passer des messages de qualité au convertisseur lui-même. Si vous définissez le membre **proportion** sur une valeur inférieure à 1000, le convertisseur vidéo insère un délai d’attente entre chaque frame qu’il restitue, ce qui ralentit le convertisseur. (Vous pouvez le faire pour réduire l’utilisation du système, par exemple). Pour plus d’informations, consultez [**CBaseVideoRenderer :: ThrottleWait**](cbasevideorenderer-throttlewait.md). La définition du membre de **proportion** sur une valeur supérieure à 1000 n’a aucun effet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion du contrôle de la qualité](quality-control-management.md)
</dt> </dl>

 

 



