---
title: commutateur/syntax_check
description: Le \_ commutateur de vérification/Syntax indique que le compilateur vérifie uniquement la syntaxe et ne génère pas de fichiers de sortie.
ms.assetid: 8d9139d3-6018-48a7-bea5-0c843b6273d3
keywords:
- /commutateur syntax_check MIDL
topic_type:
- apiref
api_name:
- /syntax_check
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b064a096b5064e6996ea4288c9ae9d4a798c2e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678518"
---
# <a name="syntax_check-switch"></a><span data-ttu-id="81280-104">commutateur de vérification de/Syntax \_</span><span class="sxs-lookup"><span data-stu-id="81280-104">/syntax\_check switch</span></span>

<span data-ttu-id="81280-105">Le commutateur de **\_ vérification/Syntax** indique que le compilateur vérifie uniquement la syntaxe et ne génère pas de fichiers de sortie.</span><span class="sxs-lookup"><span data-stu-id="81280-105">The **/syntax\_check** switch indicates that the compiler checks only syntax and does not generate output files.</span></span>

``` syntax
midl /syntax_check
midl /Zs
```

## <a name="switch-options"></a><span data-ttu-id="81280-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="81280-106">Switch Options</span></span>

<span data-ttu-id="81280-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="81280-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="81280-108">Notes</span><span class="sxs-lookup"><span data-stu-id="81280-108">Remarks</span></span>

<span data-ttu-id="81280-109">Ce commutateur remplace tous les autres commutateurs qui spécifient des informations sur les fichiers de sortie.</span><span class="sxs-lookup"><span data-stu-id="81280-109">This switch overrides all other switches that specify information about output files.</span></span>

<span data-ttu-id="81280-110">Vous pouvez également spécifier le mode de vérification de syntaxe avec l’option de compilateur MIDL [**/ZS**](-zs.md).</span><span class="sxs-lookup"><span data-stu-id="81280-110">You can also specify syntax-checking mode with the MIDL compiler option [**/Zs**](-zs.md).</span></span>

## <a name="examples"></a><span data-ttu-id="81280-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="81280-111">Examples</span></span>

<span data-ttu-id="81280-112">**MIDL/ZS NomFichier. idl**</span><span class="sxs-lookup"><span data-stu-id="81280-112">**midl /Zs filename.idl**</span></span>

<span data-ttu-id="81280-113">**/Syntax MIDL \_ vérifier filename. idl**</span><span class="sxs-lookup"><span data-stu-id="81280-113">**midl /syntax\_check filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="81280-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81280-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81280-115">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="81280-115">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="81280-116">**/ZS**</span><span class="sxs-lookup"><span data-stu-id="81280-116">**/Zs**</span></span>](-zs.md)
</dt> </dl>

 

 




