---
description: Vous pouvez spécifier la langue utilisée dans les requêtes de recherche.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Spécification des langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50b3f65a41670989d41e235831ec8c008a6d8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525479"
---
# <a name="specifying-languages"></a><span data-ttu-id="7171c-103">Spécification des langues</span><span class="sxs-lookup"><span data-stu-id="7171c-103">Specifying Languages</span></span>

<span data-ttu-id="7171c-104">Vous pouvez spécifier la langue utilisée dans les requêtes de recherche.</span><span class="sxs-lookup"><span data-stu-id="7171c-104">You can specify the language used in search queries.</span></span> <span data-ttu-id="7171c-105">Les prédicats FREETEXT et CONTAINs de la clause WHERE prennent en charge la spécification d’une langue.</span><span class="sxs-lookup"><span data-stu-id="7171c-105">Both the FREETEXT and CONTAINS predicates in the WHERE clause support specifying a language.</span></span> <span data-ttu-id="7171c-106">Vous pouvez indiquer le langage de requête en fournissant un identificateur de code de langue numérique (LCID) dans le prédicat CONTAINs ou FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="7171c-106">You can indicate the query language by providing a numeric language code identifier (LCID) in the CONTAINS or FREETEXT predicate.</span></span> <span data-ttu-id="7171c-107">Ce LCID spécifie l’analyseur lexical à utiliser pour analyser la chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="7171c-107">This LCID specifies which word breaker to use to parse the query string.</span></span> <span data-ttu-id="7171c-108">Il utilise la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="7171c-108">It uses the following syntax:</span></span>


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



<span data-ttu-id="7171c-109">Pour plus d’informations, consultez la syntaxe des prédicats [Contains](-search-sql-contains.md) et [FREETEXT](-search-sql-freetext.md) .</span><span class="sxs-lookup"><span data-stu-id="7171c-109">For more information, see the syntax for the [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) predicates.</span></span>

 

 



