---
title: commutateur/ms_union
description: Le \_ commutateur/ms. Union contrôle l’alignement du rapport de non-remise des unions non encapsulées. Notez que cet attribut est fourni à des fins de compatibilité descendante.
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /commutateur ms_union MIDL
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968618af5c2bb5b32ec14b293225bc09c2997aa5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841433"
---
# <a name="ms_union-switch"></a><span data-ttu-id="5fbd5-104">\_commutateur/ms. Union</span><span class="sxs-lookup"><span data-stu-id="5fbd5-104">/ms\_union switch</span></span>

<span data-ttu-id="5fbd5-105">Le commutateur **/ms. \_ Union** contrôle l’alignement du rapport de non-remise des unions non encapsulées.</span><span class="sxs-lookup"><span data-stu-id="5fbd5-105">The **/ms\_union** switch controls the NDR alignment of nonencapsulated unions.</span></span>

> [!Note]  
> <span data-ttu-id="5fbd5-106">Cet attribut est fourni à des fins de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="5fbd5-106">This attribute is provided for backwards compatibility.</span></span> <span data-ttu-id="5fbd5-107">Il n’est pas recommandé de l’utiliser dans une nouvelle interface.</span><span class="sxs-lookup"><span data-stu-id="5fbd5-107">It is not recommended for use in a new interface.</span></span>

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a><span data-ttu-id="5fbd5-108">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="5fbd5-108">Switch Options</span></span>

<span data-ttu-id="5fbd5-109">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5fbd5-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fbd5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5fbd5-110">Remarks</span></span>

<span data-ttu-id="5fbd5-111">Le compilateur MIDL reflète le comportement du compilateur IDL OSF-DCE pour les unions non encapsulées.</span><span class="sxs-lookup"><span data-stu-id="5fbd5-111">The MIDL compiler mirrors the behavior of the OSF-DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="5fbd5-112">Toutefois, étant donné que les versions antérieures du compilateur MIDL ne l’ont pas fait, le commutateur d' **\_ Union/ms.** fournit la compatibilité avec les interfaces générées sur les versions précédentes du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="5fbd5-112">However, because earlier versions of the MIDL compiler did not do so, the **/ms\_union** switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="5fbd5-113">La \_ fonctionnalité MS Union peut être utilisée en tant que commutateur de ligne de commande (**/ms. \_ Union**), en tant qu’attribut d’interface IDL ou en tant qu’attribut de type IDL.</span><span class="sxs-lookup"><span data-stu-id="5fbd5-113">The ms\_union feature can be used as a command-line switch (**/ms\_union**), an IDL interface attribute, or as an IDL-type attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="5fbd5-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="5fbd5-114">Examples</span></span>

<span data-ttu-id="5fbd5-115">**MIDL/ms. \_ Union fichier. idl**</span><span class="sxs-lookup"><span data-stu-id="5fbd5-115">**midl /ms\_union file.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="5fbd5-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fbd5-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fbd5-117">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="5fbd5-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="5fbd5-118">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="5fbd5-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




