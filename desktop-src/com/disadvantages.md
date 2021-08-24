---
title: Inconvénients
description: Inconvénients
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2b9d41a632c202a25c3383ffb2d1069505c0dc988651e9fc886cfeecca5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501112"
---
# <a name="disadvantages"></a>Inconvénients

Les serveurs in-process fournissent l’avantage de vitesse et de taille d’un gestionnaire d’objets avec la fonction de modification d’un serveur local. Pourquoi choisir d’implémenter votre application OLE en tant que serveur local plutôt qu’en tant que serveur in-process ? Il existe plusieurs raisons à cela :

-   Sécurité. Seul un serveur local a son espace d’adressage isolé de celui du client. Un serveur in-process partage l’espace d’adressage et le contexte de processus du client et peut donc être moins fiable face aux erreurs ou à la programmation malveillante.
-   Granularité. Un serveur local peut héberger plusieurs instances de son objet sur de nombreux clients différents, en partageant l’état du serveur entre des objets de plusieurs clients de manière difficile ou impossible à implémenter en tant que serveur in-process, qui est simplement une DLL chargée dans chaque client.
-   Compatibilité. Si vous choisissez d’implémenter un serveur in-process, vous abandonnez la compatibilité avec OLE 1, qui ne prend pas en charge ces serveurs. Ce n’est pas une considération pour de nombreux développeurs, mais si c’est le cas, il s’agit d’un problème critique.
-   Impossible de prendre en charge les liens. Un serveur in-process ne peut pas servir de source de liaison. Étant donné qu’une DLL ne peut pas s’exécuter elle-même, elle ne peut pas créer d’objet de fichier à lier.

Malgré ces inconvénients, un serveur in-process peut être un excellent choix pour sa vitesse et sa taille, s’il répond à toutes vos exigences.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Avantages](advantages.md)
</dt> <dt>

[Serveurs in-process](in-process-servers.md)
</dt> </dl>

 

 




