---
description: Opérateurs de multiplication.
ms.assetid: f8397999-9956-4d11-8705-c95b788a9f03
title: opérateurs Operator *
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 15cdb9d189d110621461c1623b4fd20eaa9e7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114466"
---
# <a name="operator--operators"></a><span data-ttu-id="281e0-103">\*opérateurs opérateur</span><span class="sxs-lookup"><span data-stu-id="281e0-103">operator \* operators</span></span>

<span data-ttu-id="281e0-104">Opérateurs de multiplication</span><span class="sxs-lookup"><span data-stu-id="281e0-104">Multiplication operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="281e0-105">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="281e0-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="281e0-106">Opérateur</span><span class="sxs-lookup"><span data-stu-id="281e0-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="281e0-107">Description</span><span class="sxs-lookup"><span data-stu-id="281e0-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="281e0-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR :: Operator \* (float, XMVECTOR)</strong></a></span><span class="sxs-lookup"><span data-stu-id="281e0-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR::operator \* (float,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="281e0-109">Multipliez une valeur à virgule flottante par une instance de <code>XMVECTOR</code> , en retournant le résultat à une nouvelle instance de <code>XMVECTOR</code> .</span><span class="sxs-lookup"><span data-stu-id="281e0-109">Multiply a floating point value by an instance of <code>XMVECTOR</code>, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="281e0-110">Le <code>operator \*</code> multiplie une valeur à virgule flottante par rapport à chaque composant d’une instance de <a href="xmvector-data-type.md"><strong>type de données XMVECTOR</strong></a>, en retournant une nouvelle <code>XMVECTOR</code> instance dont les composants contiennent le résultat.</span><span class="sxs-lookup"><span data-stu-id="281e0-110">The <code>operator \*</code> multiplies a floating point value against each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a>, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="281e0-111">Cet opérateur est uniquement disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="281e0-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="281e0-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR :: Operator \* (XMVECTOR, float)</strong></a></span><span class="sxs-lookup"><span data-stu-id="281e0-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="281e0-113">Multipliez une instance de <code>XMVECTOR</code> par une valeur à virgule flottante, en retournant le résultat à une nouvelle instance de <code>XMVECTOR</code> .</span><span class="sxs-lookup"><span data-stu-id="281e0-113">Multiply an instance of <code>XMVECTOR</code> by a floating point value, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="281e0-114">Le <code>operator \*</code> multiplie chaque composant d’une instance de <a href="xmvector-data-type.md"><strong>type de données XMVECTOR</strong></a> par une valeur à virgule flottante, en retournant une nouvelle <code>XMVECTOR</code> instance dont les composants contiennent le résultat.</span><span class="sxs-lookup"><span data-stu-id="281e0-114">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a floating point value, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="281e0-115">Cet opérateur est uniquement disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="281e0-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="281e0-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR :: Operator \* (XMVECTOR, XMVECTOR)</strong></a></span><span class="sxs-lookup"><span data-stu-id="281e0-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="281e0-117">Multiplie une instance de <code>XMVECTOR</code> par une deuxième instance, en retournant le résultat dans une troisième instance.</span><span class="sxs-lookup"><span data-stu-id="281e0-117">Multiplies one instance of <code>XMVECTOR</code> by a second instance, returning the result in a third instance.</span></span> <br/> <span data-ttu-id="281e0-118">Le <code>operator \*</code> multiplie chaque composant d’une instance de <a href="xmvector-data-type.md"><strong>type de données XMVECTOR</strong></a> par le composant correspondant dans une deuxième instance de <code>XMVECTOR</code> , en retournant une nouvelle <code>XMVECTOR</code> instance contenant le résultat.</span><span class="sxs-lookup"><span data-stu-id="281e0-118">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second instance of <code>XMVECTOR</code>, returning a new <code>XMVECTOR</code> instance containing the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="281e0-119">Cet opérateur est uniquement disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="281e0-119">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="281e0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="281e0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="281e0-121">XMVECTOR, opérateurs</span><span class="sxs-lookup"><span data-stu-id="281e0-121">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="281e0-122">**Référence**</span><span class="sxs-lookup"><span data-stu-id="281e0-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="281e0-123">**Type de données XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="281e0-123">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
