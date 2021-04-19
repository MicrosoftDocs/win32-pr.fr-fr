---
description: Le schéma d’impression et les technologies associées sont disponibles dans Microsoft .NET Framework 3,0 et versions ultérieures de Microsoft .NET Framework, et dans Windows Vista et les versions ultérieures de Windows.
ms.assetid: 98d5f8ec-54bd-4e88-b632-ed427b599cb6
title: Schéma d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3ac50b9a2f2aba9cda7dc73f183e1f3571cc9d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106531258"
---
# <a name="print-schema"></a>Schéma d’impression

Le schéma d’impression et les technologies associées sont disponibles dans Microsoft .NET Framework 3,0 et versions ultérieures de Microsoft .NET Framework, et dans Windows Vista et les versions ultérieures de Windows. Les documents XPS et le modèle d’objet XPS peuvent utiliser les objets ticket d’impression, décrits dans la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip), pour spécifier les préférences d’impression d’un document pour les imprimantes et l’affichage des applications.

La [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) est un document téléchargeable qui contient des informations sur le schéma d’impression et comment l’utiliser dans des documents et l’impression. Des informations supplémentaires sont fournies en ligne uniquement à titre d’information, au niveau de [Référence du schéma d’impression hérité](print-schema.md). Toutefois, il peut ne pas refléter avec précision la version actuelle de la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip). Reportez-vous à la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) pour obtenir les informations de conception les plus récentes.

## <a name="print-schema-overview"></a>Vue d’ensemble du schéma d’impression

Le schéma d’impression est un schéma XML structuré hiérarchiquement qui est utilisé pour organiser et décrire les propriétés d’une imprimante ou d’un travail d’impression. Le schéma d’impression comprend deux composants : les mots clés du schéma d’impression et l’infrastructure du schéma d’impression. Les mots clés du schéma d’impression sont un ensemble d’instances d’éléments qui décrivent les attributs d’imprimante et l’intention de mise en forme du travail d’impression. L’infrastructure du schéma d’impression définit une collection hiérarchique de types d’éléments XML et la façon dont ces types d’éléments peuvent être utilisés ensemble.

Les technologies de schéma d’impression, appelées *PrintCapabilities* et *PrintTicket*, sont créées à l’aide des mots clés du schéma d’impression, comme spécifié par l’infrastructure du schéma d’impression. La spécification du schéma d’impression prend en charge les extensions de schéma par des tiers, de sorte que les utilisateurs du schéma d’impression ne sont pas limités aux instances Property, Feature, option ou ParameterInit définies par les mots clés du schéma d’impression. Des instances d’élément tierces peuvent être ajoutées à des instances d’élément définies par les mots clés du schéma d’impression. Toutefois, les instances de propriété privées tierces doivent appartenir à un espace de noms qui est clairement associé au tiers qui a créé l’espace de noms.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[Référence du schéma d’impression hérité](print-schema.md)
</dt> <dt>

[Communications d’imprimante bidirectionnelles (Centre de développement matériel)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

 

 
