---
description: Traitement des In-Place
ms.assetid: 61e5c12c-e42a-42d8-ac5b-e60afaceda82
title: Traitement des In-Place
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b1a72b6bad2311a9c96bdd94e7e63acdc7e4961b51e106324dbe38de9510ad2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818794"
---
# <a name="in-place-processing"></a>Traitement des In-Place

Certaines transformations de données peuvent être effectuées en modifiant directement les données. C’est ce que l’on appelle le traitement *sur place* . De nombreux effets audio et vidéo peuvent être effectués de cette manière. si un DMO prend en charge le traitement sur place, il expose l’interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobjectinplace) . Le traitement sur place est généralement plus efficace que l’utilisation de mémoires tampons distinctes pour la sortie. (Une exception majeure se présente lorsque la mémoire tampon réside dans la mémoire vidéo. Dans ce cas, les opérations de lecture sont beaucoup plus lentes que les opérations d’écriture. par conséquent, le traitement sur place n’est pas recommandé.)

Pour traiter les données en place, le client effectue un appel unique à la méthode [**IMediaObjectInPlace ::P tionnaire**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobjectinplace-process) , plutôt qu’à des appels distincts à **ProcessInput** et **ProcessOutput**. La méthode **Process** est synchrone ; tout le traitement se produit à l’intérieur de l’appel. En outre, le traitement sur place n’utilise pas d’objets **IMediaBuffer** . La méthode **Process** prend un pointeur directement vers la mémoire tampon.

une DMO qui prend en charge le traitement sur place doit toujours implémenter l’interface **IMediaObject** , y compris les méthodes **ProcessInput** et **ProcessOutput** . Le client peut choisir s’il faut utiliser le traitement sur place ou utiliser des mémoires tampons distinctes. Toutefois, ne mélangez pas les deux types de traitement. Si vous appelez le **processus**, n’appelez pas **ProcessInput** ou **ProcessOutput**, et vice-versa.

**Fin des effets**

une DMO sur place peut créer une sortie supplémentaire après l’arrêt de l’entrée. C’est ce qu’on appelle une *fin d’effet*. Par exemple, un effet de réverbération se poursuit une fois que l’entrée atteint le silence. En cas de fin d’effet, la méthode **Process** retourne S \_ false. Une fois que l’application a traité toutes ses données, elle peut générer la fin de l’effet en envoyant des tampons vides à la méthode de **processus** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hébergement direct d’un DMO](directly-hosting-a-dmo.md)
</dt> </dl>

 

 



