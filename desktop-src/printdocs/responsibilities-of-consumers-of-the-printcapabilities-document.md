---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Responsabilités des consommateurs du document PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b74cfc1885ecc5599365bc6eadcef30ef4c4ae3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106522899"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a>Responsabilités des consommateurs du document PrintCapabilities

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Les consommateurs de documents PrintCapabilities présentent certaines obligations qu’ils doivent respecter avant de pouvoir utiliser un document PrintCapabilities. Les exigences suivantes s’appliquent aux clients d’un document PrintCapabilities.

-   Ils ne doivent pas rejeter ou échouer le traitement d’un PrintCapabilities valide syntaxiquement ; autrement dit, tout document PrintCapabilities conforme au schéma PrintCapabilities.

-   Ils doivent être en mesure de contourner la présence inattendue ou l’absence de contenu défini en privé. Cela comprend le contenu privé défini qui apparaît dans les instances d’éléments définis par le schéma d’impression.

-   Ils doivent être en mesure de contourner le contenu facultatif du schéma d’impression absent.

-   Ils doivent savoir quand demander un nouveau document.

    -   Les valeurs des instances de propriété sont dépendantes de la configuration (par conséquent, en fonction de l’instantané). Vous devez mettre à jour l’instantané lorsque vous accédez à une instance de propriété.

    -   Les instances Feature, option et ScoredProperty qui doivent être copiées dans un PrintTicket sont par définition statiques. Autrement dit, ils ne sont pas (et ne doivent pas être) dépendants de la configuration de l’appareil. Si vous accédez à n’importe quelle instance de ces types, vous n’avez pas besoin d’obtenir un nouveau document PrintCapabilities lorsque la configuration est modifiée.

-   Les consommateurs de PrintCapabilities qui sont des clients de l’interface utilisateur doivent être en mesure d’utiliser des informations dans un document PrintCapabilities pour construire une interface utilisateur et construire un PrintTicket valide à partir des sélections de l’utilisateur. Cela implique de savoir quelles instances ParameterInit doivent être spécifiées et de valider les instances spécifiées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



