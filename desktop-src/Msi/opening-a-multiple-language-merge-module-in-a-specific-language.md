---
description: Lors de la fusion d’un module dans une base de données d’installation, il existe deux langues importantes.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Ouverture d’un module de fusion Multiple-Language dans un langage spécifique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b552c41d7696b29a86987d027e00ef4cb19bbb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034120"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a><span data-ttu-id="c4986-103">Ouverture d’un module de fusion Multiple-Language dans un langage spécifique</span><span class="sxs-lookup"><span data-stu-id="c4986-103">Opening a Multiple-Language Merge Module in a Specific Language</span></span>

<span data-ttu-id="c4986-104">Lors de la fusion d’un module dans une base de données d’installation, il existe deux langues importantes.</span><span class="sxs-lookup"><span data-stu-id="c4986-104">When merging a module into an installation database, there are two important languages.</span></span> <span data-ttu-id="c4986-105">La première est la langue du package d’installation cible spécifié par [**ProductLanguage**](productlanguage.md) dans la [table des propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="c4986-105">The first is the language of the target installation package specified by [**ProductLanguage**](productlanguage.md) in the [Property Table](property-table.md).</span></span> <span data-ttu-id="c4986-106">La seconde est la langue du module de fusion qui apparaît dans la colonne Language de la [table ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="c4986-106">The second is the language of the merge module that appears in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="c4986-107">La langue du package d’installation peut être transmise au module par l’outil de fusion lorsque le package est ouvert pour une fusion.</span><span class="sxs-lookup"><span data-stu-id="c4986-107">The language of the installation package can be passed to the module by the merge tool when the package is opened for a merge.</span></span> <span data-ttu-id="c4986-108">Toutefois, il peut parfois être nécessaire d’ignorer la langue de la cible et de demander que le module soit ouvert dans un autre langage, par exemple, un package en anglais qui installe les ressources en anglais et en allemand à partir du module.</span><span class="sxs-lookup"><span data-stu-id="c4986-108">However, sometimes it may be necessary to disregard the language of the target, and request that the module be opened in another language, for example, an English package installing both the English and German resources from the module.</span></span>

<span data-ttu-id="c4986-109">Lors de l’ouverture d’un module à l’aide d’une requête de langue, l’outil de fusion vérifie la langue demandée par rapport aux langues spécifiées dans la colonne Language de la [table ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="c4986-109">When opening a module with a language request, the merge tool checks the requested language against the languages that are specified in the Language column of the [ModuleSignature Table](modulesignature-table.md).</span></span>

<span data-ttu-id="c4986-110">Le processus suivant est utilisé pour déterminer la langue à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c4986-110">The following process is used to determine which language to use.</span></span>

<span data-ttu-id="c4986-111">**Pour déterminer la langue à utiliser**</span><span class="sxs-lookup"><span data-stu-id="c4986-111">**To determine which language to use**</span></span>

1.  <span data-ttu-id="c4986-112">Si la langue de la [table ModuleSignature](modulesignature-table.md) est égale ou plus générale que la langue demandée, le module s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="c4986-112">If the language in the [ModuleSignature Table](modulesignature-table.md) is equal or more general than the requested language, the module opens.</span></span>
2.  <span data-ttu-id="c4986-113">Si le module prend en charge la langue exacte demandée, cette langue est utilisée.</span><span class="sxs-lookup"><span data-stu-id="c4986-113">If the module supports the exact language requested, that language is used.</span></span>
3.  <span data-ttu-id="c4986-114">Si le module prend en charge le groupe de langues de la langue demandée par le groupe de langues, par exemple, cochez 9 si 1033 a été demandé, mais introuvable à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="c4986-114">If the module supports the language group of the language requested that language group is used, for example, check 9 if 1033 was requested but not found in step 2.</span></span>
4.  <span data-ttu-id="c4986-115">Vérifiez s’il existe une transformation de langue qui modifie le module en neutre.</span><span class="sxs-lookup"><span data-stu-id="c4986-115">Check if there is a language transform that changes the module to neutral.</span></span>
5.  <span data-ttu-id="c4986-116">Si aucune des étapes précédentes ne réussit, le module ne prend pas en charge la langue demandée et la fusion échoue.</span><span class="sxs-lookup"><span data-stu-id="c4986-116">If none of the previous steps succeed, the module does not support the requested language and the merge fails.</span></span>

 

 



