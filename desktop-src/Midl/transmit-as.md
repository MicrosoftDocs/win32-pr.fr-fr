---
title: transmit_as (attribut)
description: L’attribut \ transmit \_ As \ demande au compilateur d’associer l’ID de type, qui est un type présenté que les applications client et serveur manipulent, avec un type de transmission de type transmis.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- transmit_as MIDL de l’attribut
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec0cba27e994f7d77d441aef7bb783cad71cbad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510875"
---
# <a name="transmit_as-attribute"></a><span data-ttu-id="738fb-104">transmettre \_ en tant qu’attribut</span><span class="sxs-lookup"><span data-stu-id="738fb-104">transmit\_as attribute</span></span>

<span data-ttu-id="738fb-105">L’attribut **\[ transmit \_ As \]** indique au compilateur d’associer \*\*type-ID \* \* *,* qui est un type présenté que les applications client et serveur manipulent, avec un type transmis de type transmission **.**</span><span class="sxs-lookup"><span data-stu-id="738fb-105">The **\[transmit\_as\]** attribute instructs the compiler to associate \**type-id\*\*\*,* which is a presented type that client and server applications manipulate, with a transmitted type **xmit-type.**</span></span>

``` syntax
typedef [transmit_as(xmit-type) [[ , type-attribute-list ]] ] type-specifier declarator-list; 

void __RPC_USER type-id_to_xmit (
  type-id __RPC_FAR *,
  xmit-type __RPC_FAR * __RPC_FAR *);
void __RPC_USER type-id_from_xmit (
  xmit-type __RPC_FAR *,
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_inst (
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_xmit (
  xmit-type__RPC_FAR *);
```

## <a name="parameters"></a><span data-ttu-id="738fb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="738fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="738fb-107">*type de transmission*</span><span class="sxs-lookup"><span data-stu-id="738fb-107">*xmit-type*</span></span> 
</dt> <dd>

