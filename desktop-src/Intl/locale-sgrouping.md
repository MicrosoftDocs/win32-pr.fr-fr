---
description: paramètres régionaux \_ SGROUPING
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7242f7d515ce17872376b9a067a7b41831a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953255"
---
# <a name="locale_sgrouping"></a><span data-ttu-id="dc601-103">paramètres régionaux \_ SGROUPING</span><span class="sxs-lookup"><span data-stu-id="dc601-103">LOCALE\_SGROUPING</span></span>

<span data-ttu-id="dc601-104">Tailles pour chaque groupe de chiffres à gauche du séparateur décimal.</span><span class="sxs-lookup"><span data-stu-id="dc601-104">Sizes for each group of digits to the left of the decimal.</span></span> <span data-ttu-id="dc601-105">Le nombre maximal de caractères autorisés pour cette chaîne est dix, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="dc601-105">The maximum number of characters allowed for this string is ten, including a terminating null character.</span></span> <span data-ttu-id="dc601-106">Une taille explicite est nécessaire pour chaque groupe, et les tailles sont séparées par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="dc601-106">An explicit size is needed for each group, and sizes are separated by semicolons.</span></span> <span data-ttu-id="dc601-107">Si la dernière valeur est égale à 0, la valeur précédente est répétée.</span><span class="sxs-lookup"><span data-stu-id="dc601-107">If the last value is 0, the preceding value is repeated.</span></span> <span data-ttu-id="dc601-108">Par exemple, pour regrouper des milliers, spécifiez 3 ; 0.</span><span class="sxs-lookup"><span data-stu-id="dc601-108">For example, to group thousands, specify 3;0.</span></span> <span data-ttu-id="dc601-109">Les paramètres régionaux indo-aryens groupent les premiers mille, puis regroupent par centaines.</span><span class="sxs-lookup"><span data-stu-id="dc601-109">Indic locales group the first thousand and then group by hundreds.</span></span> <span data-ttu-id="dc601-110">Par exemple, 12, 34, 56789 est représenté par 3 ; 2 ; 0.</span><span class="sxs-lookup"><span data-stu-id="dc601-110">For example, 12,34,56,789 is represented by 3;2;0.</span></span>

<span data-ttu-id="dc601-111">Autres exemples :</span><span class="sxs-lookup"><span data-stu-id="dc601-111">Further examples:</span></span>



| <span data-ttu-id="dc601-112">Caractéristique</span><span class="sxs-lookup"><span data-stu-id="dc601-112">Specification</span></span> | <span data-ttu-id="dc601-113">Chaîne résultante</span><span class="sxs-lookup"><span data-stu-id="dc601-113">Resulting string</span></span>   |
|---------------|--------------------|
| <span data-ttu-id="dc601-114">3 ; 0</span><span class="sxs-lookup"><span data-stu-id="dc601-114">3;0</span></span>           | <span data-ttu-id="dc601-115">3 000 000 000 000</span><span class="sxs-lookup"><span data-stu-id="dc601-115">3,000,000,000,000</span></span>  |
| <span data-ttu-id="dc601-116">3 ; 2 ; 0</span><span class="sxs-lookup"><span data-stu-id="dc601-116">3;2;0</span></span>         | <span data-ttu-id="dc601-117">30, 00, 00, 00, 00000</span><span class="sxs-lookup"><span data-stu-id="dc601-117">30,00,00,00,00,000</span></span> |
| <span data-ttu-id="dc601-118">3</span><span class="sxs-lookup"><span data-stu-id="dc601-118">3</span></span>             | <span data-ttu-id="dc601-119">3 000 000 000 000</span><span class="sxs-lookup"><span data-stu-id="dc601-119">3000000000,000</span></span>     |
| <span data-ttu-id="dc601-120">3 ; 2</span><span class="sxs-lookup"><span data-stu-id="dc601-120">3;2</span></span>           | <span data-ttu-id="dc601-121">30000000, 00000</span><span class="sxs-lookup"><span data-stu-id="dc601-121">30000000,00,000</span></span>    |



 

 

 



