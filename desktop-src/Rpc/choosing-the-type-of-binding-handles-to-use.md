---
title: Choix du type de descripteurs de liaison à utiliser
description: Choix du type de descripteurs de liaison à utiliser
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dd07716b3618766b3ea8aa07fb766f154285207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028924"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a>Choix du type de descripteurs de liaison à utiliser

**Bonne pratique :** Si vous savez quel serveur l’application doit utiliser, utilisez des handles explicites. Si vous ne le faites pas, utilisez des handles explicites à chaque fois, ou utilisez des handles génériques avec des routines de **\_ liaison** et de **\_ séparation** .

N’utilisez pas de handles implicites ou de handles auto. Les handles implicites ne sont pas thread-safe, et même si la sécurité des threads peut paraître inutile, cela peut devenir nécessaire ultérieurement. Les handles automatiques présentent une surcharge importante et nécessitent beaucoup de programme d’installation pour fonctionner correctement. Leurs fonctionnalités de recherche ont été remplacées par les services Active Directory.

Les handles explicites sont très efficaces et de nombreuses fonctionnalités attrayantes sont disponibles uniquement pour les handles explicites. Par exemple, si plusieurs appels RPC vont vers le même serveur, vous pouvez construire le descripteur de liaison une fois et effectuer tous les appels avec lui. Cette approche est bien plus efficace que toute autre méthode. Si le serveur vers lequel l’appel est placé est inconnu, construisez un handle de liaison explicite pour chaque appel ou utilisez des handles de liaison génériques.

Dans Microsoft™ Windows XP, le temps d’exécution RPC est très efficace lors de la réutilisation et de la mise en cache des appels. par conséquent, si le *n*+ premier appel finit sur le même serveur que le *n* ième appel, RPC réutilise les ressources allouées pour le *n* ième appel, en contournant la nécessité de mettre en cache des handles de liaison pour améliorer les performances

 

 




