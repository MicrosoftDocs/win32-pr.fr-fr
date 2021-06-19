---
title: Pointeurs (RPC)
description: En savoir plus sur un pointeur commun RPC, qui est défini comme tout autre que les pointeurs d’interface et les pointeurs de nombre d’octets.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e41a0b6208745b543a9efe2fe22ab090046778
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406592"
---
# <a name="pointers-rpc"></a><span data-ttu-id="56f4a-103">Pointeurs (RPC)</span><span class="sxs-lookup"><span data-stu-id="56f4a-103">Pointers (RPC)</span></span>

## <a name="common-pointers"></a><span data-ttu-id="56f4a-104">Pointeurs communs</span><span class="sxs-lookup"><span data-stu-id="56f4a-104">Common Pointers</span></span>

<span data-ttu-id="56f4a-105">Un pointeur commun est défini comme tout autre que les pointeurs d’interface et les pointeurs de nombre d’octets.</span><span class="sxs-lookup"><span data-stu-id="56f4a-105">A common pointer is defined as everything other than interface pointers and byte count pointers.</span></span>

<span data-ttu-id="56f4a-106">Il existe deux dispositions possibles pour la description :</span><span class="sxs-lookup"><span data-stu-id="56f4a-106">There are two possible layouts for the description:</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

<span data-ttu-id="56f4a-107">–ou–</span><span class="sxs-lookup"><span data-stu-id="56f4a-107">–or–</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

<span data-ttu-id="56f4a-108">Le premier format est utilisé si le pointeur est un pointeur vers un type simple ou un pointeur de chaîne non dimensionné.</span><span class="sxs-lookup"><span data-stu-id="56f4a-108">The first format is used if the pointer is a pointer to a simple type or a nonsized string pointer.</span></span> <span data-ttu-id="56f4a-109">Le deuxième format est utilisé pour les pointeurs vers tous les autres types.</span><span class="sxs-lookup"><span data-stu-id="56f4a-109">The second format is used for pointers to all other types.</span></span> <span data-ttu-id="56f4a-110">Les attributs de pointeur indiquent la disposition de description avec l' \_ indicateur de pointeur simple FC \_ .</span><span class="sxs-lookup"><span data-stu-id="56f4a-110">Pointer attributes indicate which description layout it is with the FC\_SIMPLE\_POINTER flag.</span></span>

<span data-ttu-id="56f4a-111">\_le type de pointeur<1> est l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="56f4a-111">pointer\_type<1> is one of the following.</span></span>



| <span data-ttu-id="56f4a-112">Caractère de format</span><span class="sxs-lookup"><span data-stu-id="56f4a-112">Format character</span></span> | <span data-ttu-id="56f4a-113">Description</span><span class="sxs-lookup"><span data-stu-id="56f4a-113">Description</span></span>                              |
|------------------|------------------------------------------|
| <span data-ttu-id="56f4a-114">Fibre Channel \_ RP</span><span class="sxs-lookup"><span data-stu-id="56f4a-114">FC\_RP</span></span>           | <span data-ttu-id="56f4a-115">Pointeur de référence.</span><span class="sxs-lookup"><span data-stu-id="56f4a-115">A reference pointer.</span></span>                     |
| <span data-ttu-id="56f4a-116">haut de la fibre \_</span><span class="sxs-lookup"><span data-stu-id="56f4a-116">FC\_UP</span></span>           | <span data-ttu-id="56f4a-117">Pointeur unique.</span><span class="sxs-lookup"><span data-stu-id="56f4a-117">A unique pointer.</span></span>                        |
| <span data-ttu-id="56f4a-118">\_FP FC</span><span class="sxs-lookup"><span data-stu-id="56f4a-118">FC\_FP</span></span>           | <span data-ttu-id="56f4a-119">Pointeur complet.</span><span class="sxs-lookup"><span data-stu-id="56f4a-119">A full pointer.</span></span>                          |
| <span data-ttu-id="56f4a-120">\_op FC</span><span class="sxs-lookup"><span data-stu-id="56f4a-120">FC\_OP</span></span>           | <span data-ttu-id="56f4a-121">Pointeur unique dans une interface d’objet.</span><span class="sxs-lookup"><span data-stu-id="56f4a-121">A unique pointer in an object interface.</span></span> |



 

