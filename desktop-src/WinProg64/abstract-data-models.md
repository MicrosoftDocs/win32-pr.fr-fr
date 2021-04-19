---
title: Modèles de données abstraits
description: Chaque application et chaque système d’exploitation ont un modèle de données abstraites.
ms.assetid: c670d92b-e64d-4d4c-a30c-cd4fb4f2d0b9
keywords:
- modèles de données abstraites, programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bfb116d5afccba1b1ce3438f8b7135d01bc1b7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508991"
---
# <a name="abstract-data-models"></a>Modèles de données abstraits

Chaque application et chaque système d’exploitation ont un modèle de données abstraites. De nombreuses applications n’exposent pas explicitement ce modèle de données, mais le modèle repère la manière dont le code de l’application est écrit. Dans le modèle de programmation 32 bits (connu sous le nom de modèle ILP32), les types de données Integer, long et pointeurs ont une longueur de 32 bits. La plupart des développeurs ont utilisé ce modèle sans le réaliser. Pour l’historique de l’API Win32, il s’agit d’une hypothèse valide (mais pas nécessairement sécurisée) à effectuer.

Dans 64-bitWindows, cette hypothèse de parité dans les tailles de type de données n’est pas valide. La longueur de tous les types de données 64 bits gaspillerait de l’espace, car la plupart des applications n’ont pas besoin de la taille augmentée. Toutefois, les applications ont besoin de pointeurs vers des données 64 bits, et elles ont besoin de la possibilité d’avoir des types de données 64 bits dans les cas sélectionnés. Ces considérations ont conduit à la sélection d’un modèle de données abstraites appelé LLP64 (ou P64). Dans le modèle de données LLP64, seuls les pointeurs se développent jusqu’à 64 bits ; tous les autres types de données de base (entier et long) restent de 32 bits.

Au départ, la plupart des applications qui s’exécutent sur Windows 64 bits auront été portées à partir de Windows 32 bits. L’objectif est que la même source, écrite soigneusement, s’exécute sur les deux fenêtres 32 et 64 bits. La définition du modèle de données ne simplifie pas cette tâche. Toutefois, la première étape consiste à s’assurer que le modèle de données affecte uniquement les types de données de pointeur. La deuxième étape consiste à définir un ensemble de nouveaux types de données qui permettent aux développeurs de dimensionner automatiquement leurs données liées aux pointeurs. Cela permet aux données associées aux pointeurs de changer de taille lorsque la taille du pointeur passe de 32 bits à 64 bits. Les types de données de base conservent une longueur de 32 bits, de sorte qu’il n’y a aucune modification de la taille des données sur le disque, des données partagées sur un réseau ou des données partagées via des fichiers mappés en mémoire. Cela évite aux développeurs d’effectuer la plupart des efforts liés au portage de code 32 bits vers Windows 64 bits.

Ces nouveaux types de données ont été ajoutés aux fichiers d’en-tête de l’API Windows. Par conséquent, vous pouvez commencer à utiliser les nouveaux types maintenant. Pour plus d’informations, consultez [nouveaux types de données](the-new-data-types.md).

 

 




