---
title: Routine de _allmul
description: Multiplie deux entiers LONGLONG ou ULONGLONG.
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104030717"
---
# <a name="_allmul-routine"></a><span data-ttu-id="f8496-103">\_Routine allmul</span><span class="sxs-lookup"><span data-stu-id="f8496-103">\_allmul Routine</span></span>

<span data-ttu-id="f8496-104">Multiplie deux entiers **LongLong** ou **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="f8496-104">Multiplies two **LONGLONG** or **ULONGLONG** integers.</span></span>
<span data-ttu-id="f8496-105">Par exemple, pour multiplier deux valeurs Int64, le compilateur peut générer un appel à la routine **\_ allmul** .</span><span class="sxs-lookup"><span data-stu-id="f8496-105">For example, to multiply two int64 values the compiler might generate a call to the **\_allmul** routine.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8496-106">Notes</span><span class="sxs-lookup"><span data-stu-id="f8496-106">Remarks</span></span>

<span data-ttu-id="f8496-107">La routine **\_ allmul** est une routine d’assistance pour le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="f8496-107">The **\_allmul** routine is a helper routine for the C compiler.</span></span>
<span data-ttu-id="f8496-108">Le fait que le compilateur utilise **\_ allmul** dépend entièrement du jeu d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="f8496-108">Whether the compiler uses **\_allmul** is completely dependent on the optimization set.</span></span>

<span data-ttu-id="f8496-109">Cette routine est utilisée uniquement sur les plateformes x86.</span><span class="sxs-lookup"><span data-stu-id="f8496-109">This routine is used only on x86 platforms.</span></span>
