---
title: Transmit_as et Represent_as
description: Transmettre \_ en tant que et représenter \_ comme partage la même disposition, à l’exception du jeton de début ; le jeton lit FC \_ transmit \_ As ou FC \_ représente \_ comme, mais le code sous-jacent est courant.
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941032"
---
# <a name="transmit_as-and-represent_as"></a><span data-ttu-id="fb567-103">Transmettre \_ en tant que et représenter \_ comme</span><span class="sxs-lookup"><span data-stu-id="fb567-103">Transmit\_as and Represent\_as</span></span>

<span data-ttu-id="fb567-104">Transmettre \_ en tant que et représenter \_ comme partage la même disposition, à l’exception du jeton de début ; le jeton lit FC \_ transmit \_ As ou FC \_ représente \_ comme, mais le code sous-jacent est courant.</span><span class="sxs-lookup"><span data-stu-id="fb567-104">Transmit\_as and represent\_as share the same layout except for the leading token; the token reads FC\_TRANSMIT\_AS or FC\_REPRESENT\_AS, but the underlying code is common.</span></span>

<span data-ttu-id="fb567-105">La description présente la disposition suivante :</span><span class="sxs-lookup"><span data-stu-id="fb567-105">The description has the following layout:</span></span>

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

<span data-ttu-id="fb567-106">Les indicateurs<1> octet se composent du Quartet indicateur supérieur et du Quartet alignement inférieur.</span><span class="sxs-lookup"><span data-stu-id="fb567-106">The flags<1> byte consists of the upper flag nibble and the lower alignment nibble.</span></span>

<span data-ttu-id="fb567-107">Le grignot d’alignement conserve l’alignement filaire du type transmis.</span><span class="sxs-lookup"><span data-stu-id="fb567-107">The alignment nibble keeps the wire alignment of the transmitted type.</span></span> <span data-ttu-id="fb567-108">Cela est nécessaire lorsque le dimensionnement de la mémoire tampon et l’utilisation de la taille de type transmis à partir du code de format.</span><span class="sxs-lookup"><span data-stu-id="fb567-108">This is needed when buffer sizing and using the transmitted type size from the format code.</span></span>

<span data-ttu-id="fb567-109">L’indicateur Quartet peut avoir les indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="fb567-109">The flag nibble can have the following flags:</span></span>

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

<span data-ttu-id="fb567-110">Le \_ type présenté \_ est \_ un indicateur de tableau qui marque une transmission de niveau supérieur en tant qu’argument (ou représente en tant que) comme un tableau d’éléments et une valeur passée.</span><span class="sxs-lookup"><span data-stu-id="fb567-110">The PRESENTED\_TYPE\_IS\_ARRAY flag marks a top-level transmit as (or represent as) argument being an array of something and passed-by value.</span></span> <span data-ttu-id="fb567-111">L’interpréteur [**– OI**](/windows/desktop/Midl/-oi) utilise cet indicateur pour effectuer un pas à pas principal de ce type d’argument (qui est en fait un pointeur sur Stack, et non sur le tableau).</span><span class="sxs-lookup"><span data-stu-id="fb567-111">The [**–Oi**](/windows/desktop/Midl/-oi) interpreter uses this flag to step over such an argument (which is actually a pointer on stack, not the array).</span></span> <span data-ttu-id="fb567-112">Les deux autres indicateurs sont également utilisés uniquement dans les interpréteurs précédents pour effectuer un pas à pas détaillé sur un type présenté sur la pile.</span><span class="sxs-lookup"><span data-stu-id="fb567-112">The other two flags are also used only in previous interpreters to step correctly over a presented type on the stack.</span></span>

<span data-ttu-id="fb567-113">L' \_ index quintuple<2> est un index de la routine de rappel quintuple (il s’agit en fait d’un quadruple) de fonctions.</span><span class="sxs-lookup"><span data-stu-id="fb567-113">The quintuple\_index<2> is an index of the callback routine quintuple (this is actually a quadruple) of functions.</span></span> <span data-ttu-id="fb567-114">La table est commune à la fois à transmit As et à replacer en tant que et il existe un mappage évident pour la position des routines, étant donné que le même service de points d’entrée transmet les codes et les représente comme des codes.</span><span class="sxs-lookup"><span data-stu-id="fb567-114">The table is common to both transmit as and represent as and there is an obvious mapping for the position of the routines, as the same entry points service transmit as and represent as codes.</span></span> <span data-ttu-id="fb567-115">Le mappage est de \_ local => à transmission \_ , à \_ local => de transmission \_ , Free \_ inst => transmission gratuite \_ , Free \_ local => Free \_ inst.</span><span class="sxs-lookup"><span data-stu-id="fb567-115">The mapping is from\_local => to\_xmit, to\_local => from\_xmit, free\_inst => free\_xmit, free\_local => free\_inst.</span></span>

<span data-ttu-id="fb567-116">La \_ \_ \_ taille de mémoire de type présentée<2> fournit toujours une taille pour le type présenté/local, y compris les types de représentation inconnus.</span><span class="sxs-lookup"><span data-stu-id="fb567-116">The presented\_type\_memory\_size<2> always provides a size for the presented/local type, including unknown represent as types.</span></span>

<span data-ttu-id="fb567-117">La taille de la \_ mémoire tampon de type transmis \_ \_<2> est égale à zéro, lorsque la taille est variable ou la taille fixe réelle.</span><span class="sxs-lookup"><span data-stu-id="fb567-117">The transmitted\_type\_buffer\_size<2> is either zero, when the size is varying, or the actual fixed size.</span></span> <span data-ttu-id="fb567-118">Il s’agit d’une optimisation qui permet d’ignorer certains rappels lors du dimensionnement de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fb567-118">This is an optimization that enables skipping some callbacks when sizing the buffer.</span></span>

<span data-ttu-id="fb567-119">Le \_ décalage de type transmis \_<2> est le décalage de type relatif habituel par rapport à la chaîne de format de type transmis.</span><span class="sxs-lookup"><span data-stu-id="fb567-119">The transmitted\_type\_offset<2> is the usual relative type offset to the transmitted type format string.</span></span>

 

 