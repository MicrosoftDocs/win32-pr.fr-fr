---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilités des fournisseurs PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bbf355f7b62f8f9c8b3f3b0c59714cdd6ade5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106539150"
---
# <a name="responsibilities-of-printcapabilities-providers"></a>Responsabilités des fournisseurs PrintCapabilities

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Les fournisseurs PrintCapabilities doivent prendre en charge un ensemble minimal de fonctionnalités, qui sont implicites par l’interface du fournisseur PrintTicket/PrintCapabilities. Ces fonctionnalités sont répertoriées ici.

-   Ils doivent suivre la direction de la propagation ? Attribut XML, lorsqu’il apparaît dans le contexte approprié et contient une valeur valide pour ce contexte.

-   Ils doivent générer un document PrintCapabilities conforme au schéma PrintCapabilities et répondant aux exigences spécifiées dans le schéma d’impression.

-   Ils doivent être en mesure de reconnaître un PrintTicket valide.

-   Ils doivent être en mesure d’interpréter un PrintTicket et de comprendre la configuration spécifique qu’il représente.

-   Ils doivent être en mesure de déterminer si cette configuration contient des conflits de contrainte.

-   Ils doivent être en mesure de modifier un PrintTicket non valide ou en conflit en rendant la modification la moins importante nécessaire pour qu’il soit valide et sans conflit.

-   Ils doivent être en mesure de générer un document PrintCapabilities pour une configuration d’appareil particulière.

-   Ils doivent être en mesure de générer une configuration par défaut ou un PrintTicket.

-   Ils doivent être en mesure de générer un document PrintCapabilities qui correspond à la configuration par défaut.

-   Ils doivent implémenter un processus de notation des options défini par le pilote de périphérique capable de déterminer la proximité de la correspondance entre deux instances d’option qui appartiennent à la même fonctionnalité. Cet algorithme est utilisé dans le processus de validation PrintTicket.

En plus des exigences ci-dessus, le document PrintCapabilities doit contenir des valeurs valides et correctes pour chaque attribut XML (par exemple, contractions) de chaque option.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



