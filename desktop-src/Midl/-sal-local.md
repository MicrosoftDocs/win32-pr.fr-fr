---
title: commutateur/sal_local
description: Le \_ commutateur local/SAL dirige MIDL pour générer également des annotations SAL pour les paramètres des méthodes d’interface marquées \ local \. Le commutateur/SAL doit également être présent.
ms.assetid: 49AFC3F6-EAD5-45F6-8862-EFB3D9C479D1
keywords:
- /commutateur sal_local MIDL
topic_type:
- apiref
api_name:
- /sal_local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03263b94b809407d1c3e55c2f3dacc5e10684bc1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106510650"
---
# <a name="sal_local-switch"></a><span data-ttu-id="bd737-105">\_commutateur local/SAL</span><span class="sxs-lookup"><span data-stu-id="bd737-105">/sal\_local switch</span></span>

<span data-ttu-id="bd737-106">Le **commutateur \_ local/SAL** dirige MIDL pour générer également des annotations SAL pour les paramètres de méthodes d’interface marquées comme [**\[ locales \]**](local.md).</span><span class="sxs-lookup"><span data-stu-id="bd737-106">The **/sal\_local** switch directs MIDL to also generate SAL annotations for parameters of interface methods marked [**\[local\]**](local.md).</span></span> <span data-ttu-id="bd737-107">Le commutateur [**/SAL**](-sal.md) doit également être présent.</span><span class="sxs-lookup"><span data-stu-id="bd737-107">The [**/sal**](-sal.md) switch must also be present.</span></span>

``` syntax
midl /sal /sal_local
```

## <a name="switch-options"></a><span data-ttu-id="bd737-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="bd737-108">Switch Options</span></span>

<span data-ttu-id="bd737-109">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bd737-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd737-110">Notes</span><span class="sxs-lookup"><span data-stu-id="bd737-110">Remarks</span></span>

<span data-ttu-id="bd737-111">Modifie le comportement du commutateur [**/SAL**](-sal.md) pour fournir également des annotations sur les paramètres des méthodes d’interface marquées avec l’attribut [**\[ local \]**](local.md) .</span><span class="sxs-lookup"><span data-stu-id="bd737-111">Modifies the behavior of the [**/sal**](-sal.md) switch to also provide annotations on the parameters of interface methods marked with the [**\[local\]**](local.md) attribute.</span></span> <span data-ttu-id="bd737-112">Utilisez l’attribut [**\[ annoter \]**](annotate.md)pour remplacer l’annotation générée par MIDL par une autre chaîne d’annotation.</span><span class="sxs-lookup"><span data-stu-id="bd737-112">Use the [**\[annotate\]**](annotate.md)attribute to override the MIDL-generated annotation with a different annotation string.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd737-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd737-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd737-114">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="bd737-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="bd737-115">**/sal**</span><span class="sxs-lookup"><span data-stu-id="bd737-115">**/sal**</span></span>](-sal.md)
</dt> <dt>

<span data-ttu-id="bd737-116">[**\[annoter\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="bd737-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