<span data-ttu-id="56f4a-122">La raison de la distinction entre FC \_ op est sémantique : dans les interfaces d’objet, un \[ pointeur in, out \] doit être libéré avant d’annuler le marshaling d’un nouvel objet et d’assigner une nouvelle valeur de pointeur.</span><span class="sxs-lookup"><span data-stu-id="56f4a-122">The reason to distinguish FC\_OP is semantic: in object interfaces, an \[in,out\] pointer should be freed before unmarshaling a new object and assigning a new pointer value.</span></span>

<span data-ttu-id="56f4a-123">Les \_ attributs de pointeur<1> peuvent avoir l’un des indicateurs répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="56f4a-123">Pointer\_attributes<1> can have any of the flags shown in the following table.</span></span>



| <span data-ttu-id="56f4a-124">Indicateur</span><span class="sxs-lookup"><span data-stu-id="56f4a-124">Flag</span></span> | <span data-ttu-id="56f4a-125">Description</span><span class="sxs-lookup"><span data-stu-id="56f4a-125">Description</span></span>              |                                                                                                                                                                                                                                       |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56f4a-126">01</span><span class="sxs-lookup"><span data-stu-id="56f4a-126">01</span></span>   | <span data-ttu-id="56f4a-127">FC- \_ allouer \_ tous les \_ nœuds</span><span class="sxs-lookup"><span data-stu-id="56f4a-127">FC\_ALLOCATE\_ALL\_NODES</span></span> | <span data-ttu-id="56f4a-128">Le pointeur fait partie d’un schéma d’allocation Allocate (tous les \_ nœuds).</span><span class="sxs-lookup"><span data-stu-id="56f4a-128">The pointer is a part of an allocate(all\_nodes) allocation scheme.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="56f4a-129">02</span><span class="sxs-lookup"><span data-stu-id="56f4a-129">02</span></span>   | <span data-ttu-id="56f4a-130">FC n’est pas \_ \_ libre</span><span class="sxs-lookup"><span data-stu-id="56f4a-130">FC\_DONT\_FREE</span></span>           | <span data-ttu-id="56f4a-131">Pointeur Allocate (ne pas \_ libérer).</span><span class="sxs-lookup"><span data-stu-id="56f4a-131">An allocate(dont\_free) pointer.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="56f4a-132">04</span><span class="sxs-lookup"><span data-stu-id="56f4a-132">04</span></span>   | <span data-ttu-id="56f4a-133">FC \_ alloué \_ sur la \_ pile</span><span class="sxs-lookup"><span data-stu-id="56f4a-133">FC\_ALLOCED\_ON\_STACK</span></span>   | <span data-ttu-id="56f4a-134">Pointeur dont le référent est alloué sur la pile du stub.</span><span class="sxs-lookup"><span data-stu-id="56f4a-134">A pointer whose referent is allocated on the stub's stack.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="56f4a-135">08</span><span class="sxs-lookup"><span data-stu-id="56f4a-135">08</span></span>   | <span data-ttu-id="56f4a-136">\_pointeur simple \_ FC</span><span class="sxs-lookup"><span data-stu-id="56f4a-136">FC\_SIMPLE\_POINTER</span></span>      | <span data-ttu-id="56f4a-137">Pointeur vers un type simple ou une chaîne conforme non dimensionnée.</span><span class="sxs-lookup"><span data-stu-id="56f4a-137">A pointer to a simple type or nonsized conformant string.</span></span> <span data-ttu-id="56f4a-138">Cet indicateur défini indique la disposition de la description du pointeur comme disposition simple du pointeur décrite ci-dessus, sinon le format du descripteur avec l’offset est indiqué.</span><span class="sxs-lookup"><span data-stu-id="56f4a-138">This flag being set indicates layout of the pointer description as the simple pointer layout described above, otherwise the descriptor format with the offset is indicated.</span></span> |
| <span data-ttu-id="56f4a-139">10</span><span class="sxs-lookup"><span data-stu-id="56f4a-139">10</span></span>   | <span data-ttu-id="56f4a-140">\_Deref du pointeur FC \_</span><span class="sxs-lookup"><span data-stu-id="56f4a-140">FC\_POINTER\_DEREF</span></span>       | <span data-ttu-id="56f4a-141">Pointeur qui doit être déréférencé avant de gérer le référent du pointeur.</span><span class="sxs-lookup"><span data-stu-id="56f4a-141">A pointer that must be dereferenced before handling the pointer's referent.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="56f4a-142">Les pointeurs dont la taille \_ est (), Max \_ is (), Length \_ est (), Last \_ is () et/ou First \_ est () s’y appliquent des descriptions de chaîne de format identiques à un pointeur vers un tableau du type approprié (par exemple, un tableau conforme si la taille est \_ () est appliquée, un tableau variable conforme si la taille \_ est () et si la longueur est \_ appliquée).</span><span class="sxs-lookup"><span data-stu-id="56f4a-142">Pointers that have size\_is(), max\_is(), length\_is(), last\_is(), and/or first\_is() applied to them have format string descriptions identical to a pointer to an array of the appropriate type (for example, a conformant array if size\_is() is applied, a conformant varying array if size\_is() and length\_is are applied).</span></span>

