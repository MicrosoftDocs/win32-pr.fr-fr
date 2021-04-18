---
title: Fonctionnement de l’exemple Echo
description: Fonctionnement de l’exemple Echo
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- Plug-ins du lecteur Windows Media, vue d’ensemble de l’exemple Echo
- plug-ins, vue d’ensemble de l’exemple Echo
- plug-ins de traitement de signal numérique, vue d’ensemble de l’exemple Echo
- Plug-ins DSP, vue d’ensemble de l’exemple Echo
- Echo DSP, exemple de plug-in, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08814a6f0d604c7d566a0fc8d9f07b05446fca64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509391"
---
# <a name="how-the-echo-sample-works"></a>Fonctionnement de l’exemple Echo

Le code crée l’effet ECHO en allouant une mémoire tampon suffisamment grande pour contenir exactement la quantité de données audio qui peuvent être rendues dans l’intervalle de temps spécifié par la valeur Delay Time. La taille de la mémoire tampon est calculée, en octets, par la formule suivante :

taille de la mémoire tampon = taux d’échantillonnage de délai \* / \* alignement de bloc 1000

Le délai est exprimé en millisecondes. Le taux d’échantillonnage et les valeurs d’alignement de bloc sont fournis dans une structure WAVEFORMATEX. Le taux d’échantillonnage est en échantillons par seconde ; la division par 1000 donne des échantillons par milliseconde. L’alignement du bloc est égal au produit du nombre de canaux (1 pour mono, 2 pour stéréo) et du nombre de bits par échantillon (8 ou 16) divisé par 8 (bits par octet).

En plus de la variable pointeur qui pointe vers le début de la mémoire tampon de délai, le code crée un pointeur mobile qui parcourt les données dans la mémoire tampon en synchronisation avec la boucle de traitement dans la fonction **DoProcessOutput** . Lorsque le pointeur mobile atteint la fin de la mémoire tampon de retard, il revient à l’en-tête de la mémoire tampon. Une mémoire tampon utilisée de cette manière est appelée mémoire tampon circulaire.

Une fois que la mémoire tampon de délai existe et que le lecteur Windows Media a alloué une mémoire tampon d’entrée pour fournir des données audio et une mémoire tampon de sortie pour recevoir les données audio traitées, le traitement des échos se déroule comme suit :

1.  Entrez une boucle qui autorise le traitement de chaque échantillon audio dans la mémoire tampon d’entrée.
2.  Récupérez un exemple de la mémoire tampon d’entrée. Ensuite, déplacez le pointeur de la mémoire tampon d’entrée vers l’exemple suivant pour préparer l’itération de la boucle suivante.
3.  Récupérez un exemple de la mémoire tampon de délai.
4.  Copiez l’exemple à partir de la mémoire tampon d’entrée vers le même emplacement dans la mémoire tampon de délai à partir de laquelle l’échantillon de dernier retard a été récupéré.
5.  Déplacez le pointeur de mémoire tampon de délai vers l’exemple suivant. Si le pointeur se déplace au-delà de la fin de la mémoire tampon, déplacez-le vers l’en-tête de la mémoire tampon.
6.  Associez l’exemple de la mémoire tampon d’entrée à l’exemple de la mémoire tampon de délai.
7.  Copiez le résultat dans la mémoire tampon de sortie. Ensuite, déplacez le pointeur de la mémoire tampon de sortie vers l’unité suivante pour préparer l’itération de la boucle suivante.
8.  Répétez l’opération jusqu’à ce que tous les exemples soient traités.

Lorsqu’un exemple d’entrée récupéré à l’étape 2 est copié dans la mémoire tampon de délai de l’étape 4, il reste là jusqu’à ce que le pointeur mobile effectue un pas à pas détaillé dans la mémoire tampon de retard et finalement retourne à la même position. Étant donné que la taille de la mémoire tampon de délai est conçue pour correspondre au délai, le temps écoulé entre l’échantillon copié dans la mémoire tampon de retard et l’échantillon récupéré une nouvelle fois est égal au délai spécifié (plus toute latence introduite par le traitement réel).

Lorsqu’un flux démarre, aucune donnée de délai n’est générée tant que le délai n’est pas écoulé. Par conséquent, il est important que la mémoire tampon de délai contienne initialement un silence. Si la mémoire tampon de délai contient des données aléatoires, l’utilisateur entendra un bruit blanc jusqu’à ce que le plug-in génère suffisamment de données de délai pour remplacer l’intégralité de la mémoire tampon de retard.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble de l’exemple Echo**](echo-sample-overview.md)
</dt> </dl>

 

 




