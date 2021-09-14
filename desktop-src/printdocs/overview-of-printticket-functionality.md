---
description: Cette vue d’ensemble de la fonctionnalité PrintTicket décrit le format permettant d’exprimer les informations de configuration de l’appareil et l’utilisation d’un PrintTicket.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Vue d’ensemble de la fonctionnalité PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90aa6f967f5fce25977b52a4d0bec7e9e1ea705
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231641"
---
# <a name="overview-of-printticket-functionality"></a>Vue d’ensemble de la fonctionnalité PrintTicket

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le PrintTicket utilise un format XML pour exprimer les informations de configuration de l’appareil à l’aide de la fonctionnalité/option et des constructions de paramètre de l’infrastructure du schéma d’impression. Cela comprend tous les types d’éléments standard, ainsi que les fonctionnalités d’extensibilité de l’infrastructure de schéma d’impression. Un PrintTicket est supposé être une description autonome de la façon dont une seule page doit être traitée. Les étapes impliquées dans l’extraction et la construction d’un tel PrintTicket à partir d’un format de document particulier ne sont pas abordées ici.

Un PrintTicket peut être utilisé pour obtenir un document PrintCapabilities décrivant les caractéristiques de l’appareil pour une configuration particulière. L’PrintTicket peut également être envoyé avec un ensemble d’instructions de rendu pour produire une page de sortie rendue et traitée en fonction de la configuration spécifiée dans PrintTicket.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



