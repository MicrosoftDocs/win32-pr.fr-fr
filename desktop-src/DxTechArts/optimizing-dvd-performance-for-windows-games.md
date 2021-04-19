---
title: Optimisation des performances des DVD pour les jeux Windows
description: Cet article explique comment optimiser les performances des DVD pour les jeux Windows.
ms.assetid: 01e8dc7d-4ba7-40dd-d845-a20000201ae1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb15063d0441423ccb3a9f67db84caa134f801c6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511299"
---
# <a name="optimizing-dvd-performance-for-windows-games"></a>Optimisation des performances des DVD pour les jeux Windows

Un pourcentage élevé d’ordinateurs qui exécutent Windows ont un lecteur de DVD, et de nombreux jeux sont livrés sur DVD. Par conséquent, nous vous recommandons de vous assurer que vos jeux utilisent le lecteur de DVD pour tirer pleinement parti. En comprenant comment les données sont lues à partir d’un DVD et comment l’emplacement des données affecte le temps de lecture, vous pouvez réduire les temps de chargement et améliorer les performances globales lors du jeu. Cet article explique comment optimiser les performances des DVD pour les jeux Windows.

-   [Disposition de base d’un DVD](#basic-layout-of-a-dvd)
-   [Lecture à partir d’un DVD](#reading-from-a-dvd)
-   [Lecture des erreurs](#reading-errors)
-   [Débit de données](#data-throughput)
-   [Exemples de débit gaspillé](#examples-of-wasted-throughput)
-   [Lire de façon synchrone ou asynchrone](#reading-synchronously-vs-asynchronously)
-   [Lecture optimale](#reading-optimally)
-   [Compatibilité DVD](#dvd-compatibility)
-   [Résumé](#summary)

## <a name="basic-layout-of-a-dvd"></a>Disposition de base d’un DVD

Cette illustration montre la mise en page de base d’un DVD.

![disposition DVD](images/dvdsector.png)

Les données d’un DVD sont stockées en spirale continue, comme sur un CD ; Toutefois, les fichiers sont divisés en blocs et secteurs. Les fichiers sont répartis sur des blocs ECC (error correction code) et chaque bloc est divisé en secteurs de 16 2 Ko (c’est-à-dire 32 Ko de données dans chaque bloc). Les fichiers sont alignés le long des limites du secteur et tout espace inutilisé dans un secteur reste vide. Si un fichier n’a que 10 octets, le reste de l’espace dans ce secteur de 2 Ko est gaspillé. Si possible, regroupez les fichiers en incréments de 2 Ko pour obtenir la meilleure densité de données. N’oubliez pas que ces spécifications concernent uniquement les DVD et que les CD et HD-DVD présentent des spécifications différentes.

## <a name="reading-from-a-dvd"></a>Lecture à partir d’un DVD

Voici la séquence qu’un lecteur de DVD exécute lors de la réception d’une demande de lecture à partir d’un DVD :

1.  Modifier les couches, si nécessaire
2.  Seek
3.  Refocaliser l’unité de collecte optique (OPU) pour lire les données
4.  Vérifier la position réelle
5.  Ajuster et répéter jusqu’à la détection des données correctes

Les opérations de lecture de lecteur sont quantifiées différemment, selon qu’il s’agit de lectures de lecteurs logiques ou de lectures de lecteurs physiques. Les lectures de lecteurs logiques peuvent uniquement lire une quantité entière de secteurs DVD, tandis qu’une requête de lecture de lecteur physique peut uniquement lire une quantité entière de blocs ECC. En règle générale, le lecteur physique reçoit une demande de lecture ; il essaiera de remplir son cache. La taille du cache du lecteur de DVD dépend des spécifications de chaque lecteur.

Lorsqu’un lecteur de DVD reçoit une demande de lecture qui dépasse la taille du cache, la demande est décomposée en demandes de taille de cache. Le lecteur recherche le bloc ECC qui contient le premier secteur de la demande et lit l’intégralité du bloc ECC. Le microprogramme de lecteur décode le bloc ECC, puis lit le bloc ECC suivant. Le processus se répète jusqu’à ce que le cache du lecteur soit rempli ou que toutes les demandes soient satisfaites. Le noyau lit ensuite les données décodées à partir du cache du lecteur. Il vide ensuite le cache et démarre l’opération de lecture suivante, si des demandes de lecture sont conservées.

> [!Note]  
> Chaque lecture non mise en cache vide le cache du lecteur.

 

## <a name="reading-errors"></a>Lecture des erreurs

Les DVD et les lecteurs DVD ne sont pas parfaits, et des erreurs peuvent se produire pendant la lecture. Comme les CDs, les portions d’un DVD peuvent devenir illisibles de la poussière ou des éraflures. Si une partie d’un bloc est illisible, le bloc entier est considéré comme illisible. Si une erreur de lecture se produit, le lecteur tente à nouveau de lire le bloc ECC. Si le bloc est toujours illisible, le lecteur abandonne l’opération de lecture et retourne une valeur au noyau qui indique que le bloc n’a pas été lu. Le noyau décide ensuite de l’étape à suivre. Le noyau peut soit réémettre la demande, abandonner la lecture complètement, soit faire tourner le lecteur et réexécuter la requête.

## <a name="data-throughput"></a>Débit de données

Le débit de données d’un lecteur de DVD dépend de plusieurs facteurs : l’emplacement des données demandées, le nettoyage ou le grattage du disque, le nombre de flux lus à partir du disque, la taille des mémoires tampons associées à ces flux et les spécifications du lecteur individuel. Le débit varie également selon que le lecteur dispose d’une vélocité angulaire constante (CAV) ou d’une vélocité linéaire constante (CLV). Si un lecteur tourne avec CAV, le disque tourne à la même vitesse, quel que soit l’endroit où se trouve l’unité de collecte optique (OPU). Cela signifie que la piste de données se déplace au-delà de la OPU plus rapidement, car le OPU est plus proche du bord extérieur du disque. Avec CLV, le disque tourne plus lentement au fur et à mesure que le OPU progresse vers l’extérieur, de sorte que la piste de données passe au-delà du OPU à une vitesse constante. Les lecteurs de DVD sur la plupart des PC utilisent CLV.

Pendant que le lecteur recherche et modifie les couches, les données ne peuvent pas être lues à partir du disque. Il est conseillé de réduire ces opérations, en particulier lors de la lecture de données pour un écran de chargement initial.

## <a name="examples-of-wasted-throughput"></a>Exemples de débit gaspillé

Pour comprendre comment les données peuvent être perdues, envisagez un lecteur et un DVD hypothétiques. Supposons qu’un fichier au milieu du disque doit être lu. Le débit de cette zone du disque est d’environ 8,25 Mo/s. Si le trait de recherche est un demi-entier ou un troisième, le temps de recherche moyen est de 150 ms. Dans cet exemple, 1,2 Mo (150 ms × 8,25 Mo/s) ont peut-être été lus dans le temps qu’il a fallu pour obtenir le OPU à l’emplacement où il peut être lu. L’ajout d’une modification de couche augmente le débit perdu à 1,8 Mo (225 ms × 8,25 Mo/s).

Un autre exemple illustrant le débit perdu est le chargement de 20 fichiers mal installés à partir d’un lecteur CAV sans aucune modification de couche. Si le temps de recherche de chaque fichier, plus la latence avant que les données ne puissent être lues, est d’environ 200 ms, puis 4 secondes (20 fichiers × 200 ms) sont consacrées à la recherche des données. Si les fichiers se trouvent sur le diamètre externe et sont lus à 11 × vitesse, la moyenne du débit 15,2 Mo/s (11 vitesse/12 Vitesse × 16 Mo/s). Le débit perdu dans cet exemple est d’environ 60,8 Mo (15,2 Mo/s × 4 s).

## <a name="reading-synchronously-vs-asynchronously"></a>Lire de façon synchrone ou asynchrone

La lecture asynchrone est plus efficace que la lecture synchrone. Lors de la lecture de manière synchrone, un ou plusieurs blocs ECC de données sont lus dans la mémoire système avant d’être copiés dans la mémoire de l’application. En revanche, la lecture asynchrone copie les blocs ECC décodés directement dans la mémoire de l’application, ce qui permet d’éviter le cache L2 et de réduire la surcharge du processeur. Pour lire de façon asynchrone, utilisez l' \_ indicateur de chevauchement de l’indicateur de fichier \_ lors de l’utilisation de la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir des fichiers. La fonction [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) a également besoin d’une structure OVERLAPPED valide passée pour exécuter des e/s asynchrones.

Vous trouverez plus d’informations sur les e/s asynchrones dans [les e/s synchrones et asynchrones](/windows/desktop/FileIO/synchronous-and-asynchronous-i-o).

## <a name="reading-optimally"></a>Lecture optimale

Le meilleur principe à lire à partir d’un DVD est d’éviter de rechercher et de lire de petites quantités de données. Lorsque la quantité de données lues est inférieure à la capacité d’un bloc ECC (inférieure à 32 Ko), le reste du bloc est perdu. Étant donné que les tailles de cache varient d’un lecteur à l’autre, les développeurs doivent décider d’une quantité minimale de données pour les requêtes de lecture et ne pas en réduire la taille. La taille minimale doit être un entier multiple d’un bloc ECC pour éviter de perdre du temps à lire et décoder les données qui ne seront pas utilisées. Il est également important de ne pas rechercher tous les coûts, car tout le temps passé à la recherche est le temps passé à ne pas lire les données.

## <a name="dvd-compatibility"></a>Compatibilité DVD

Certains problèmes de compatibilité importants doivent être pris en compte lors de la publication sur DVD. Tout d’abord, les lecteurs de DVD des ordinateurs Windows peuvent varier en termes de performances. par conséquent, si votre DVD a une exigence spécifique pour le débit, il est important de s’assurer que le matériel de vos utilisateurs répond à ces exigences. En outre, les DVD multicouches peuvent entraîner des problèmes de compatibilité sur certains lecteurs de DVD. Pour éviter ces problèmes, il est recommandé de fournir un DVD à une seule couche ou de tester minutieusement un DVD multicouche sur une majorité de lecteurs avant la version finale.

## <a name="summary"></a>Résumé

Pour améliorer les performances des DVD, certaines règles générales peuvent être appliquées. Les techniques suivantes peuvent permettre d’optimiser le débit et de réduire les pertes de données :

-   Évitez les lectures inférieures à 32 Ko
-   Disposer des données pour réduire ou éliminer les recherches
-   Disposer des données sur les limites de bloc ECC
-   Optimisez la capacité en regroupant de petits fichiers en blocs de 2 Ko et en réduisant l’espace de remplissage dans les secteurs des DVD
-   Lecture asynchrone pour réduire la charge de l’UC et l’utilisation excessive de la mémoire
-   Éviter de libérer des DVD multicouches

 

 