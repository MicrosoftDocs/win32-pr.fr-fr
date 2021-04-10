---
title: Commutateur/ZS
description: Le commutateur/ZS indique que le compilateur vérifie la syntaxe uniquement et ne génère pas de fichiers de sortie.
ms.assetid: 5ff44607-12c3-4a2d-8a7f-2056504990e2
keywords:
- MIDL du commutateur/ZS
topic_type:
- apiref
api_name:
- /Zs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 469802434d54319aa55c1e409ccb8d64e942836f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678309"
---
# <a name="zs-switch"></a><span data-ttu-id="0e0ba-104">Commutateur/ZS</span><span class="sxs-lookup"><span data-stu-id="0e0ba-104">/Zs switch</span></span>

<span data-ttu-id="0e0ba-105">Le commutateur **/ZS** indique que le compilateur vérifie la syntaxe uniquement et ne génère pas de fichiers de sortie.</span><span class="sxs-lookup"><span data-stu-id="0e0ba-105">The **/Zs** switch indicates that the compiler only checks syntax and does not generate output files.</span></span>

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a><span data-ttu-id="0e0ba-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="0e0ba-106">Switch Options</span></span>

<span data-ttu-id="0e0ba-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0e0ba-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e0ba-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0e0ba-108">Remarks</span></span>

<span data-ttu-id="0e0ba-109">Ce commutateur remplace tous les autres commutateurs qui spécifient des informations sur les fichiers de sortie.</span><span class="sxs-lookup"><span data-stu-id="0e0ba-109">This switch overrides all other switches that specify information about output files.</span></span>

<span data-ttu-id="0e0ba-110">Vous pouvez également spécifier le mode de vérification de syntaxe avec le commutateur de compilateur MIDL [**/Syntax \_ Check**](-syntax-check.md).</span><span class="sxs-lookup"><span data-stu-id="0e0ba-110">You can also specify syntax-checking mode with the MIDL compiler switch [**/syntax\_check**](-syntax-check.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0e0ba-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="0e0ba-111">Examples</span></span>

<span data-ttu-id="0e0ba-112">**MIDL/ZS NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="0e0ba-112">**midl /Zs filename.idl**</span></span>

<span data-ttu-id="0e0ba-113">**/Syntax MIDL \_ vérifier filename. idl**</span><span class="sxs-lookup"><span data-stu-id="0e0ba-113">**midl /syntax\_check filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="0e0ba-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e0ba-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e0ba-115">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="0e0ba-115">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="0e0ba-116">**vérification de/Syntax \_**</span><span class="sxs-lookup"><span data-stu-id="0e0ba-116">**/syntax\_check**</span></span>](-syntax-check.md)
</dt> </dl>

 

 




