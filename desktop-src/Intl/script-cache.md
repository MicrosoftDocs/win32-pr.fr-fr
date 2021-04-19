---
description: Définit un cache de métriques de police Uniscribe.
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: SCRIPT_CACHE (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527689"
---
# <a name="script_cache"></a><span data-ttu-id="1054c-103">CACHE de SCRIPT \_</span><span class="sxs-lookup"><span data-stu-id="1054c-103">SCRIPT\_CACHE</span></span>

<span data-ttu-id="1054c-104">Définit un cache de métriques de police Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="1054c-104">Defines a Uniscribe font metric cache.</span></span>


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a><span data-ttu-id="1054c-105">Notes</span><span class="sxs-lookup"><span data-stu-id="1054c-105">Remarks</span></span>

<span data-ttu-id="1054c-106">Il s’agit d’une structure opaque.</span><span class="sxs-lookup"><span data-stu-id="1054c-106">This is an opaque structure.</span></span> <span data-ttu-id="1054c-107">L’application doit allouer et conserver une \_ variable de cache de script pour chaque style de caractère utilisé.</span><span class="sxs-lookup"><span data-stu-id="1054c-107">The application must allocate and retain one SCRIPT\_CACHE variable for each character style used.</span></span> <span data-ttu-id="1054c-108">La variable doit être initialisée avec la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1054c-108">The variable must be initialized to **NULL**.</span></span>

<span data-ttu-id="1054c-109">De nombreuses fonctions de script prennent une combinaison d’un handle de contexte de périphérique matériel et d’une variable de cache de SCRIPT \_ .</span><span class="sxs-lookup"><span data-stu-id="1054c-109">Many script functions take a combination of a hardware device context handle and a SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="1054c-110">Uniscribe tente d’abord d’accéder aux données de police à l’aide de la \_ variable cache de script.</span><span class="sxs-lookup"><span data-stu-id="1054c-110">Uniscribe first attempts to access font data by using the SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="1054c-111">Il inspecte uniquement le contexte de périphérique matériel si les données requises ne sont pas déjà mises en cache.</span><span class="sxs-lookup"><span data-stu-id="1054c-111">It only inspects the hardware device context if the required data is not already cached.</span></span>

<span data-ttu-id="1054c-112">Le descripteur de contexte de périphérique matériel peut être passé à Uniscribe en tant que **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1054c-112">The hardware device context handle can be passed to Uniscribe as **NULL**.</span></span> <span data-ttu-id="1054c-113">Si les données requises par Uniscribe sont déjà mises en cache, le contexte de périphérique n’est pas accessible et l’opération se poursuit normalement.</span><span class="sxs-lookup"><span data-stu-id="1054c-113">If data required by Uniscribe is already cached, the device context is not accessed, and the operation continues normally.</span></span>

<span data-ttu-id="1054c-114">Si le contexte de périphérique est passé comme **null** et que Uniscribe doit y accéder pour une raison quelconque, Uniscribe retourne le code d’erreur E \_ en attente.</span><span class="sxs-lookup"><span data-stu-id="1054c-114">If the device context is passed as **NULL** and Uniscribe needs to access it for any reason, Uniscribe returns the error code E\_PENDING.</span></span> <span data-ttu-id="1054c-115">Ce code est retourné rapidement, ce qui permet à l’application d’éviter les appels [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) fastidieux.</span><span class="sxs-lookup"><span data-stu-id="1054c-115">This code is returned quickly, allowing the application to avoid time-consuming [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) calls.</span></span>

## <a name="examples"></a><span data-ttu-id="1054c-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="1054c-116">Examples</span></span>

<span data-ttu-id="1054c-117">L’exemple suivant s’applique à toutes les fonctions qui prennent une variable de cache de SCRIPT \_ et un handle facultatif à un contexte de périphérique matériel.</span><span class="sxs-lookup"><span data-stu-id="1054c-117">The following example applies to all functions that take a SCRIPT\_CACHE variable and an optional handle to a hardware device context.</span></span>


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a><span data-ttu-id="1054c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1054c-118">Requirements</span></span>



| <span data-ttu-id="1054c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1054c-119">Requirement</span></span> | <span data-ttu-id="1054c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1054c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1054c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1054c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1054c-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1054c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1054c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1054c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1054c-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1054c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1054c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="1054c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1054c-126"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1054c-126"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1054c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1054c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1054c-128">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="1054c-128">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="1054c-129">Structures Uniscribe</span><span class="sxs-lookup"><span data-stu-id="1054c-129">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="1054c-130">Mise en cache</span><span class="sxs-lookup"><span data-stu-id="1054c-130">Caching</span></span>](caching.md)
</dt> </dl>

 

 
