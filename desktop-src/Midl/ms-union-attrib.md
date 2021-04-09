---
title: ms_union (attribut)
description: Le mot clé \ MS \_ Union \ est utilisé pour contrôler l’alignement du rapport de non-remise des unions non encapsulées.
ms.assetid: 20ac2985-4552-4224-b03b-07378a2c0cdf
keywords:
- ms_union MIDL de l’attribut
topic_type:
- apiref
api_name:
- ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ad9b750027163aef806f5a66e51f87874a0ad2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030064"
---
# <a name="ms_union-attribute"></a><span data-ttu-id="d1117-104">\_attribut ms Union</span><span class="sxs-lookup"><span data-stu-id="d1117-104">ms\_union attribute</span></span>

<span data-ttu-id="d1117-105">Le mot clé \[ **MS \_ Union** \] est utilisé pour contrôler l’alignement du rapport de non-remise des unions non encapsulées.</span><span class="sxs-lookup"><span data-stu-id="d1117-105">The keyword \[**ms\_union**\] is used to control the NDR alignment of nonencapsulated unions.</span></span>

``` syntax
[
    ms_union,
    ...
]
interface interface-name 
{
    ...
}

[ms_union] procedure-type procedure-name(param-list);
```

## <a name="parameters"></a><span data-ttu-id="d1117-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1117-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1117-107">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="d1117-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d1117-108">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="d1117-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="d1117-109">*type de procédure*</span><span class="sxs-lookup"><span data-stu-id="d1117-109">*procedure-type*</span></span> 
</dt> <dd>

<span data-ttu-id="d1117-110">Spécifie le type de retour de la procédure à laquelle l’attribut est appliqué.</span><span class="sxs-lookup"><span data-stu-id="d1117-110">Specifies the return type of the procedure to which the attribute is being applied.</span></span>

</dd> <dt>

<span data-ttu-id="d1117-111">*nom de la procédure*</span><span class="sxs-lookup"><span data-stu-id="d1117-111">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d1117-112">Spécifie le nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="d1117-112">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="d1117-113">*Param-liste*</span><span class="sxs-lookup"><span data-stu-id="d1117-113">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d1117-114">Spécifie la liste de paramètres de la procédure, qui peut être vide.</span><span class="sxs-lookup"><span data-stu-id="d1117-114">Specifies the procedure's parameter list, which may be empty.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1117-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d1117-115">Remarks</span></span>

<span data-ttu-id="d1117-116">N’utilisez jamais ce commutateur ou cet attribut avec les nouvelles interfaces.</span><span class="sxs-lookup"><span data-stu-id="d1117-116">Never use this switch or attribute with new interfaces.</span></span> <span data-ttu-id="d1117-117">Il s’agit uniquement d’une fonctionnalité de compatibilité descendante. Le compilateur MIDL dans cette version de Microsoft RPC reflète le comportement du compilateur de l’IDL ETCD OSF pour les unions qui ne sont pas encapsulées.</span><span class="sxs-lookup"><span data-stu-id="d1117-117">This is a backward compatibility feature only.The MIDL compiler in this version of Microsoft RPC mirrors the behavior of the OSF DCE IDL compiler for nonencapsulated unions.</span></span> <span data-ttu-id="d1117-118">Toutefois, étant donné que les versions antérieures du compilateur MIDL ne l’ont pas fait, le commutateur d' [**\_ Union/ms.**](-ms-union.md) fournit la compatibilité avec les interfaces générées sur les versions précédentes du compilateur MIDL.</span><span class="sxs-lookup"><span data-stu-id="d1117-118">However, because earlier versions of the MIDL compiler did not do so, the [**/ms\_union**](-ms-union.md) switch provides compatibility with interfaces built on previous versions of the MIDL compiler.</span></span>

<span data-ttu-id="d1117-119">La fonctionnalité **MS \_ Union** peut être utilisée en tant qu’attribut d’interface IDL, en tant qu’attribut de type IDL ou en tant que commutateur de ligne de commande ( [**/ms. \_ Union**](-ms-union.md)).</span><span class="sxs-lookup"><span data-stu-id="d1117-119">The **ms\_union** feature can be used as an IDL interface attribute, an IDL type attribute, or as a command-line switch ( [**/ms\_union**](-ms-union.md)).</span></span>

## <a name="examples"></a><span data-ttu-id="d1117-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="d1117-120">Examples</span></span>

``` syntax
[ms_union] long procedure (...);
```

## <a name="see-also"></a><span data-ttu-id="d1117-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1117-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1117-122">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="d1117-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="d1117-123">**/ms. \_ Union**</span><span class="sxs-lookup"><span data-stu-id="d1117-123">**/ms\_union**</span></span>](-ms-union.md)
</dt> </dl>

 

 




