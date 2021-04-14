---
title: Exécution de l’exemple de projet
description: Exécution de l’exemple de projet
ms.assetid: d0c32a75-4d30-408b-8da8-3917f6fd6ea4
keywords:
- Windows Media Player Online stores, exécution d’exemples de projets
- magasins en ligne, exemples de projets en cours d’exécution
- type 2 magasins en ligne, exemples de projets en cours d’exécution
- Magasins en ligne du lecteur Windows Media, exemples de projets
- magasins en ligne, exemples de projets
- types 2 magasins en ligne, exemples de projets
- exemples de projets en cours d’exécution
- exemples, type 2 magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8f42829add3ffbe5cc026f7dc2451513701fd2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380140"
---
# <a name="running-the-sample-project"></a>Exécution de l’exemple de projet

L’exemple de composant COM illustre la fonctionnalité fournie par les méthodes de **IWMPSubscriptionServices** en affichant une boîte de dialogue chaque fois que le lecteur Windows Media appelle l’une des méthodes. Pour voir cela se produit, vous devez d’abord ajouter du contenu à la bibliothèque qui contient un attribut **ContentDistributor** qui correspond à votre service. Consultez [Ajout de l’attribut ContentDistributor](adding-the-contentdistributor-attribute.md). Ensuite, utilisez le lecteur Windows Media 10 ou une version ultérieure pour ouvrir votre boutique en ligne, lire votre contenu Premium et copier votre contenu Premium sur un appareil. Le lecteur Windows Media instanciera l’exemple de composant COM et appellera les méthodes quand cela est approprié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du plug-in pour un magasin de type 2 en ligne**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




