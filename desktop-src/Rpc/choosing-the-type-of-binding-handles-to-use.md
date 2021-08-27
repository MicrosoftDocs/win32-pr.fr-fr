---
title: Choix du type de descripteurs de liaison à utiliser
description: Choix du type de descripteurs de liaison à utiliser
ms.assetid: b0c2c71d-c6c9-4a58-83f9-10ac9b6b214b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd35286a5bb88be3094238e0e4c43b701826bca0a7e5ad02d35c5f87f0cbdaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022919"
---
# <a name="choosing-the-type-of-binding-handles-to-use"></a>Choix du type de descripteurs de liaison à utiliser

**Bonne pratique :** Si vous savez quel serveur l’application doit utiliser, utilisez des handles explicites. Si vous ne le faites pas, utilisez des handles explicites à chaque fois, ou utilisez des handles génériques avec des routines de **\_ liaison** et de **\_ séparation** .

N’utilisez pas de handles implicites ou de handles auto. Les handles implicites ne sont pas thread-safe, et même si la sécurité des threads peut paraître inutile, cela peut devenir nécessaire ultérieurement. Les handles automatiques présentent une surcharge importante et nécessitent beaucoup de programme d’installation pour fonctionner correctement. Leurs fonctionnalités de recherche ont été remplacées par les services Active Directory.

Les handles explicites sont très efficaces et de nombreuses fonctionnalités attrayantes sont disponibles uniquement pour les handles explicites. Par exemple, si plusieurs appels RPC vont vers le même serveur, vous pouvez construire le descripteur de liaison une fois et effectuer tous les appels avec lui. Cette approche est bien plus efficace que toute autre méthode. Si le serveur vers lequel l’appel est placé est inconnu, construisez un handle de liaison explicite pour chaque appel ou utilisez des handles de liaison génériques.

dans Microsoft™ Windows XP, le temps d’exécution RPC est très efficace pour la réutilisation et la mise en cache des appels. par conséquent, si le *n*+ 1er appel finit sur le même serveur que le *n* ième appel, RPC réutilise les ressources allouées pour le *n* ième appel, en contournant la nécessité de mettre en cache des handles de liaison pour améliorer les performances.

 

 




