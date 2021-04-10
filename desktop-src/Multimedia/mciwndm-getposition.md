---
title: Message MCIWNDM_GETPOSITION (VFW. h)
description: Le \_ message GETPOSITION MCIWNDM récupère la valeur numérique de la position actuelle dans le contenu de l’appareil MCI.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- Message MCIWNDM_GETPOSITION Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7468b0e3698a72d3dce82bbd1591d59940d9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843193"
---
# <a name="mciwndm_getposition-message"></a><span data-ttu-id="8f980-104">\_Message MCIWNDM GETPOSITION</span><span class="sxs-lookup"><span data-stu-id="8f980-104">MCIWNDM\_GETPOSITION message</span></span>

<span data-ttu-id="8f980-105">Le **message \_ GETPOSITION MCIWNDM** récupère la valeur numérique de la position actuelle dans le contenu de l’appareil MCI.</span><span class="sxs-lookup"><span data-stu-id="8f980-105">The **MCIWNDM\_GETPOSITION** message retrieves the numerical value of the current position within the content of the MCI device.</span></span> <span data-ttu-id="8f980-106">Cette macro fournit également la position actuelle sous forme de chaîne dans une mémoire tampon définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="8f980-106">This macro also provides the current position in string form in an application-defined buffer.</span></span> <span data-ttu-id="8f980-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) ou [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .</span><span class="sxs-lookup"><span data-stu-id="8f980-107">You can send this message explicitly or by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) or [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="8f980-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f980-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f980-109"><span id="len"></span><span id="LEN"></span>*Len*</span><span class="sxs-lookup"><span data-stu-id="8f980-109"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="8f980-110">Taille, en octets, de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="8f980-110">Size, in bytes, of the buffer.</span></span> <span data-ttu-id="8f980-111">Si la chaîne se terminant par un caractère NULL est plus longue que la mémoire tampon, elle est tronquée.</span><span class="sxs-lookup"><span data-stu-id="8f980-111">If the null-terminated string is longer than the buffer, it is truncated.</span></span> <span data-ttu-id="8f980-112">Utilisez zéro pour empêcher la récupération de la position comme une chaîne.</span><span class="sxs-lookup"><span data-stu-id="8f980-112">Use zero to inhibit retrieval of the position as a string.</span></span>

</dd> <dt>

<span data-ttu-id="8f980-113"><span id="lp"></span><span id="LP"></span>*Aid*</span><span class="sxs-lookup"><span data-stu-id="8f980-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="8f980-114">Pointeur vers une mémoire tampon définie par l’application utilisée pour retourner la position.</span><span class="sxs-lookup"><span data-stu-id="8f980-114">Pointer to an application-defined buffer used to return the position.</span></span> <span data-ttu-id="8f980-115">Utilisez zéro pour empêcher la récupération de la position comme une chaîne.</span><span class="sxs-lookup"><span data-stu-id="8f980-115">Use zero to inhibit retrieval of the position as a string.</span></span> <span data-ttu-id="8f980-116">Si l’appareil prend en charge les suivis, les informations de position de la chaîne sont retournées sous la forme TT : MM : SS : FF où TT correspond aux suivis, MM et SS correspondent aux minutes et aux secondes, et FF correspond aux frames.</span><span class="sxs-lookup"><span data-stu-id="8f980-116">If the device supports tracks, the string position information is returned in the form TT:MM:SS:FF where TT corresponds to tracks, MM and SS correspond to minutes and seconds, and FF corresponds to frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f980-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8f980-117">Return Value</span></span>

<span data-ttu-id="8f980-118">Retourne un entier correspondant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="8f980-118">Returns an integer corresponding to the current position.</span></span> <span data-ttu-id="8f980-119">Les unités pour la valeur de position dépendent du format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="8f980-119">The units for the position value depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f980-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f980-120">Requirements</span></span>



| <span data-ttu-id="8f980-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f980-121">Requirement</span></span> | <span data-ttu-id="8f980-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f980-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8f980-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f980-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8f980-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f980-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8f980-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f980-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8f980-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f980-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8f980-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f980-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f980-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f980-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f980-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f980-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f980-130">**MCIWndGetPosition**</span><span class="sxs-lookup"><span data-stu-id="8f980-130">**MCIWndGetPosition**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[<span data-ttu-id="8f980-131">**MCIWndGetPositionString**</span><span class="sxs-lookup"><span data-stu-id="8f980-131">**MCIWndGetPositionString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





