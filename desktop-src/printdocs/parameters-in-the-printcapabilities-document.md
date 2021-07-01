---
description: Comprendre les paramètres dans le document PrintCapabilities. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Paramètres dans le document PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6b2ba61f1985fdcd02f40e8e08100725968a8e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118624"
---
# <a name="parameters-in-the-printcapabilities-document"></a>Paramètres dans le document PrintCapabilities

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Comme indiqué dans [éléments de référence de paramètre](parameter-reference-elements.md), les éléments ParameterInit peuvent être référencés à partir d’instances d’option, mais la construction de paramètre a également une utilisation indépendante de ce type d’élément.

CopyCount est un exemple d’attribut de configuration d’appareil adapté à la représentation des paramètres. Les valeurs autorisées pour cet attribut de configuration de périphérique peuvent être définies facilement et de façon concise sans répertorier chacune d’elles de manière explicite. Bien qu’il soit possible, bien que fastidieux, de répertorier chaque valeur CopyCount dans sa propre option, certains attributs de configuration de l’appareil ne peuvent pas être représentés à l’aide d’une construction fonctionnalité/option. Par exemple, imaginez un appareil qui accepte une chaîne de texte qui est ensuite utilisée pour produire un filigrane virtuel sur chaque page de sortie. L’ensemble de toutes les chaînes de texte possibles ne peut pas être facilement énuméré, mais la chaîne de texte peut facilement être décrite à l’aide d’un élément ParameterDef.

Le document des mots clés du schéma d’impression définit un certain nombre de constructions de paramètres couramment utilisées, mais les fournisseurs PrintCapabilities sont libres de définir des éléments supplémentaires. Toutefois, ces constructions de paramètres définies de manière privée ne sont pas portables vers d’autres appareils, en raison du fait qu’un document PrintCapabilities fourni par une autre partie ne définit pas une telle construction de paramètre. Que la définition d’un schéma ou d’une définition privée soit définie, l’instance ParameterDef doit être présente dans le document PrintCapabilities avant que le paramètre soit reconnu et utilisé par les clients. Ces paramètres sont appelés *paramètres désignés*.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



