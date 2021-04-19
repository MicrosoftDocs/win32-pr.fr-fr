---
description: Le type de données LARGEINT définit une \_ valeur entière de type long.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: LARGEINT (NetMon. h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d857179e97586974e11815ced5ec7c50ca276789
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106517336"
---
# <a name="largeint"></a><span data-ttu-id="e030b-103">LARGEINT</span><span class="sxs-lookup"><span data-stu-id="e030b-103">LARGEINT</span></span>

<span data-ttu-id="e030b-104">Le type de données **LARGEINT** définit une valeur [**entière de \_ type long**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) .</span><span class="sxs-lookup"><span data-stu-id="e030b-104">The **LARGEINT** datatype defines a [**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) value.</span></span>


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a><span data-ttu-id="e030b-105">Notes</span><span class="sxs-lookup"><span data-stu-id="e030b-105">Remarks</span></span>

<span data-ttu-id="e030b-106">Le membre **lpLargeIntTable** de la structure [**Set**](set.md) pointe vers un tableau de structures d' **ensemble** qui définissent une ou plusieurs valeurs LARGEINT.</span><span class="sxs-lookup"><span data-stu-id="e030b-106">The **lpLargeIntTable** member of the [**SET**](set.md) structure points to an array of **SET** structures that define one or more LARGEINT values.</span></span> <span data-ttu-id="e030b-107">Lorsque ce type de structure de **jeu** est spécifié, moniteur réseau affiche l’une des étiquettes suivantes avec chaque valeur LARGEINT trouvée dans le paquet de protocole.</span><span class="sxs-lookup"><span data-stu-id="e030b-107">When this type of **SET** structure is specified, Network Monitor displays one of the following labels with each LARGEINT value that it finds in the protocol packet.</span></span>

-   <span data-ttu-id="e030b-108">Correspond à la valeur définie.</span><span class="sxs-lookup"><span data-stu-id="e030b-108">Matches set value.</span></span> <span data-ttu-id="e030b-109">La valeur LARGEINT est incluse dans le jeu.</span><span class="sxs-lookup"><span data-stu-id="e030b-109">The LARGEINT value is included in the set.</span></span>
-   <span data-ttu-id="e030b-110">Valeur définie inconnue.</span><span class="sxs-lookup"><span data-stu-id="e030b-110">Unknown set value.</span></span> <span data-ttu-id="e030b-111">La valeur LARGEINT n’est pas incluse dans le jeu.</span><span class="sxs-lookup"><span data-stu-id="e030b-111">The LARGEINT value is not included in the set.</span></span>

## <a name="requirements"></a><span data-ttu-id="e030b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e030b-112">Requirements</span></span>



| <span data-ttu-id="e030b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e030b-113">Requirement</span></span> | <span data-ttu-id="e030b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e030b-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e030b-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e030b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e030b-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e030b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e030b-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e030b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e030b-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e030b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e030b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="e030b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e030b-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e030b-120"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e030b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e030b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e030b-122">SET</span><span class="sxs-lookup"><span data-stu-id="e030b-122">SET</span></span>](set.md)
</dt> </dl>

 

