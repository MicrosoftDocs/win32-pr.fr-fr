---
title: Être non exclusif
description: Être non exclusif
ms.assetid: 7a44840d-6bf9-4c12-ba14-66d7067a984d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b637bcf0860ccc4917b1af344664f9828b0da8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379772"
---
# <a name="be-non-exclusive"></a>Être non exclusif

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Les caractères interactifs peuvent être utilisés dans l’interface utilisateur en tant qu’assistants, guides, artisteseurs, réciteurs, agents commerciaux ou dans divers autres rôles. Un caractère qui effectue ou aide automatiquement ne doit pas être conçu de façon contraire au principe de conception permettant de garder le contrôle de l’utilisateur. Lorsque vous ajoutez un caractère à l’interface d’un site Web ou d’une application conventionnelle, utilisez le caractère comme une amélioration plutôt qu’un remplacement de l’interface principale. Évitez d’implémenter une fonctionnalité ou une opération qui requiert en exclusivité un caractère.

De même, permettez à l’utilisateur de choisir le moment où il souhaite interagir avec votre caractère. Un utilisateur doit être en mesure de faire disparaître le caractère et de le faire retourner uniquement avec l’autorisation de l’utilisateur. L’interaction forcée des caractères sur les utilisateurs peut avoir un effet négatif sérieux. Pour prendre en charge le contrôle utilisateur de l’interaction de caractères, Microsoft Agent comprend automatiquement les commandes masquer et afficher. L’API Microsoft agent prend également en charge ces méthodes. vous pouvez donc inclure la prise en charge de ces fonctions dans votre propre interface. En outre, l’interface utilisateur de Microsoft Agent comprend des propriétés globales qui permettent à l’utilisateur de remplacer certaines options de sortie de caractères. Pour vous assurer que les préférences de l’utilisateur sont conservées, ces propriétés ne peuvent pas être remplacées par le biais de l’API.

 

 