## <a name="interface-pointers"></a><span data-ttu-id="56f4a-143">Pointeurs d’interface</span><span class="sxs-lookup"><span data-stu-id="56f4a-143">Interface Pointers</span></span>

<span data-ttu-id="56f4a-144">Une chaîne de format de pointeur d’interface d’objet a l’un des deux formats, selon que l’IID correspondant est connu du compilateur ou non.</span><span class="sxs-lookup"><span data-stu-id="56f4a-144">An object interface pointer format string has one of two formats, depending on whether the corresponding IID is known to the compiler.</span></span>

<span data-ttu-id="56f4a-145">Un pointeur d’interface avec un IID de constante a la description suivante :</span><span class="sxs-lookup"><span data-stu-id="56f4a-145">An interface pointer with a constant IID has the following description:</span></span>

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

<span data-ttu-id="56f4a-146">L’IID<16> composant est l’IID réel du pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="56f4a-146">The iid<16> part is the actual IID for the interface pointer.</span></span> <span data-ttu-id="56f4a-147">L’IID est écrit dans la chaîne de format dans un format identique à la structure de données GUID : long, Short, Short, char \[ 8 \] .</span><span class="sxs-lookup"><span data-stu-id="56f4a-147">The iid is written to the format string in a format identical to the GUID data structure: long, short, short, char \[8\].</span></span>

<span data-ttu-id="56f4a-148">La description d’un pointeur d’interface avec IID \_ est () appliquée à celle-ci :</span><span class="sxs-lookup"><span data-stu-id="56f4a-148">The description of an interface pointer with iid\_is() applied to it is:</span></span>

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

<span data-ttu-id="56f4a-149">La \_ Description iid<> est un descripteur de corrélation et contient 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non.</span><span class="sxs-lookup"><span data-stu-id="56f4a-149">The iid\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="56f4a-150">La valeur calculée par la fonction **NdrComputeConformance** est le pointeur iid.</span><span class="sxs-lookup"><span data-stu-id="56f4a-150">The value calculated by the **NdrComputeConformance** function is the IID pointer.</span></span>

## <a name="byte-count-pointers"></a><span data-ttu-id="56f4a-151">Pointeurs de nombre d’octets</span><span class="sxs-lookup"><span data-stu-id="56f4a-151">Byte Count Pointers</span></span>

<span data-ttu-id="56f4a-152">Les pointeurs de nombre d’octets sont liés à un attribut d’optimisation spécial appelé \[ **\_ nombre d’octets** \] .</span><span class="sxs-lookup"><span data-stu-id="56f4a-152">Byte count pointers relate to a special optimization attribute called \[**byte\_count**\].</span></span> <span data-ttu-id="56f4a-153">Les formats suivants sont utilisés :</span><span class="sxs-lookup"><span data-stu-id="56f4a-153">The following formats are used:</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

<span data-ttu-id="56f4a-154">les</span><span class="sxs-lookup"><span data-stu-id="56f4a-154">–and –</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<span data-ttu-id="56f4a-155">La \_ Description du nombre \_ d’octets<> est un descripteur de corrélation et contient 4 ou 6 octets selon que [**/Robust**](/windows/desktop/Midl/-robust) est utilisé ou non.</span><span class="sxs-lookup"><span data-stu-id="56f4a-155">The byte\_count\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

<span data-ttu-id="56f4a-156">La description du pointee \_<> est une description du type de point.</span><span class="sxs-lookup"><span data-stu-id="56f4a-156">The pointee\_description<> is a description of the pointee type.</span></span>

 

 
