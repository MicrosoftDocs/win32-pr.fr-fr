---
title: Prise en charge de l’exemple alloué par l’utilisateur
description: Prise en charge de l’exemple alloué par l’utilisateur
ms.assetid: c747139e-e157-4ea0-9132-256dc70e2b15
keywords:
- Windows Media Format SDK, exemple de prise en charge allouée par l’utilisateur
- ASF (Advanced Systems Format), prise en charge des exemples alloués par l’utilisateur
- ASF (format de systèmes avancés), prise en charge des exemples alloués par l’utilisateur
- prise en charge de l’exemple alloué par l’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8cba2d20586cc47845d961e5c92a0138a37d5d0db07feb23dbb68dda1b72eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845253"
---
# <a name="user-allocated-sample-support"></a>Prise en charge de l’exemple alloué par l’utilisateur

Dans des circonstances normales, l’objet lecteur et l’objet lecteur synchrone créent un nouvel objet buffer pour chaque exemple fourni à votre application. Cela est dû au fait que l’objet de lecture n’a aucun moyen de savoir ce que fait votre application avec les exemples après l’avoir extraite. Même si de nombreuses applications lisent uniquement les exemples pour les rendre immédiatement, certaines applications peuvent avoir besoin de gérer des échantillons pendant une longue période. Par conséquent, l’objet de lecture ne peut pas réutiliser les mémoires tampons qu’il alloue. elle les remet à votre application, qui les contrôle ensuite.

Le problème de cette approche est qu’un fichier peut contenir un nombre énorme d’exemples. Si chacune d’entre elles requiert la création d’un nouvel objet de mémoire tampon, l’allocation et la libération de la mémoire est beaucoup plus longue. Dans les applications sensibles au temps, telles que les lecteurs multimédias, cette surcharge peut être très préjudiciable aux performances.

Pour atténuer les problèmes de performances des exemples alloués par lecteur, le lecteur et le lecteur synchrone prennent en charge les exemples alloués par l’utilisateur. Pour utiliser des exemples alloués par votre application, l’objet de lecture effectue des appels à un exemple de méthode de rappel d’allocation que vous implémentez. La logique utilisée par le rappel pour fournir des tampons à l’objet de lecture dépend entièrement de vous. Vous pouvez utiliser un pool de mémoires tampons pour le fichier entier ou utiliser plusieurs pools de mémoires tampons, un pour chaque sortie ou flux, ou tout autre schéma qui fonctionne pour votre application.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Allocation de tampons pour la lecture de fichiers**](allocating-buffers-for-file-reading.md)
</dt> <dt>

[**Fonctionnalités de lecture de fichier**](file-reading-features.md)
</dt> </dl>

 

 




