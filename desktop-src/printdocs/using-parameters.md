---
description: Apprenez à utiliser des paramètres dans un document PrintCapabilities. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 4a596604-8a0d-4971-96f3-643727312cfc
title: Utilisation des paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6417a6d30716cf19d22773c28dbf471e75f967d6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119394"
---
# <a name="using-parameters"></a>Utilisation des paramètres

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En plus de la notation correcte d’une option qui contient des instances ParameterRef (consultez [références de paramètres](referencing-parameters.md)), les fournisseurs et les clients PrintCapabilities ou PrintTicket doivent être préparés pour gérer les situations suivantes impliquant des paramètres.

Les clients de l’interface utilisateur doivent inviter l’utilisateur à fournir des initialiseurs de paramètres (valeurs pour les éléments ParameterInit) pour les paramètres désignés au moment opportun afin que les éléments ParameterInit appropriés soient insérés dans PrintTicket. Les clients de l’interface utilisateur doivent être en mesure de faire la distinction entre les deux types de paramètres, obligatoire de manière inconditionnelle et obligatoire, et doivent pouvoir gérer chaque type de façon appropriée. Pour un paramètre obligatoire de manière inconditionnelle, l’interface utilisateur doit s’assurer qu’un élément ParameterInit est fourni pour ce type de paramètre. Pour un paramètre obligatoire de manière conditionnelle, l’interface utilisateur doit fournir une valeur ParameterInit si le paramètre est référencé par une option sélectionnée dans PrintTicket. L’État obligatoire d’un paramètre est spécifié dans une instance de ParameterDef. Pour plus d’informations, consultez [ParameterDef et ParameterInit Elements](parameterdef-and-parameterinit-elements.md). Les clients de l’interface utilisateur doivent valider les valeurs ParameterInit fournies par l’utilisateur pour vérifier qu’elles répondent aux exigences spécifiées dans l’instance ParameterDef.

Les fournisseurs PrintTicket doivent également vérifier les instances ParameterInit fournies par l’PrintTicket pour vérifier que tous les paramètres nécessaires sont présents et qu’ils répondent aux exigences spécifiées dans l’instance ParameterDef. Le code de validation doit fournir des valeurs par défaut raisonnables dans le cas où les valeurs ParameterInit ne sont pas valides ou sont manquantes. Notez qu’un ParameterDef permet de fournir une valeur par défaut à cet effet. En outre, s’il existe des contraintes impliquant les paramètres, par exemple, « si *CopyCount* est supérieur à N, n’utilisez pas un casier d’entrée de petite capacité », le code de validation PrintTicket doit détecter cette contrainte et modifier l’PrintTicket pour éviter d’activer la contrainte.

S’il existe une dépendance du PrintCapabilities sur les paramètres spécifiés dans le PrintTicket, les fournisseurs PrintCapabilities doivent surveiller les valeurs ParameterInit et produire un document PrintCapabilities approprié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



