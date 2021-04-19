---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 8084fa15-85e5-4c8d-b585-8c349482a6eb
title: Fonctionnalités et options
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866cead02021b8d933ca03483e77de832d8d094a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106524789"
---
# <a name="features-and-options"></a>Fonctionnalités et options

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Les constructions de fonctionnalité/option et de paramètre sont utilisées dans un document PrintCapabilities pour représenter des attributs d’appareil qui contribuent à la définition de la configuration de l’appareil. Pour obtenir un exemple de construction d’une fonctionnalité/option, envisagez un périphérique d’impression capable d’imprimer dans plusieurs résolutions. L’attribut d’appareil qui définit la résolution peut être représenté sous la forme d’une instance de fonctionnalité, avec chacune des valeurs de résolution de sortie possibles représentées en tant qu’instance d’option individuelle. Une instance d’option peut représenter une résolution de 300 ppp, une autre peut représenter une résolution de 600 ppp, et ainsi de suite.

Il convient de noter que le schéma d’impression exige que la liste des instances Feature, option et ParameterDef signalées dans chaque document PrintCapabilities reste constante, quelle que soit la configuration. Cela permet d’exprimer de manière non ambiguë des configurations et des dépendances sur les configurations. L’implication de cette exigence est que chaque fonctionnalité et sous-fonctionnalité doit avoir un paramètre bien défini, quel que soit le paramétrage de toute autre fonctionnalité ou sous-fonctionnalité. Par conséquent, chaque sous-fonctionnalité doit avoir une option qui est équivalente à un paramètre no-op (désactivé, désactivé ou aucun), qui est automatiquement sélectionné pour tous les sous-composants lorsque l’utilisateur sélectionne l’option no-op dans la fonctionnalité parente. À l’inverse, lorsque l’une des sous-fonctionnalités est définie sur une option activée, la fonctionnalité parente et les autres sous-fonctionnalités associées sont également activées. Entre-temps, le fournisseur PrintTicket doit garantir (pendant la validation PrintTicket) que les paramètres de toutes les instances de fonctionnalité et de sous-fonctionnalité sont définis, quelle que soit la configuration de l’appareil, et que les paramètres de la sous-fonctionnalité sont cohérents avec les paramètres de la fonctionnalité parente. Cela permet de s’assurer que l’appareil ne reçoit pas un PrintTicket incohérent dans lequel certaines sous-fonctionnalités indiquent que, par exemple, l’agrafage est activé, mais d’autres sous-fonctionnalités indiquent que l’agrafage est désactivé.

Notez que les auteurs PrintCapabilities ne sont pas tenus d’utiliser les fonctionnalités d’imbrication des éléments de fonctionnalité. S’ils préfèrent, ils peuvent présenter toutes les instances de fonctionnalités dans une structure plate, en tant que frères les unes des autres. Notez également qu’une collection imbriquée d’instances de fonctionnalités peut être aplatie simplement en déplaçant toutes les sous-fonctionnalités vers le niveau racine. La seule précaution à prendre est de s’assurer que les attributs Name de ces instances de fonctionnalités sont uniques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



