---
title: Routine de _aulldiv
description: Divise deux entiers ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _aulldiv, ntoskrnl.exe!_aulldiv
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _aulldiv
targetos: Windows
ms.openlocfilehash: 2fce346ee9608f20667c76841a63a8a3fb9cfe21
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104462687"
---
# <a name="_aulldiv-routine"></a><span data-ttu-id="9b16d-103">\_Routine aulldiv</span><span class="sxs-lookup"><span data-stu-id="9b16d-103">\_aulldiv Routine</span></span>

<span data-ttu-id="9b16d-104">Divise deux entiers **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="9b16d-104">Divides two **ULONGLONG** integers.</span></span>
<span data-ttu-id="9b16d-105">Par exemple, pour diviser deux valeurs UInt64, le compilateur peut générer un appel à la routine **\_ aulldiv** .</span><span class="sxs-lookup"><span data-stu-id="9b16d-105">For example, to divide two uint64 values the compiler might generate a call to the **\_aulldiv** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b16d-106">Notes</span><span class="sxs-lookup"><span data-stu-id="9b16d-106">Remarks</span></span>

<span data-ttu-id="9b16d-107">La routine **\_ aulldiv** est une routine d’assistance pour le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="9b16d-107">The **\_aulldiv** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="9b16d-108">Le fait que le compilateur utilise **\_ aulldiv** dépend entièrement du jeu d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="9b16d-108">Whether the compiler uses **\_aulldiv** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="9b16d-109">Cette fonction est utilisée uniquement sur les plateformes x86.</span><span class="sxs-lookup"><span data-stu-id="9b16d-109">This function is used only on x86 platforms.</span></span>
