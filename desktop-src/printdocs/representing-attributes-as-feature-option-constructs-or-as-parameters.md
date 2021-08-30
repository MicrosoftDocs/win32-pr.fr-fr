---
description: Représentent des attributs en tant que constructions feature/option ou en tant que paramètres. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Représentation des attributs en tant que constructions feature/option ou en tant que paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a1d1923eb019ae1985b2000896389fa9c945b25430eda77e59e9c673d8ba9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091689"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a>Représentation des attributs en tant que constructions feature/option ou en tant que paramètres

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

L’auteur d’un document PrintCapabilities définit les attributs de l’appareil qui composent la configuration. Dans le document PrintCapabilities, l’auteur peut choisir de représenter un attribut d’appareil en tant que construction fonctionnalité/option ou en tant que construction de paramètre.

Si un attribut d’appareil a un nombre relativement faible d’États possibles qui ne sont pas classés dans un modèle évident, une construction fonctionnalité/option est généralement le meilleur choix. Par exemple, si les valeurs autorisées pour l’attribut d’appareil PageMediaSize sont les valeurs letter, Legal, A4ISO, tabloïd et Envelope10, une fonctionnalité/option est le meilleur choix pour la représentation. En raison de la difficulté et de l’ambiguïté associées à l’expression des valeurs autorisées sans énumération explicite, la construction de paramètre n’est pas appropriée pour l’attribut PageMediaSize.

Si un attribut d’appareil peut être représenté par une plage d’entiers, la représentation des paramètres est généralement le meilleur choix, en particulier pour les plages qui incluent de nombreuses valeurs. Par exemple, si l’attribut d’appareil CopyCount pour un modèle d’imprimante donné peut être compris entre 1 et 99 999, cet attribut doit être catégorisé comme paramètre, en définissant une instance ParameterDef. Assignez des valeurs aux instances de propriété standard MinValue et MaxValue de l’élément ParameterDef pour définir la plage de valeurs de l’attribut JobCopyCount. En raison du grand nombre de valeurs qui doivent être explicitement listées en tant qu’éléments option, la représentation fonctionnalité/option n’est pas appropriée pour l’attribut d’appareil JobCopyCount.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



