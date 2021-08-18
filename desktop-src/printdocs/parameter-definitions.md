---
description: En savoir plus sur les définitions de paramètres dans un document PrintCapabilities. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Définitions de paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dad2f596592efddfafe97b32660d92bb67b6097012fe9599f89ce0e63526f72e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034057"
---
# <a name="parameter-definitions"></a>Définitions de paramètres

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Cette section décrit les définitions de paramètres publics qui peuvent apparaître dans un document PrintCapabilities.

Les paramètres sont utilisés pour décrire une plage acceptable de valeurs, plutôt qu’une énumération discrète de valeurs.

## <a name="parameterdef"></a>ParameterDef

Pour obtenir un résumé du type d’élément ParameterDef, reportez-vous à la section [ParameterDef](parameterdef.md) .

Pour plus d’informations sur l’interaction entre les éléments ParameterDef et les éléments ParameterInit, reportez-vous à la section [éléments ParameterDef et ParameterInit](./parameterdef-and-parameterinit-elements.md) .

Les éléments ParameterDef définis dans les mots clés du schéma d’impression doivent être entièrement définis dans un document PrintCapabilities.

## <a name="parameterref"></a>ParameterRef

Pour obtenir un résumé du type d’élément ParameterRef, reportez-vous à la section [ParameterRef](parameterref.md) .

Un mot clé d’élément configurable par l’utilisateur peut contenir une référence à un paramètre. Les éléments ParameterRef sont spécifiés en tant qu’enfants d’un élément ScoredProperty. pour plus d’informations, consultez la section [éléments de référence de paramètre](parameter-reference-elements.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
