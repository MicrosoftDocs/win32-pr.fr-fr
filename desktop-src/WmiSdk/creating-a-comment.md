---
description: Le compilateur format MOF (MOF) prend en charge deux styles de commentaires à l’aide de deux styles différents de délimiteurs de commentaire.
ms.assetid: 5ab71b45-7ed1-44c4-8710-6b833b0afb80
ms.tgt_platform: multiple
title: Création d’un commentaire
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2d0e7cf2484fef018c62c8c47d9c55d245191681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524150"
---
# <a name="creating-a-comment"></a><span data-ttu-id="74f4f-103">Création d’un commentaire</span><span class="sxs-lookup"><span data-stu-id="74f4f-103">Creating a Comment</span></span>

<span data-ttu-id="74f4f-104">Le compilateur format MOF (MOF) prend en charge deux styles de commentaires à l’aide de deux styles différents de délimiteurs de commentaire.</span><span class="sxs-lookup"><span data-stu-id="74f4f-104">The Managed Object Format (MOF) compiler supports two styles of comment using two different styles of comment delimiters.</span></span>

<span data-ttu-id="74f4f-105">Le tableau suivant répertorie les délimiteurs utilisés pour les commentaires et l’effet que les délimiteurs ont dans le code.</span><span class="sxs-lookup"><span data-stu-id="74f4f-105">The following table lists the delimiters that are used for comments and the effect that the delimiters have in the code.</span></span>



| <span data-ttu-id="74f4f-106">Délimiteur</span><span class="sxs-lookup"><span data-stu-id="74f4f-106">Delimiter</span></span>   | <span data-ttu-id="74f4f-107">Marques</span><span class="sxs-lookup"><span data-stu-id="74f4f-107">Marks</span></span>                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | <span data-ttu-id="74f4f-108">Début d’un commentaire qui se termine à la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="74f4f-108">Start of a comment that terminates at the end of the line.</span></span>                                    |
| <span data-ttu-id="74f4f-109">/\* les \*/</span><span class="sxs-lookup"><span data-stu-id="74f4f-109">/\* and \*/</span></span> | <span data-ttu-id="74f4f-110">Début et fin d’un commentaire qui peut s’étendre sur plusieurs lignes ou s’étendre uniquement sur une partie d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="74f4f-110">Beginning and end of a comment that may span multiple lines or only span a portion of a line.</span></span> |



 

<span data-ttu-id="74f4f-111">Comme dans les langages de programmation C et C++, vous devez utiliser le délimiteur//avec des commentaires sur une seule ligne, mais vous pouvez utiliser les \* \* délimiteurs/et/avec des commentaires sur une ou plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="74f4f-111">As in the C and C++ programming languages, you must use the // delimiter with single-line comments only, but use the /\* and \*/ delimiters with either single-line or multiple-line comments.</span></span>

<span data-ttu-id="74f4f-112">L’exemple de code suivant décrit les deux styles de délimiteur.</span><span class="sxs-lookup"><span data-stu-id="74f4f-112">The following code example describes the two delimiter styles.</span></span>

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a><span data-ttu-id="74f4f-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="74f4f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74f4f-114">Conception de classes format MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="74f4f-114">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



