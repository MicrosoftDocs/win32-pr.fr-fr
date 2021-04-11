---
title: Indicateurs de type
description: Les propriétés réelles suivent la table des valeurs de jeu de propriétés d’identificateurs de propriété/de paires de décalage. Chaque propriété est stockée sous la forme d’un DWORD, suivi de la valeur du type de données.
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8383a860f07e908b72a7b25091f3cc2e280e4407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031601"
---
# <a name="type-indicators"></a><span data-ttu-id="577e8-104">Indicateurs de type</span><span class="sxs-lookup"><span data-stu-id="577e8-104">Type Indicators</span></span>

<span data-ttu-id="577e8-105">Les propriétés réelles suivent la table des valeurs de jeu de propriétés d’identificateurs de propriété/de paires de décalage.</span><span class="sxs-lookup"><span data-stu-id="577e8-105">The actual properties follow the table of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="577e8-106">Chaque propriété est stockée sous la forme d’un **DWORD**, suivi de la valeur du type de données.</span><span class="sxs-lookup"><span data-stu-id="577e8-106">Each property is stored as a **DWORD**, followed by the data type value.</span></span>

<span data-ttu-id="577e8-107">Les indicateurs de type et leurs valeurs associées sont décrits dans la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="577e8-107">Type indicators and their associated values are described in the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="577e8-108">Toutes les paires type/valeur doivent commencer sur une limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="577e8-108">All Type/Value pairs must begin on a 32-bit boundary.</span></span> <span data-ttu-id="577e8-109">Par conséquent, les valeurs peuvent être suivies avec des octets null pour aligner la paire suivante sur une limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="577e8-109">Thus, values may be followed with null bytes to align the subsequent pair on a 32-bit boundary.</span></span>

<span data-ttu-id="577e8-110">L’exemple de code suivant calcule le nombre d’octets requis pour l’alignement sur une limite de 32 bits, en fonction d’un nombre d’octets.</span><span class="sxs-lookup"><span data-stu-id="577e8-110">The following example code calculates how many bytes are required to align on a 32-bit boundary, given a count of bytes.</span></span>


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



<span data-ttu-id="577e8-111">Dans un vecteur de valeurs, chaque répétition d’une valeur scalaire simple inférieure à 32 bits doit être alignée avec son alignement naturel plutôt qu’avec un alignement de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="577e8-111">Within a vector of values, each repetition of a simple scalar value smaller than 32 bits must align with its natural alignment rather than with a 32-bit alignment.</span></span> <span data-ttu-id="577e8-112">Dans la pratique, cela n’est significatif que pour les types **VT \_ UI1**, **VT \_ UI2**, **VT \_ I2** et **VT \_ bool** (qui ont un alignement naturel sur un octet ou sur deux octets).</span><span class="sxs-lookup"><span data-stu-id="577e8-112">In practice, this is only significant for types **VT\_UI1**, **VT\_UI2**, **VT\_I2**, and **VT\_BOOL** (which have one-byte or two-byte natural alignment).</span></span> <span data-ttu-id="577e8-113">Tous les autres types ont un alignement naturel sur quatre octets.</span><span class="sxs-lookup"><span data-stu-id="577e8-113">All other types have four-byte natural alignment.</span></span> <span data-ttu-id="577e8-114">Certains types, par exemple, **VT \_ R8**, ont en fait un alignement naturel sur 8 octets, mais ils sont stockés comme s’ils avaient un alignement sur quatre octets.</span><span class="sxs-lookup"><span data-stu-id="577e8-114">Some types, for example, **VT\_R8**, actually have 8-byte natural alignment, but are stored as if they have four-byte alignment.</span></span>

<span data-ttu-id="577e8-115">Une valeur de propriété avec l’indicateur de type **VT \_ I2** \| **VT \_ Vector** contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="577e8-115">A property value with type indicator **VT\_I2** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="577e8-116">Nombre d’éléments **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="577e8-116">A **DWORD** element count.</span></span>
-   <span data-ttu-id="577e8-117">Séquence d’entiers compactés sur deux octets sans remplissage null entre eux.</span><span class="sxs-lookup"><span data-stu-id="577e8-117">A sequence of packed two-byte integers with no null padding between them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="577e8-118">Tout nombre 32 bits ou type de propriété qui sont stockés dans le cadre d’un élément de propriété Vector doit également être aligné sur 32 bits.</span><span class="sxs-lookup"><span data-stu-id="577e8-118">Any 32-bit counts or property types that are stored as a part of a vector property element must also be 32-bit aligned.</span></span>

 

<span data-ttu-id="577e8-119">Une valeur de propriété de type identificateur **VT \_ LPSTR** VT \| **\_ vecteur** inclut les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="577e8-119">A property value of type identifier **VT\_LPSTR** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="577e8-120">Nombre d’éléments **DWORD** (**DWORD** *cElems*).</span><span class="sxs-lookup"><span data-stu-id="577e8-120">A **DWORD** element count (**DWORD** *cElems*).</span></span>
-   <span data-ttu-id="577e8-121">Séquence de chaînes (**char** *RGCH \[ \]*), chacune précédée d’un **DWORD** de longueur-nombre et éventuellement suivie d’un remplissage null pour arrondir à une limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="577e8-121">A sequence of strings (**char** *rgch\[\]*), each preceded by a length-count **DWORD** and possibly followed by null padding to round to a 32-bit boundary.</span></span>

 

 