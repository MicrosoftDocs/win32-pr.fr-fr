---
description: Définit les unités de nanosecondes de 100.
ms.assetid: 9273ff1f-382e-4c58-b571-4852545915b3
title: MFTIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e82c99c3c4a42b652c04595d086951c3c1a71a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521604"
---
# <a name="mftime"></a><span data-ttu-id="d882e-103">MFTIME</span><span class="sxs-lookup"><span data-stu-id="d882e-103">MFTIME</span></span>

<span data-ttu-id="d882e-104">Définit les unités de nanosecondes de 100.</span><span class="sxs-lookup"><span data-stu-id="d882e-104">Defines units of 100 nanoseconds.</span></span>


```C++
typedef LONGLONG MFTIME;
```



## <a name="examples"></a><span data-ttu-id="d882e-105">Exemples</span><span class="sxs-lookup"><span data-stu-id="d882e-105">Examples</span></span>


```C++
const MFTIME ONE_SECOND = 10000000; // One second.
const LONG   ONE_MSEC = 1000;       // One millisecond

// Convert 100-nanosecond units to milliseconds.

inline LONG MFTimeToMsec(const LONGLONG& time)
{
    return (LONG)(time / (ONE_SECOND / ONE_MSEC));
}
```



## <a name="requirements"></a><span data-ttu-id="d882e-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d882e-106">Requirements</span></span>



| <span data-ttu-id="d882e-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d882e-107">Requirement</span></span> | <span data-ttu-id="d882e-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d882e-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d882e-109">En-tête</span><span class="sxs-lookup"><span data-stu-id="d882e-109">Header</span></span><br/> | <dl> <span data-ttu-id="d882e-110"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d882e-110"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d882e-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d882e-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d882e-112">Types de données Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d882e-112">Media Foundation Datatypes</span></span>](media-foundation-datatypes.md)
</dt> </dl>

 

 




