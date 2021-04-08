---
description: La langue par défaut d’un module de fusion correspond à la langue répertoriée dans la table ModuleSignature du module avant l’application des transformations de langue. Il s’agit également de la première langue qui est indiquée dans la propriété Résumé du modèle.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Choix de la langue par défaut d’un module de fusion à plusieurs langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758a3b47b7a41777652a11a1cdc1b7f380055cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864417"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a><span data-ttu-id="9004f-104">Choix de la langue par défaut d’un module de fusion à plusieurs langues</span><span class="sxs-lookup"><span data-stu-id="9004f-104">Choosing the Default Language of a Multiple Language Merge Module</span></span>

<span data-ttu-id="9004f-105">La langue par défaut d’un module de fusion correspond à la langue répertoriée dans la [table ModuleSignature](modulesignature-table.md) du module avant l’application des transformations de langue.</span><span class="sxs-lookup"><span data-stu-id="9004f-105">The default language for a merge module is the language that is listed in the [ModuleSignature Table](modulesignature-table.md) of the module before language transforms are applied.</span></span> <span data-ttu-id="9004f-106">Il s’agit également de la première langue qui est indiquée dans la propriété [**Résumé du modèle**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="9004f-106">This is also the first language that is listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="9004f-107">La langue par défaut pour le module doit être l’un des langages les plus spécifiques que vous prenez en charge, car la langue par défaut est toujours vérifiée en premier et, si elle est conforme à la langue demandée, elle est utilisée même si une autre langue est une meilleure correspondance.</span><span class="sxs-lookup"><span data-stu-id="9004f-107">The default language for the module should be one of the most specific languages that you support, because the default language is always checked first, and if it satisfies the requested language, it is used even if another language is a better match.</span></span> <span data-ttu-id="9004f-108">Par exemple, si un module prend en charge 1033 et 0, 1033 doit être la langue par défaut.</span><span class="sxs-lookup"><span data-stu-id="9004f-108">For example, if a module supports 1033 and 0, 1033 should be the default language.</span></span> <span data-ttu-id="9004f-109">Si 0 était la langue par défaut, elle répondrait toujours à toute demande, et la transformation 1033 ne serait jamais utilisée, même si 1033 correspond exactement à la langue demandée.</span><span class="sxs-lookup"><span data-stu-id="9004f-109">If 0 were the default language, it would always satisfy any request, and the 1033 transform would never be used, even if 1033 is the exact language requested.</span></span>

 

 



