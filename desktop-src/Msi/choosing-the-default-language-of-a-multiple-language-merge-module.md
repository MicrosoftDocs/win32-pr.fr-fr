---
description: La langue par défaut d’un module de fusion correspond à la langue répertoriée dans la table ModuleSignature du module avant l’application des transformations de langue. Il s’agit également de la première langue qui est indiquée dans la propriété Résumé du modèle.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Choix de la langue par défaut d’un module de fusion à plusieurs langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c174a3917538b1562626819f8ba2bf07864c9169c27e717a078cca8d64992ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145655"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a>Choix de la langue par défaut d’un module de fusion à plusieurs langues

La langue par défaut d’un module de fusion correspond à la langue répertoriée dans la [table ModuleSignature](modulesignature-table.md) du module avant l’application des transformations de langue. Il s’agit également de la première langue qui est indiquée dans la propriété [**Résumé du modèle**](template-summary.md) .

La langue par défaut pour le module doit être l’un des langages les plus spécifiques que vous prenez en charge, car la langue par défaut est toujours vérifiée en premier et, si elle est conforme à la langue demandée, elle est utilisée même si une autre langue est une meilleure correspondance. Par exemple, si un module prend en charge 1033 et 0, 1033 doit être la langue par défaut. Si 0 était la langue par défaut, elle répondrait toujours à toute demande, et la transformation 1033 ne serait jamais utilisée, même si 1033 correspond exactement à la langue demandée.

 

 



