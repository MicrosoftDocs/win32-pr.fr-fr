---
description: Les opérateurs suivants sont exposés par la structure XMVECTOR.
ms.assetid: 16fc1276-7bed-4e6f-8af5-d871afa73b68
title: XMVECTOR, opérateurs
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0611be5e9737e2829bc06f9a3fade10db233cbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517593"
---
# <a name="xmvector-operators"></a><span data-ttu-id="907b5-103">XMVECTOR, opérateurs</span><span class="sxs-lookup"><span data-stu-id="907b5-103">XMVECTOR Operators</span></span>

<span data-ttu-id="907b5-104">Les opérateurs suivants sont exposés par la structure [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="907b5-104">The following operators are exposed by the [**XMVECTOR**](xmvector-data-type.md) structure.</span></span>

> [!Note]  
> <span data-ttu-id="907b5-105">Les opérateurs répertoriés ici sont uniquement disponibles en C++.</span><span class="sxs-lookup"><span data-stu-id="907b5-105">The operators listed here are only available under C++.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="907b5-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="907b5-106">In this section</span></span>



| <span data-ttu-id="907b5-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="907b5-107">Methods</span></span>                                                    | <span data-ttu-id="907b5-108">Description</span><span class="sxs-lookup"><span data-stu-id="907b5-108">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="907b5-109">[**opérateur + =**](/previous-versions/windows/desktop/legacy/ee421394(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="907b5-109">[**operator +=**](/previous-versions/windows/desktop/legacy/ee421394(v=vs.85))</span></span><br/>  | <span data-ttu-id="907b5-110">Ajoute une valeur à virgule flottante à une `XMVECTOR` instance et retourne une référence à l’instance mise à jour.</span><span class="sxs-lookup"><span data-stu-id="907b5-110">Adds a floating point value to an `XMVECTOR` instance, and returns a reference to the updated instance.</span></span> <br/>                         |
| <span data-ttu-id="907b5-111">[**opérateur =**](/previous-versions/windows/desktop/legacy/ee421383(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="907b5-111">[**operator -=**](/previous-versions/windows/desktop/legacy/ee421383(v=vs.85))</span></span><br/>    | <span data-ttu-id="907b5-112">Soustrait une valeur à virgule flottante de l’instance actuelle de `XMVECTOR` , en retournant le résultat dans l’instance actuelle mise à jour.</span><span class="sxs-lookup"><span data-stu-id="907b5-112">Subtracts a floating point value from the current instance of `XMVECTOR`, returning the result in the updated current instance.</span></span> <br/> |
| [<span data-ttu-id="907b5-113">\**opérateur \** _</span><span class="sxs-lookup"><span data-stu-id="907b5-113">\**operator \** _</span></span>](xmvector-operator-mul.md)<br/>    | <span data-ttu-id="907b5-114">Opérateurs de multiplication</span><span class="sxs-lookup"><span data-stu-id="907b5-114">Multiplication operators</span></span><br/>                                                                                                         |
| [<span data-ttu-id="907b5-115">_ *, \* = opérateur*\*</span><span class="sxs-lookup"><span data-stu-id="907b5-115">_ *operator \*=*\*</span></span>](xmvector-operator-muleq.md)<br/> | <span data-ttu-id="907b5-116">Opérateurs d’assignation de multiplication</span><span class="sxs-lookup"><span data-stu-id="907b5-116">Multiplication assignment operators</span></span><br/>                                                                                              |
| [<span data-ttu-id="907b5-117">**and**</span><span class="sxs-lookup"><span data-stu-id="907b5-117">**operator /**</span></span>](xmvector-operator-div.md)<br/>     | <span data-ttu-id="907b5-118">Opérateur de division.</span><span class="sxs-lookup"><span data-stu-id="907b5-118">Division operator.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="907b5-119">**opérateur/=**</span><span class="sxs-lookup"><span data-stu-id="907b5-119">**operator /=**</span></span>](xmvector-operator-diveq.md)<br/>  | <span data-ttu-id="907b5-120">Opérateur d’assignation de division.</span><span class="sxs-lookup"><span data-stu-id="907b5-120">Division Assignment operator.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="907b5-121">**and**</span><span class="sxs-lookup"><span data-stu-id="907b5-121">**operator -**</span></span>](xmvector-operator--.md)<br/>       | <span data-ttu-id="907b5-122">Opérateurs de soustraction et de négation</span><span class="sxs-lookup"><span data-stu-id="907b5-122">Subtraction and negation operators</span></span><br/>                                                                                               |
| [<span data-ttu-id="907b5-123">**opérateur +**</span><span class="sxs-lookup"><span data-stu-id="907b5-123">**operator +**</span></span>](xmvector-operator-pls.md)<br/>     | <span data-ttu-id="907b5-124">Opérateurs d’addition.</span><span class="sxs-lookup"><span data-stu-id="907b5-124">Addition operators.</span></span><br/>                                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="907b5-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="907b5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="907b5-126">Extensions XMVECTOR</span><span class="sxs-lookup"><span data-stu-id="907b5-126">XMVECTOR Extensions</span></span>](ovw-xmvector-extensions.md)
</dt> <dt>

<span data-ttu-id="907b5-127">**Types**</span><span class="sxs-lookup"><span data-stu-id="907b5-127">**Types**</span></span>
</dt> <dt>

[<span data-ttu-id="907b5-128">**Type de données XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="907b5-128">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
