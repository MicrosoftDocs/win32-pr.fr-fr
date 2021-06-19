---
description: Découvrez comment l’auteur d’un client PrintTicket peut utiliser les types d’éléments pour créer un PrintTicket qui décrit les intentions d’un appareil.
ms.assetid: ed53d1a8-d302-4855-9858-0f37dfbbd1d3
title: Listes de vérification de la construction PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76d47911d0060cc6d06604bfaeaa4abcebd3daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405472"
---
# <a name="printticket-construction-checklists"></a>Listes de vérification de la construction PrintTicket

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Cette section montre comment l’auteur d’un client PrintTicket peut utiliser les types d’éléments définis dans l’infrastructure du schéma d’impression pour créer un PrintTicket qui décrit les intentions d’un appareil. Le PrintTicket peut être générique (non lié à un appareil spécifique) ou il peut être spécifique à l’appareil. La sémantique du PrintTicket est présentée plus en détail. En outre, cette section contient une vue d’ensemble des concepts et de la terminologie qui sont traités plus en détail dans les sections suivantes.

Il existe deux approches fondamentalement différentes de la construction d’un PrintTicket. Vous pouvez utiliser l’une ou l’autre de ces approches.

-   Ciblez le PrintTicket sur un appareil inconnu ou générique en [créant un PrintTicket générique](creating-a-generic-printticket.md).

    Si votre objectif principal est de préserver l’intention de l’utilisateur final, vous souhaiterez peut-être adopter cette approche, en construisant et en stockant un PrintTicket générique non validé avec le document.

-   Ciblez le PrintTicket sur un appareil spécifique, en [créant un Device-Specific PrintTicket](creating-a-device-specific-printticket.md).

    Si vous souhaitez tirer parti de toutes les fonctionnalités offertes par un appareil particulier, vous souhaiterez peut-être adopter cette approche, en construisant un PrintTicket pour l’appareil spécifique et en stockant le PrintTicket validé avec le document.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



