---
description: Cet article spécifie les mots clés publics qui sont définis pour le schéma d’impression et leur utilisation pour PrintCapabilities et PrintTicket.
ms.assetid: ff966475-626d-4a48-9349-e60454d47c57
title: Mots clés publics du schéma d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbcab9ce943b7f344ce12c378252bc07c69260f75c607b36f7af54c107d3f84a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886359"
---
# <a name="print-schema-public-keywords"></a>Mots clés publics du schéma d’impression

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

La section suivante spécifie les mots clés publics qui sont définis pour le schéma d’impression.

## <a name="print-schema-public-keywords-usage-for-print-capabilities"></a>Utilisation des mots clés publics du schéma d’impression pour les fonctionnalités d’impression

Les mots clés spécifiés sous les mots clés publics PrintCapabilities peuvent apparaître dans un document de fonctionnalités d’impression. Pour plus d’informations sur la façon dont ces mots clés interagissent avec la technologie PrintCapabilities, consultez [vue d’ensemble de la section PrintCapabilities](overview-of-the-printcapabilities.md) .

Les mots clés publics spécifiques à PrintTicket ne doivent pas apparaître dans un document PrintCapabilities.

## <a name="print-schema-public-keywords-usage-for-printticket"></a>Utilisation des mots clés publics du schéma d’impression pour PrintTicket

Les mots clés spécifiés sous les mots clés publics PrintTicket peuvent apparaître dans un PrintTicket. Les mots clés PrintTicket sont implémentés en tant que type d’élément de propriété. Pour plus d’informations sur la façon dont ces mots clés interagissent avec la technologie PrintTicket, consultez les [informations de configuration non liées à](configuration-information-not-related-to-printcapabilities.md) la section PrintCapabilities.

Les mots clés spécifiés sous les mots clés publics PrintCapabilities peuvent apparaître dans un PrintTicket en fonction de l’implémentation de PrintTicket dans une application et/ou un pilote. Cela permet de sélectionner les attributs d’appareil définis dans le document PrintCapabilities. Pour plus d’informations sur l’interaction entre les mots clés PrintCapabilities et PrintTicket, reportez-vous à [l’objectif de la section PrintTicket](purpose-of-the-printticket.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



