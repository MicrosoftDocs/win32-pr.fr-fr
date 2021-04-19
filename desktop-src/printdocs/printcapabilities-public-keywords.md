---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Mots clés publics PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d5e7b001a8106f95c830f0af5e99ee9821af64
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106523760"
---
# <a name="printcapabilities-public-keywords"></a>Mots clés publics PrintCapabilities

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

La section suivante spécifie les éléments configurables par l’utilisateur et les définitions de paramètres qui peuvent s’appliquer à un document PrintCapabilities.

## <a name="user-configurable-elements-usage"></a>Utilisation des éléments configurables par l’utilisateur

Les éléments configurables par l’utilisateur représentent les mots clés publics du schéma d’impression, qui peuvent apparaître dans un document PrintCapabilities ou un PrintTicket. Ils sont destinés à représenter des attributs d’appareil configurables pris en charge par un appareil spécifique ou à communiquer des intentions de paramètres d’impression par une application ou un utilisateur.

Les éléments configurables par l’utilisateur peuvent référencer des éléments de référence de paramètre. Pour plus d’informations, reportez-vous à la section [éléments de référence de paramètre](parameter-reference-elements.md) .

## <a name="parameter-definitions-usage"></a>Utilisation des définitions de paramètres

Les définitions de paramètres prennent la forme de types d’éléments ParameterDef dans un document de fonctionnalités d’impression. Les types d’éléments ParameterDef sont initialisés dans un PrintTicket à l’aide du type d’élément ParameterInit. La valeur du paramètre est spécifiée à l’aide de l’élément ParameterInit. Un mot clé configurable par l’utilisateur peut faire référence à une définition de paramètre à l’aide du type d’élément ParameterRef. Pour plus d’informations, consultez la section [constructions de paramètres](parameter-constructs.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



