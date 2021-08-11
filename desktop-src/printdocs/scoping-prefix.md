---
description: Un préfixe d’étendue est une étiquette textuelle pré-ajoutée à un mot clé de schéma pour fournir une étendue contextuelle, y compris le travail, le document et la page.
ms.assetid: 4bad85d7-a933-43fe-9d79-4835d92c82d6
title: Préfixe d’étendue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ad23369d2b2c60c00752e4f5be31f6ad605e2814d0b7502d42ff79baa10977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234092"
---
# <a name="scoping-prefix"></a>Préfixe d’étendue

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un préfixe d’étendue est une étiquette textuelle pré-ajoutée à un mot clé de schéma pour fournir une étendue contextuelle. Cela permet à ascribing un contexte spécifique et bien compris aux mots clés d’une manière prédéfinie. La fonctionnalité de schéma d’impression, ParameterDef, ParameterInit et ParameterRef et les éléments de mot clé de propriété de niveau racine doivent avoir l’un des préfixes de portée suivants : « job », « document » ou « page ».

## <a name="interpretation-of-the-scoping-prefix-with-printticket-content"></a>Interprétation du préfixe d’étendue avec le contenu PrintTicket

Le PrintTicket peut être divisé en trois niveaux de contenu représentant le travail de haut niveau, les documents du travail et les pages de chaque document. Ces niveaux sont classés en fonction de leur spécificité. le niveau du travail est le plus général, puis le niveau du document, puis le niveau de la page est plus spécifique. Un travail se compose d’un ou de plusieurs documents et un document se compose d’une ou de plusieurs pages.

## <a name="job-level-prefix"></a>Préfixe au niveau du travail

Un ticket au niveau du travail contient tous les paramètres de mise en forme du travail destinés à s’appliquer à un travail entier. Tous les éléments avec des préfixes de portée « Job », « document » ou « page » sont autorisés dans un ticket au niveau du travail.

Les paramètres préfixes « document » et « page » spécifiés dans un ticket au niveau du travail sont automatiquement appliqués aux tickets de document et de niveau page.

## <a name="document-level-prefix"></a>Préfixe au niveau du document

Le ticket au niveau du document intègre tous les paramètres de mise en forme des tâches destinés à s’appliquer à un ou plusieurs documents d’un travail. Celles-ci peuvent inclure des paramètres précédemment spécifiés dans le ticket au niveau du travail. Seuls les éléments avec des préfixes de portée « document » ou « page » sont autorisés dans un ticket au niveau du document.

Un ticket au niveau du document peut contenir des paramètres prédéfinis de document précédemment spécifiés par le ticket au niveau du travail.

## <a name="page-level-prefix"></a>Préfixe au niveau de la page

Le ticket au niveau de la page intègre tous les paramètres de mise en forme du travail destinés à s’appliquer à une ou plusieurs pages d’un travail (pas limité à un seul document). Celles-ci peuvent inclure des paramètres précédemment spécifiés dans le travail ou le ticket au niveau du document. Seuls les éléments avec des préfixes d’étendue de « page » sont autorisés dans un ticket au niveau de la page.

Un ticket au niveau de la page peut contenir des paramètres de préfixe « page » précédemment spécifiés par le ticket au niveau du travail et/ou le ticket au niveau du document.

## <a name="prefix-usage-within-a-printticket-or-print-capabilities-document"></a>Utilisation d’un préfixe dans un document PrintTicket ou des fonctionnalités d’impression

Les documents PrintTicket et PrintCapabilities ne doivent pas contenir plusieurs mots clés qui diffèrent uniquement par le préfixe d’étendue. Par exemple, un document PrintCapabilities ne doit pas avoir à la fois JobInputBin et PageInputBin spécifiés. Toutefois, un document de fonctionnalités d’impression peut avoir à la fois JobDuplexAllDocumentsContiguously et DocumentDuplex spécifiés, car ils sont considérés comme des fonctionnalités différentes, car ils présentent un comportement différent. Cet exemple est également vrai pour un seul PrintTicket.

## <a name="prefix-conflict-management"></a>Préfixer la gestion des conflits

Un conflit de mots clés entre les paramètres est défini en tant que, le même élément de schéma d’impression de niveau racine, indiqué par l’attribut XML « Name », apparaissant dans plusieurs tickets de niveau. En l’absence de conflit, un élément délimité par un préfixe peut être déplacé vers le niveau supérieur, ou hérité, d’un ticket plus général à un ticket plus spécifique. En cas de conflit, le paramètre du ticket le plus spécifique est prioritaire. Autrement dit, les paramètres de page d’un ticket au niveau de la page remplacent les mêmes paramètres par page dans un document ou un ticket au niveau du travail. De même, les paramètres du document dans le ticket au niveau du document sont prioritaires par rapport aux paramètres du document dans le ticket au niveau du travail.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



