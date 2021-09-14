---
description: Apprenez à prendre en charge différentes versions de l’infrastructure du schéma d’impression. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: fc89dd2d-9a5d-400b-aee9-a1e4cf7d83da
title: Versions de schéma de prise en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eac627d3dd711bc952d881efd393720af128e7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117990"
---
# <a name="supporting-schema-versions"></a>Versions de schéma de prise en charge

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

L’infrastructure du schéma d’impression est susceptible de changer à l’avenir à mesure que de nouveaux besoins se présentent. Ces modifications sont censées être très rares, car la modification la plus courante est l’introduction de nouveaux noms d’instance. Cette modification n’affecte pas la structure de l’infrastructure et doit être transparente pour les clients et les fournisseurs. Toute modification apportée à la structure et à l’organisation de l’infrastructure du schéma d’impression est identifiée par un incrément de son numéro de version. Les ajouts aux mots clés du schéma d’impression ne sont pas identifiés. Les fournisseurs PrintTicket doivent être en mesure de prendre en charge la version actuelle de l’infrastructure du schéma d’impression, ainsi que toute version antérieure. La version de l’infrastructure du schéma d’impression est identifiée à l’aide de l’attribut XML : version qui apparaît à l’élément racine du PrintTicket.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



