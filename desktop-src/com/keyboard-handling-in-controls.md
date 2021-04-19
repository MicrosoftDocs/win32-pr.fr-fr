---
title: Gestion du clavier dans les contrôles
description: Gestion du clavier dans les contrôles
ms.assetid: 33affb3f-5d52-4ada-9751-0775b31a375e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f32610732ddbf88c6a587d5bc0fd7de1188152d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106538790"
---
# <a name="keyboard-handling-in-controls"></a>Gestion du clavier dans les contrôles

La prise en charge de la gestion du clavier pour les fonctionnalités suivantes est fortement recommandée, bien qu’elle soit reconnue qu’elle n’est pas applicable à tous les conteneurs.

-   Prise en charge des \_ bits d’État OLEMISC ACTSLIKELABEL et OLEMISC \_ ACTSLIKEBUTTON.
-   L’implémentation de la propriété ambiante DisplayAsDefault (si elle existe, elle peut retourner **false**).
-   Implémentation de la gestion des onglets, y compris l’ordre de tabulation.

Certains conteneurs utilisent des contrôles ActiveX dans les scénarios de documents composés traditionnels. Par exemple, une feuille de calcul peut permettre à un utilisateur d’incorporer un contrôle ActiveX dans une feuille de calcul. Dans de tels scénarios, le conteneur effectue une gestion différente du clavier, car l’interface clavier doit rester cohérente avec les attentes de l’utilisateur d’une feuille de calcul. La documentation de ces produits doit informer les utilisateurs des différences de gestion des contrôles dans ces différents scénarios. D’autres conteneurs doivent s’efforcer d’honorer correctement les fonctionnalités ci-dessus, y compris la gestion des mnémoniques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Containers](containers.md)
</dt> </dl>

 

 




