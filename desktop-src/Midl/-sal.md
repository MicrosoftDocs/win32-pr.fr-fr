---
title: commutateur/SAL
description: Le commutateur/SAL dirige MIDL pour générer des annotations SAL dans les fichiers stub générés.
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- MIDL du commutateur/SAL
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106509012"
---
# <a name="sal-switch"></a><span data-ttu-id="67801-104">commutateur/SAL</span><span class="sxs-lookup"><span data-stu-id="67801-104">/sal switch</span></span>

<span data-ttu-id="67801-105">Le commutateur **/SAL** dirige MIDL pour générer des annotations SAL dans les fichiers stub générés.</span><span class="sxs-lookup"><span data-stu-id="67801-105">The **/sal** switch directs MIDL to generate SAL annotations in the generated stub files.</span></span>

``` syntax
midl /sal
```

## <a name="switch-options"></a><span data-ttu-id="67801-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="67801-106">Switch Options</span></span>

<span data-ttu-id="67801-107">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="67801-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="67801-108">Notes</span><span class="sxs-lookup"><span data-stu-id="67801-108">Remarks</span></span>

<span data-ttu-id="67801-109">MIDL marquera les paramètres de pointeur et de tableau avec des annotations qui reflètent la description de paramètre dans le fichier IDL, telle qu’elle est appliquée par RPC et le moteur de conversion de NDR.</span><span class="sxs-lookup"><span data-stu-id="67801-109">MIDL will mark pointer and array parameters with annotations that reflect the parameter description in the IDL file as enforced by RPC and the NDR marshaling engine.</span></span> <span data-ttu-id="67801-110">MIDL ne crée pas d’annotations pour les paramètres dans les méthodes d’interface marquées avec l’attribut [**\[ local \]**](local.md), sauf si [**/SAL \_ local**](-sal-local.md) est également présent sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="67801-110">MIDL does not create annotations for parameters in interface methods marked with the [**\[local\]**](local.md)attribute unless [**/sal\_local**](-sal-local.md) is also present on the command line.</span></span> <span data-ttu-id="67801-111">Pour remplacer l’annotation générée par MIDL, utilisez l’attribut [**\[ annoter \]**](annotate.md) .</span><span class="sxs-lookup"><span data-stu-id="67801-111">To override the MIDL-generated annotation, use the [**\[annotate\]**](annotate.md) attribute.</span></span>

<span data-ttu-id="67801-112">Les annotations générées par MIDL ont toujours le préfixe \_ \_ RPC \_ et nécessitent l’utilisation de l’en-tête **rpcsal. h** pour convertir l’annotation en annotations SAL standard.</span><span class="sxs-lookup"><span data-stu-id="67801-112">MIDL-generated annotations are always prefixed with \_\_RPC\_, and require use of the **rpcsal.h** header to translate the annotation into standard SAL annotations.</span></span>

## <a name="see-also"></a><span data-ttu-id="67801-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67801-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67801-114">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="67801-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="67801-115">**/SAL \_ local**</span><span class="sxs-lookup"><span data-stu-id="67801-115">**/sal\_local**</span></span>](-sal-local.md)
</dt> <dt>

<span data-ttu-id="67801-116">[**\[annoter\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="67801-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




