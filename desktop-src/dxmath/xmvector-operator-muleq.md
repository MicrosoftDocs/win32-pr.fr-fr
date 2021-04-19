---
description: Opérateurs d’assignation de multiplication.
ms.assetid: 4d25cef1-8b39-42db-80df-c749940feb0b
title: opérateurs * =, opérateur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 486e85ae8f541c802e50c38d29cd16beb746b587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518142"
---
# <a name="operator--operators"></a><span data-ttu-id="4a0b2-103">Operator \* =, opérateurs</span><span class="sxs-lookup"><span data-stu-id="4a0b2-103">operator \*= operators</span></span>

<span data-ttu-id="4a0b2-104">Opérateurs d’assignation de multiplication</span><span class="sxs-lookup"><span data-stu-id="4a0b2-104">Multiplication assignment operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="4a0b2-105">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="4a0b2-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4a0b2-106">Opérateur</span><span class="sxs-lookup"><span data-stu-id="4a0b2-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4a0b2-107">Description</span><span class="sxs-lookup"><span data-stu-id="4a0b2-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4a0b2-108"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR :: Operator \* = (XMVECTOR&, float)</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a0b2-108"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR::operator \*= (XMVECTOR&,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a0b2-109">Multiplie une <code>XMVECTOR</code> instance par une valeur à virgule flottante et retourne une référence à l’instance mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4a0b2-109">Multiplies an <code>XMVECTOR</code> instance by a floating point value and returns a reference to the updated instance.</span></span> <br/> <span data-ttu-id="4a0b2-110">Le <code>operator \*=</code> multiplie chaque composant de l’instance actuelle du <a href="xmvector-data-type.md"><strong>type de données XMVECTOR</strong></a> par une valeur à virgule flottante spécifiée, en retournant une référence à l’instance actuelle mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4a0b2-110">The <code>operator \*=</code> multiplies each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a specified floating point value, returning a reference to the updated current instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4a0b2-111">Cet opérateur est uniquement disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="4a0b2-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4a0b2-112"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR :: Operator \* = (XMVECTOR&, XMVECTOR)</strong></a></span><span class="sxs-lookup"><span data-stu-id="4a0b2-112"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR::operator \*= (XMVECTOR&,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4a0b2-113">Multiplie une <code>XMVECTOR</code> instance par une deuxième instance, en retournant une référence à l’instance initiale mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4a0b2-113">Multiplies one <code>XMVECTOR</code> instance by a second instance, returning a reference to the updated initial instance.</span></span> <br/> <span data-ttu-id="4a0b2-114">Le <code>operator \*=</code> multiplie chaque composant de l’instance actuelle du <a href="xmvector-data-type.md"><strong>type de données XMVECTOR</strong></a> par le composant correspondant dans une deuxième instance spécifiée de <code>XMVECTOR</code> , en retournant une référence à l’instance initiale mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4a0b2-114">The <code>operator \*=</code> multiplies each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second specified instance of <code>XMVECTOR</code>, returning a reference to the updated initial instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4a0b2-115">Cet opérateur est uniquement disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="4a0b2-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="4a0b2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a0b2-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a0b2-117">XMVECTOR, opérateurs</span><span class="sxs-lookup"><span data-stu-id="4a0b2-117">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="4a0b2-118">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4a0b2-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4a0b2-119">**Type de données XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="4a0b2-119">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
