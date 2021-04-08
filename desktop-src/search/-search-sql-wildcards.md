---
description: Le prédicat CONTAINs prend en charge l’utilisation de l’astérisque ( \* ) comme caractère générique pour représenter des mots et des expressions. Vous pouvez ajouter l’astérisque uniquement à la fin du mot ou de l’expression. La présence de l’astérisque active le mode de correspondance de préfixe.
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: Utilisation de caractères génériques dans le prédicat CONTAINs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013e49f97cf23c7a00aca7bb287edd19951520f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112410"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a><span data-ttu-id="89ad8-105">Utilisation de caractères génériques dans le prédicat CONTAINs</span><span class="sxs-lookup"><span data-stu-id="89ad8-105">Using Wildcard Characters in the CONTAINS Predicate</span></span>

<span data-ttu-id="89ad8-106">Le prédicat CONTAINs prend en charge l’utilisation de l’astérisque ( \* ) comme caractère générique pour représenter des mots et des expressions.</span><span class="sxs-lookup"><span data-stu-id="89ad8-106">The CONTAINS predicate supports the use of the asterisk (\*) as a wildcard character to represent words and phrases.</span></span> <span data-ttu-id="89ad8-107">Vous pouvez ajouter l’astérisque uniquement à la fin du mot ou de l’expression.</span><span class="sxs-lookup"><span data-stu-id="89ad8-107">You can add the asterisk only at the end of the word or phrase.</span></span> <span data-ttu-id="89ad8-108">La présence de l’astérisque active le mode de correspondance de préfixe.</span><span class="sxs-lookup"><span data-stu-id="89ad8-108">The presence of the asterisk enables the prefix-matching mode.</span></span> <span data-ttu-id="89ad8-109">Dans ce mode, les correspondances sont retournées si la colonne contient le mot de recherche spécifié, suivi de zéro, un ou plusieurs autres caractères.</span><span class="sxs-lookup"><span data-stu-id="89ad8-109">In this mode, matches are returned if the column contains the specified search word followed by zero or more other characters.</span></span> <span data-ttu-id="89ad8-110">Si une expression est fournie, les correspondances sont détectées si la colonne contient tous les mots spécifiés avec zéro, un ou plusieurs autres caractères après le mot final.</span><span class="sxs-lookup"><span data-stu-id="89ad8-110">If a phrase is provided, matches are detected if the column contains all the specified words with zero or more other characters following the final word.</span></span>

## <a name="examples"></a><span data-ttu-id="89ad8-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="89ad8-111">Examples</span></span>

<span data-ttu-id="89ad8-112">Le premier exemple correspond à des documents dont la colonne de nom de fichier contient des mots commençant par « serv ».</span><span class="sxs-lookup"><span data-stu-id="89ad8-112">The first example matches documents that have any word in the FileName column beginning with "serv".</span></span> <span data-ttu-id="89ad8-113">Exemples de mots correspondants : « Server », « Servers » et « service ».</span><span class="sxs-lookup"><span data-stu-id="89ad8-113">Example matching words include "server", "servers", and "service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



<span data-ttu-id="89ad8-114">Le deuxième exemple correspond à des documents avec une expression dans la colonne nom de fichier qui commence par « COMP » et dans laquelle le mot suivant commence par « serv ».</span><span class="sxs-lookup"><span data-stu-id="89ad8-114">The second example matches documents with any phrase in the FileName column that begins with "comp" and in which the next word begins with "serv".</span></span> <span data-ttu-id="89ad8-115">Exemples de mots correspondants : « COMP Server », « COMP Servers » et « COMP service ».</span><span class="sxs-lookup"><span data-stu-id="89ad8-115">Example matching words include "comp server", "comp servers", and "comp service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



<span data-ttu-id="89ad8-116">L’astérisque ne fonctionne que pour la correspondance de préfixe et ne peut être placé qu’à la fin du mot ou de l’expression. il ne fonctionne pas pour la correspondance des suffixes.</span><span class="sxs-lookup"><span data-stu-id="89ad8-116">The asterisk works only for prefix-matching and can be placed only at the end of the word or phrase; it does not work for suffix-matching.</span></span> <span data-ttu-id="89ad8-117">La syntaxe suivante n’est pas valide et ne correspond pas aux documents avec un mot de la colonne de nom de fichier se terminant par « servi ».</span><span class="sxs-lookup"><span data-stu-id="89ad8-117">The following syntax is not valid and does not match documents with any word in the FileName column ending with "serve".</span></span>


```
WHERE CONTAINS(System.FileName, '"*serve"')
```



## <a name="related-topics"></a><span data-ttu-id="89ad8-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89ad8-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="89ad8-119">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="89ad8-119">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="89ad8-120">Prédicat FREETEXT</span><span class="sxs-lookup"><span data-stu-id="89ad8-120">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="89ad8-121">Clause WHERE</span><span class="sxs-lookup"><span data-stu-id="89ad8-121">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



