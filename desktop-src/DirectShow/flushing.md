---
description: Vidage
ms.assetid: 868218c4-3e1a-4da0-89fa-30a9848da0e8
title: Vidage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e70f610a68b2ca81afff736b3e7402d80e5d5675e429d1715ebebf5b640a362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401743"
---
# <a name="flushing"></a>Vidage

Pendant l’exécution du graphique de filtre, des quantités arbitraires de données peuvent être déplacées dans le graphique. Certaines d’entre elles peuvent être dans des files d’attente, en attente de remise. Il arrive parfois que le graphique de filtre doive supprimer ces données en attente aussi rapidement que possible et les remplacer par de nouvelles données. Après une commande Seek, par exemple, le filtre source génère des échantillons à partir d’une nouvelle position dans la source. Pour réduire la latence, les filtres en aval doivent ignorer les exemples qui ont été créés avant la commande Seek. Le processus d’abandon des exemples s’appelle le *vidage*. Cela permet au graphique d’être plus réactif lorsque les événements modifient le workflow de données normal.

Le vidage est géré légèrement différemment par le modèle d’extraction. Cet article commence par décrire le modèle push. Il décrit ensuite les différences dans le modèle d’extraction.

Le vidage se produit en deux étapes.

-   Tout d’abord, le filtre source appelle [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sur la broche d’entrée du filtre en aval. Le filtre en aval commence à rejeter les exemples de en amont. Il ignore également tous les exemples qu’il contient et envoie l’appel **BeginFlush** en aval au filtre suivant.
-   Lorsque le filtre source est prêt à envoyer de nouvelles données, il appelle [**IPIN :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sur la broche d’entrée. Cela indique au filtre en aval qu’il peut recevoir de nouveaux exemples. Le filtre en aval envoie l’appel **EndFlush** au filtre suivant.

Dans la méthode **BeginFlush** , la broche d’entrée effectue les opérations suivantes :

1.  Appelle **BeginFlush** sur les broches d’entrée en aval.
2.  Rejette les autres appels qui diffusent des données, notamment **Receive** et **EndOfStream**.
3.  Débloque tous les filtres en amont qui sont bloqués en attente d’un échantillon à partir de l’allocateur du filtre. Certains filtres annulent la validation de leurs allocateurs à cet effet.
4.  Quitte toutes les attentes qui bloquent la diffusion en continu. Par exemple, les filtres de convertisseur sont bloqués lorsqu’ils sont en pause. Ils sont également bloqués lorsqu’ils sont en attente de rendu d’un exemple au moment du flux correct. Le filtre doit débloquer, de sorte que les exemples en attente en attente peuvent être remis et rejetés. Cette étape garantit que tous les filtres en amont finissent par débloquer.

Dans la méthode **EndFlush** , la broche d’entrée effectue les opérations suivantes :

1.  Attend que tous les échantillons mis en file d’attente soient ignorés.
2.  Libère toutes les données mises en mémoire tampon. Cette étape peut parfois être effectuée dans la méthode **BeginFlush** . Toutefois, **BeginFlush** n’est pas synchronisé avec le thread de streaming. Le filtre ne doit pas traiter ni mettre en mémoire tampon plus de données entre l’appel à **BeginFlush** et l’appel à **EndFlush**.
3.  Efface toutes les notifications d’achèvement EC en attente \_ .
4.  Appelle **EndFlush** en aval.

À ce stade, le filtre peut à nouveau accepter des exemples. Tous les échantillons sont garantis comme étant plus récents que le vidage.

Dans le modèle d’extraction, le filtre de l’analyseur lance le vidage, plutôt que le filtre source. Non seulement elle appelle **IPIN :: BeginFlush** et **IPIN :: EndFlush** sur le filtre en aval, mais elle appelle également [**IAsyncReader :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-beginflush) et [**IAsyncReader :: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-endflush) sur la broche de *sortie* du filtre source. Si le filtre source a des demandes de lecture en attente, il les ignore.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidage des données](flushing-data.md)
</dt> </dl>

 

 



