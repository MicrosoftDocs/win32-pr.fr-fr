---
description: Découvrez comment PrintTicket et PrintCapabilities gèrent les options paramétrables et non paramétrées.
ms.assetid: 92438df1-afde-4038-853e-9b98f7e589ea
title: Options paramétrées et options non paramétrées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4c788eaf2fa08f4f29a541a775d2bcbf523aa51
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407222"
---
# <a name="parameterized-options-versus-nonparameterized-options"></a>Options paramétrées et options non paramétrées

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Les fournisseurs PrintCapabilities et PrintTicket doivent gérer correctement les instances d’option paramétrable pendant le processus de validation PrintTicket. Comme indiqué dans [définitions d’options](option-definitions.md), une étape effectuée dans la validation PrintTicket consiste à trouver l’option dans le document PrintCapabilities de l’appareil actif (l’option candidate) qui correspond le mieux à l’option spécifiée dans PrintTicket (l’option de référence). Quand l’une des instances d’option ou les deux sont paramétrables, il existe trois cas possibles qui doivent être gérés par le processus de notation défini par le pilote de périphérique : le cas où les deux instances d’option sont paramétrables et les deux cas où une option est paramétrable et l’autre non. Dans les cas suivants, on suppose qu’il existe une correspondance entre les instances ScoredProperty paramétrables dans l’option PrintTicket et un ScoredProperty particulier dans l’option PrintCapabilities. En l’absence de correspondance, le processus de notation peut traiter ces instances ScoredProperty de la même manière qu’une autre instance ScoredProperty non correspondante.

## <a name="case-1---parameterized-printticket-and-printcapabilities-document-options"></a>Cas 1-options du document PrintTicket et PrintCapabilities paramétrées

Dans ce cas, l’option reference (dans PrintTicket) et l’option candidat (dans le document PrintCapabilities) sont paramétrables. Accédez à l’instance ParameterDef référencée par l’option candidat (à la fois dans le document PrintCapabilities) et déterminez si la valeur ParameterInit spécifiée dans PrintTicket est comprise dans la plage autorisée par l’instance ParameterDef. Si c’est le cas, considérez ce ScoredProperty comme une correspondance. Dans le cas contraire, ce ScoredProperty n’est pas une correspondance.

## <a name="case-2---parameterized-printticket-option-nonparameterized-printcapabilities-document-option"></a>Cas 2-option PrintTicket paramétrable, option de document PrintCapabilities non paramétrable

Dans ce cas, PrintTicket contient une fonctionnalité avec une option paramétrée, tandis que la fonctionnalité correspondante dans le document PrintCapabilities contient au moins une option qui n’est pas paramétrable. Même si le document PrintCapabilities contient également d’autres instances d’option paramétrées, le processus de notation doit être appliqué à chaque option, car l’objectif est d’identifier la meilleure option correspondante. Le client doit être en mesure de comparer les options candidates non paramétrées à une option de référence paramétrée.

Étant donné que l’option paramétrable apparaît dans PrintTicket, les instances ParameterInit doivent également être présentes, comme illustré dans le cas précédent. Le processus de calcul de score peut simplement remplacer n’importe quelle instance ParameterRef dans l’option paramétrable de PrintTicket par la valeur spécifiée par l’instance ParameterInit de PrintTicket. Cela convertit efficacement une option paramétrable en une option qui n’est pas paramétrable. À ce stade, le processus de correspondance conventionnel peut être utilisé.

## <a name="case-3---nonparameterized-printticket-option-parameterized-printcapabilities-document-option"></a>Cas 3-option PrintTicket non paramétrée, option de document PrintCapabilities paramétrable

Dans ce cas, l’option Reference dans PrintTicket n’est pas paramétrable, tandis que l’option candidat dans le document PrintCapabilities est paramétrable. Accédez à l’instance ParameterDef dans le document PrintCapabilities qui est référencé par l’instance ParameterRef de l’option candidat dans le PrintTicket, et déterminez si la valeur définie dans l’option de référence pour le ScoredProperty correspondant est comprise dans la plage autorisée par l’instance ParameterDef. Si c’est le cas, considérez ce ScoredProperty comme une correspondance. Si ce n’est pas le cas, ce ScoredProperty n’est pas une correspondance.

Il convient de mettre l’accent sur la détermination de la correspondance entre deux instances d’option et le nombre (et la précision) des instances de ScoredProperty qui correspondent, indépendamment du fait que les instances de ScoredProperty contiennent des instances de valeur explicite ou des instances de ParameterRef. Il est possible qu’une option candidate soit la meilleure correspondance, même si elle contient plusieurs instances de propriété qui ne correspondent pas à celles de l’option de référence, ou qui n’ont pas de propriété correspondante dans l’option de référence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



