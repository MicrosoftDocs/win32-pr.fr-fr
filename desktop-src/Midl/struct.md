---
title: struct (attribut)
description: Le mot clé struct est utilisé dans un spécificateur de type structure.
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- MIDL, attribut de struct
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106511282"
---
# <a name="struct-attribute"></a><span data-ttu-id="08e1e-104">struct (attribut)</span><span class="sxs-lookup"><span data-stu-id="08e1e-104">struct attribute</span></span>

<span data-ttu-id="08e1e-105">Le mot clé **struct** est utilisé dans un spécificateur de type structure.</span><span class="sxs-lookup"><span data-stu-id="08e1e-105">The **struct** keyword is used in a structure type specifier.</span></span>

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="08e1e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08e1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08e1e-107">*struct-tag*</span><span class="sxs-lookup"><span data-stu-id="08e1e-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="08e1e-108">Spécifie une balise facultative pour la structure.</span><span class="sxs-lookup"><span data-stu-id="08e1e-108">Specifies an optional tag for the structure.</span></span>

</dd> <dt>

<span data-ttu-id="08e1e-109">*Field-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="08e1e-109">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="08e1e-110">Spécifie zéro, un ou plusieurs attributs de champ qui s’appliquent au membre de la structure.</span><span class="sxs-lookup"><span data-stu-id="08e1e-110">Specifies zero or more field attributes that apply to the structure member.</span></span> <span data-ttu-id="08e1e-111">Les attributs de champ valides sont **\[** [**First \_**](first-is.md)is, **\]** **\[** [**Last \_ is**](last-is.md), **\]** **\[** [**Length \_ is**](length-is.md) **\]** , **\[** [**Max \_ is**](max-is.md) **\]** et **\[** [**size \_ is**](size-is.md) **\]** ; les attributs d’utilisation **\[** [**String**](string.md) **\]** et **\[** [**ignore**](ignore.md) **\]** ; l’attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et le **\[** [**\_ type de commutateur**](switch-type.md)d’attribut Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="08e1e-111">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="08e1e-112">Séparez plusieurs attributs de champ par des virgules.</span><span class="sxs-lookup"><span data-stu-id="08e1e-112">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="08e1e-113">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="08e1e-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="08e1e-114">Spécifie un type de [base](midl-base-types.md), un **struct**, une [**Union**](union.md)ou un type [**enum**](enum.md) ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="08e1e-114">Specifies a [base type](midl-base-types.md), **struct**, [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="08e1e-115">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="08e1e-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="08e1e-116">*déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="08e1e-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="08e1e-117">Spécifie un ou plusieurs déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="08e1e-117">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="08e1e-118">(Les déclarateurs de fonction et les déclarations de champ de bits ne sont pas autorisés dans les structures transmises dans les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="08e1e-118">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="08e1e-119">Ces déclarateurs sont autorisés dans les structures qui ne sont pas transmises.) Séparez plusieurs déclarateurs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="08e1e-119">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08e1e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="08e1e-120">Remarks</span></span>

<span data-ttu-id="08e1e-121">Le spécificateur de type de structure IDL, **struct**, diffère du spécificateur de type C standard de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="08e1e-121">The IDL structure type specifier, **struct**, differs from the standard C type specifier in the following ways:</span></span>

-   <span data-ttu-id="08e1e-122">Chaque membre de structure peut être associé à des attributs de champ facultatifs qui décrivent les caractéristiques de ce membre de structure dans le cadre d’un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="08e1e-122">Each structure member can be associated with optional field attributes that describe characteristics of that structure member for the purposes of a remote procedure call.</span></span>
-   <span data-ttu-id="08e1e-123">Les champs de bits et les déclarateurs de fonction ne sont pas autorisés dans les structures utilisées dans les appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="08e1e-123">Bit fields and function declarators are not allowed in structures that are used in remote procedure calls.</span></span> <span data-ttu-id="08e1e-124">Ces constructions de déclarateur C standard ne peuvent être utilisées que si la structure n’est pas transmise sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="08e1e-124">These standard C declarator constructs can be used only if the structure is not transmitted on the network.</span></span>

<span data-ttu-id="08e1e-125">La forme des structures doit être la même sur toutes les plateformes pour garantir l’interconnexion.</span><span class="sxs-lookup"><span data-stu-id="08e1e-125">The shape of structures must be the same across platforms to ensure interconnectivity.</span></span>

## <a name="examples"></a><span data-ttu-id="08e1e-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="08e1e-126">Examples</span></span>

``` syntax
typedef struct _PITCHER_RECORD_TYPE 
{ 
    short flag; 
    [switch_is(flag)] union PITCHER_STATISTICS_TYPE p; 
} PITCHER_RECORD_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="08e1e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08e1e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08e1e-128">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="08e1e-128">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="08e1e-129">Tableaux et pointeurs</span><span class="sxs-lookup"><span data-stu-id="08e1e-129">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="08e1e-130">Attributs de tableau et de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="08e1e-130">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="08e1e-131">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="08e1e-131">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="08e1e-132">**/c \_ ext**</span><span class="sxs-lookup"><span data-stu-id="08e1e-132">**/c\_ext**</span></span>](-c-ext.md)
</dt> <dt>

[<span data-ttu-id="08e1e-133">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="08e1e-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="08e1e-134">**variables**</span><span class="sxs-lookup"><span data-stu-id="08e1e-134">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="08e1e-135">**tout d’abord, \_**</span><span class="sxs-lookup"><span data-stu-id="08e1e-135">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="08e1e-136">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="08e1e-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="08e1e-137">**tenir**</span><span class="sxs-lookup"><span data-stu-id="08e1e-137">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="08e1e-138">**la dernière \_ est**</span><span class="sxs-lookup"><span data-stu-id="08e1e-138">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="08e1e-139">**la longueur \_ est**</span><span class="sxs-lookup"><span data-stu-id="08e1e-139">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="08e1e-140">**le nombre maximal \_ est**</span><span class="sxs-lookup"><span data-stu-id="08e1e-140">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="08e1e-141">**/osf**</span><span class="sxs-lookup"><span data-stu-id="08e1e-141">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="08e1e-142">**ptr**</span><span class="sxs-lookup"><span data-stu-id="08e1e-142">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="08e1e-143">**ref**</span><span class="sxs-lookup"><span data-stu-id="08e1e-143">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="08e1e-144">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="08e1e-144">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="08e1e-145">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="08e1e-145">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="08e1e-146">**type de commutateur \_**</span><span class="sxs-lookup"><span data-stu-id="08e1e-146">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="08e1e-147">**UE**</span><span class="sxs-lookup"><span data-stu-id="08e1e-147">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="08e1e-148">**unique**</span><span class="sxs-lookup"><span data-stu-id="08e1e-148">**unique**</span></span>](unique.md)
</dt> </dl>

 

 