<span data-ttu-id="738fb-108">Spécifie le type de données transmis entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="738fb-108">Specifies the data type that is transmitted between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="738fb-109">*type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="738fb-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="738fb-110">Spécifie un ou plusieurs attributs qui s’appliquent au type.</span><span class="sxs-lookup"><span data-stu-id="738fb-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="738fb-111">Les attributs de type valides incluent **\[** [**handle**](handle.md) **\]** , **\[** [**\_ type de commutateur**](switch-type.md) **\]** ; attribut de pointeur **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** ou **\[** [**ptr**](ptr.md) **\]** ; et la chaîne d’attributs d’utilisation **\[** [](string.md) **\]** et **\[** [**ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="738fb-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="738fb-112">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="738fb-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="738fb-113">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="738fb-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="738fb-114">Spécifie un [type de base](midl-base-types.md), un [**struct**](struct.md), une [**Union**](union.md), un type [**enum**](enum.md) ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="738fb-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="738fb-115">Une spécification de stockage facultative peut précéder *le type-specifier*.</span><span class="sxs-lookup"><span data-stu-id="738fb-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="738fb-116">*déclarateur-liste*</span><span class="sxs-lookup"><span data-stu-id="738fb-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="738fb-117">Spécifie les déclarateurs C standard, tels que les identificateurs, les déclarateurs de pointeurs et les déclarateurs de tableau.</span><span class="sxs-lookup"><span data-stu-id="738fb-117">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="738fb-118">Pour plus d’informations, consultez [tableau et Sized-Pointer attributs](array-and-sized-pointer-attributes.md), [**tableaux**](arrays-1.md), tableaux [et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="738fb-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="738fb-119">La *liste déclarateur* se compose d’un ou de plusieurs déclarateurs séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="738fb-119">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="738fb-120">Le déclarateur de paramètre dans le déclarateur de fonction, tel que le nom du paramètre, est facultatif.</span><span class="sxs-lookup"><span data-stu-id="738fb-120">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> <dt>

<span data-ttu-id="738fb-121">*ID de type*</span><span class="sxs-lookup"><span data-stu-id="738fb-121">*type-id*</span></span> 
</dt> <dd>

<span data-ttu-id="738fb-122">Spécifie le nom du type de données présenté aux applications clientes et serveur.</span><span class="sxs-lookup"><span data-stu-id="738fb-122">Specifies the name of the data type that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="738fb-123">Notes</span><span class="sxs-lookup"><span data-stu-id="738fb-123">Remarks</span></span>

<span data-ttu-id="738fb-124">Pour utiliser l’attribut **\[ transmettre \_ en tant que \]** , l’utilisateur doit fournir des routines qui convertissent les données entre les types présentés et transmis ; ces routines doivent également libérer de la mémoire utilisée pour stocker les données converties.</span><span class="sxs-lookup"><span data-stu-id="738fb-124">To use the **\[transmit\_as\]** attribute, the user must supply routines that convert data between the presented and the transmitted types; these routines must also free memory used to hold the converted data.</span></span> <span data-ttu-id="738fb-125">L’attribut **\[ transmit \_ As \]** indique aux stubs d’appeler les routines de conversion fournies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="738fb-125">The **\[transmit\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="738fb-126">Le type *de* transmission de type transmis doit être résolu en un type de base MIDL, un type prédéfini ou un identificateur de type.</span><span class="sxs-lookup"><span data-stu-id="738fb-126">The transmitted type *xmit-type* must resolve to a MIDL base type, predefined type, or a type identifier.</span></span> <span data-ttu-id="738fb-127">Pour plus d’informations, consultez [types de base MIDL](midl-base-types.md).</span><span class="sxs-lookup"><span data-stu-id="738fb-127">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="738fb-128">L’utilisateur doit fournir les routines suivantes.</span><span class="sxs-lookup"><span data-stu-id="738fb-128">The user must supply the following routines.</span></span>



| <span data-ttu-id="738fb-129">Nom de la routine</span><span class="sxs-lookup"><span data-stu-id="738fb-129">Routine name</span></span>              | <span data-ttu-id="738fb-130">Description</span><span class="sxs-lookup"><span data-stu-id="738fb-130">Description</span></span>                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="738fb-131">*type-ID \* \* \* \_ à \_ transmission*\*</span><span class="sxs-lookup"><span data-stu-id="738fb-131">*type-id\*\*\*\_to\_xmit*\*</span></span>   | <span data-ttu-id="738fb-132">Convertit les données du type présenté en type transmis.</span><span class="sxs-lookup"><span data-stu-id="738fb-132">Converts data from the presented type to the transmitted type.</span></span> <span data-ttu-id="738fb-133">Cette routine alloue de la mémoire pour le type transmis et pour toutes les données référencées par des pointeurs dans le type transmis.</span><span class="sxs-lookup"><span data-stu-id="738fb-133">This routine allocates memory for the transmitted type and for any data referenced by pointers in the transmitted type.</span></span>                            |
| <span data-ttu-id="738fb-134">*ID de type \* \* \* \_ de l' \_ émetteur*\*</span><span class="sxs-lookup"><span data-stu-id="738fb-134">*type-id\*\*\*\_from\_xmit*\*</span></span> | <span data-ttu-id="738fb-135">Convertit les données du type transmis vers le type présenté.</span><span class="sxs-lookup"><span data-stu-id="738fb-135">Converts data from the transmitted type to the presented type.</span></span> <span data-ttu-id="738fb-136">Cette routine est chargée d’allouer de la mémoire pour les données référencées par des pointeurs dans le type présenté.</span><span class="sxs-lookup"><span data-stu-id="738fb-136">This routine is responsible for allocating memory for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="738fb-137">RPC alloue de la mémoire pour le type lui-même.</span><span class="sxs-lookup"><span data-stu-id="738fb-137">RPC allocates memory for the type itself.</span></span> |
| <span data-ttu-id="738fb-138">*ID de type \* \* \* \_ Free \_ inst*\*</span><span class="sxs-lookup"><span data-stu-id="738fb-138">*type-id\*\*\*\_free\_inst*\*</span></span> | <span data-ttu-id="738fb-139">Libère la mémoire allouée pour les données référencées par des pointeurs dans le type présenté.</span><span class="sxs-lookup"><span data-stu-id="738fb-139">Frees memory allocated for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="738fb-140">RPC libère de la mémoire pour le type lui-même.</span><span class="sxs-lookup"><span data-stu-id="738fb-140">RPC frees memory for the type itself.</span></span>                                                                                               |
| <span data-ttu-id="738fb-141">*type-ID \* \* \* transmission \_ gratuite \_*\*</span><span class="sxs-lookup"><span data-stu-id="738fb-141">*type-id\*\*\*\_free\_xmit*\*</span></span> | <span data-ttu-id="738fb-142">Libère le stockage utilisé par l’appelant pour le type transmis et pour les données référencées par des pointeurs dans le type transmis.</span><span class="sxs-lookup"><span data-stu-id="738fb-142">Frees storage used by the caller for the transmitted type and for data referenced by pointers in the transmitted type.</span></span>                                                                                            |



 

 

<span data-ttu-id="738fb-143">Le stub client appelle l' *ID de type \* \* \_ \* \_ pour* transmettre \* pour allouer de l’espace pour le type transmis et pour convertir les données en objets de type transmission *-type.*</span><span class="sxs-lookup"><span data-stu-id="738fb-143">The client stub calls *type-id\*\*\*\_to\_xmit*\* to allocate space for the transmitted type and to translate the data into objects of type *xmit-type.*</span></span> <span data-ttu-id="738fb-144">Le stub serveur alloue de l’espace pour le type de données d’origine et appelle l' *ID de type \* \* \* \_ à partir de \_* transmission \* pour convertir les données de son type transmis vers le type présenté.</span><span class="sxs-lookup"><span data-stu-id="738fb-144">The server stub allocates space for the original data type and calls *type-id\*\*\*\_from\_xmit*\* to translate the data from its transmitted type to the presented type.</span></span>

<span data-ttu-id="738fb-145">Lors du retour du code de l’application, le stub serveur appelle le *type-ID \* \* \* \_ Free \_ inst*\* pour libérer le stockage de l' *ID de type* côté serveur.</span><span class="sxs-lookup"><span data-stu-id="738fb-145">Upon return from the application code, the server stub calls *type-id\*\*\*\_free\_inst*\* to deallocate the storage for *type-id* on the server side.</span></span> <span data-ttu-id="738fb-146">Le stub client appelle l' *ID de type \* \* \* transmission \_ gratuite \_*\* pour libérer le stockage de *type* transmission côté client.</span><span class="sxs-lookup"><span data-stu-id="738fb-146">The client stub calls *type-id\*\*\*\_free\_xmit*\* to deallocate the *xmit-type* storage on the client side.</span></span>

<span data-ttu-id="738fb-147">Les types suivants ne peuvent pas avoir d’attribut **\[ transmit \_ As \]** :</span><span class="sxs-lookup"><span data-stu-id="738fb-147">The following types cannot have a **\[transmit\_as\]** attribute:</span></span>

-   <span data-ttu-id="738fb-148">Handles de contexte (types avec l’attribut de type de **\[** [**\_ handle de contexte**](context-handle.md) **\]** et les types utilisés comme paramètres avec l’attribut de **\[ \_ handle \] de contexte** )</span><span class="sxs-lookup"><span data-stu-id="738fb-148">Context handles (types with the **\[**[**context\_handle**](context-handle.md)**\]** type attribute and types that are used as parameters with the **\[context\_handle\]** attribute)</span></span>
-   <span data-ttu-id="738fb-149">Types qui sont des canaux ou dérivés de canaux</span><span class="sxs-lookup"><span data-stu-id="738fb-149">Types that are pipes or derived from pipes</span></span>
-   <span data-ttu-id="738fb-150">Types de données utilisés comme type de base d’une définition de canal</span><span class="sxs-lookup"><span data-stu-id="738fb-150">Data types that are used as the base type of a pipe definition</span></span>
-   <span data-ttu-id="738fb-151">Paramètres qui sont des pointeurs ou qui sont résolus en pointeurs</span><span class="sxs-lookup"><span data-stu-id="738fb-151">Parameters that are pointers or resolve to pointers</span></span>
-   <span data-ttu-id="738fb-152">Paramètres qui sont des tableaux conformes, variables ou ouverts</span><span class="sxs-lookup"><span data-stu-id="738fb-152">Parameters that are conformant, varying, or open arrays</span></span>
-   <span data-ttu-id="738fb-153">Structures qui contiennent des tableaux conformes</span><span class="sxs-lookup"><span data-stu-id="738fb-153">Structures that contain conformant arrays</span></span>
-   <span data-ttu-id="738fb-154">Handle de type prédéfini [**\_ t**](handle-t.md), [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="738fb-154">The predefined type [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>

<span data-ttu-id="738fb-155">Les types transmis doivent respecter les restrictions suivantes :</span><span class="sxs-lookup"><span data-stu-id="738fb-155">Types that are transmitted must conform to the following restrictions:</span></span>

-   <span data-ttu-id="738fb-156">Ils ne doivent pas être des pointeurs ou contenir des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="738fb-156">They must not be pointers or contain pointers.</span></span>
-   <span data-ttu-id="738fb-157">Ils ne doivent pas être des canaux ou contenir des canaux.</span><span class="sxs-lookup"><span data-stu-id="738fb-157">They must not be pipes or contain pipes.</span></span>

## <a name="examples"></a><span data-ttu-id="738fb-158">Exemples</span><span class="sxs-lookup"><span data-stu-id="738fb-158">Examples</span></span>

``` syntax
typedef struct _TREE_NODE_TYPE 
{ 
    unsigned short data; 
    struct _TREE_NODE_TYPE * left; 
    struct _TREE_NODE_TYPE * right; 
} TREE_NODE_TYPE; 
 
typedef [transmit_as(TREE_XMIT_TYPE)] TREE_NODE_TYPE * TREE_TYPE; 
 
void __RPC_USER TREE_TYPE_to_xmit( 
    TREE_TYPE __RPC_FAR * , 
    TREE_XMIT_TYPE __RPC_FAR * __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_from_xmit ( 
    TREE_XMIT_TYPE __RPC_FAR *, 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_inst( 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_xmit( 
    TREE_XMIT_TYPE __RPC_FAR *);
```

## <a name="see-also"></a><span data-ttu-id="738fb-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="738fb-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="738fb-160">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="738fb-160">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="738fb-161">Types de base MIDL</span><span class="sxs-lookup"><span data-stu-id="738fb-161">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="738fb-162">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="738fb-162">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="738fb-163">**variables**</span><span class="sxs-lookup"><span data-stu-id="738fb-163">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="738fb-164">**traitée**</span><span class="sxs-lookup"><span data-stu-id="738fb-164">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="738fb-165">**handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="738fb-165">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="738fb-166">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="738fb-166">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="738fb-167">**tenir**</span><span class="sxs-lookup"><span data-stu-id="738fb-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="738fb-168">**ptr**</span><span class="sxs-lookup"><span data-stu-id="738fb-168">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="738fb-169">**ref**</span><span class="sxs-lookup"><span data-stu-id="738fb-169">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="738fb-170">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="738fb-170">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="738fb-171">**modélis**</span><span class="sxs-lookup"><span data-stu-id="738fb-171">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="738fb-172">**type de commutateur \_**</span><span class="sxs-lookup"><span data-stu-id="738fb-172">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="738fb-173">**typedef**</span><span class="sxs-lookup"><span data-stu-id="738fb-173">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="738fb-174">**UE**</span><span class="sxs-lookup"><span data-stu-id="738fb-174">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="738fb-175">**unique**</span><span class="sxs-lookup"><span data-stu-id="738fb-175">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="738fb-176">**void**</span><span class="sxs-lookup"><span data-stu-id="738fb-176">**void**</span></span>](void.md)
</dt> </dl>

 

 