---
title: Message LVM_GETISEARCHSTRING (commctrl. h)
description: Récupère la chaîne de recherche incrémentielle d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetISearchString.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- LVM_GETISEARCHSTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETISEARCHSTRING
- LVM_GETISEARCHSTRINGA
- LVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9040cf96c5c483b29764b1ccfb67e0e4fff3f897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466514"
---
# <a name="lvm_getisearchstring-message"></a><span data-ttu-id="7f650-105">\_Message GETISEARCHSTRING LVM</span><span class="sxs-lookup"><span data-stu-id="7f650-105">LVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="7f650-106">Récupère la chaîne de recherche incrémentielle d’un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="7f650-106">Retrieves the incremental search string of a list-view control.</span></span> <span data-ttu-id="7f650-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) .</span><span class="sxs-lookup"><span data-stu-id="7f650-107">You can send this message explicitly or by using the [**ListView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f650-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f650-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f650-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f650-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7f650-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="7f650-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7f650-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f650-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f650-112">Pointeur vers une mémoire tampon qui reçoit la chaîne de recherche incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="7f650-112">Pointer to a buffer that receives the incremental search string.</span></span> <span data-ttu-id="7f650-113">Pour récupérer uniquement la longueur de la chaîne, affectez à *lParam* la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7f650-113">To just retrieve the length of the string, set *lParam* to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f650-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f650-114">Return value</span></span>

<span data-ttu-id="7f650-115">Retourne le nombre de caractères de la chaîne de recherche incrémentielle, à l’exclusion du caractère NULL de fin, ou zéro si le contrôle de liste n’est pas en mode de recherche incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="7f650-115">Returns the number of characters in the incremental search string, not including the terminating NULL character, or zero if the list-view control is not in incremental search mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f650-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7f650-116">Remarks</span></span>

<span data-ttu-id="7f650-117">**Avertissement de sécurité :** L’utilisation incorrecte de ce message peut compromettre la sécurité de votre programme.</span><span class="sxs-lookup"><span data-stu-id="7f650-117">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="7f650-118">Ce message n’offre aucun moyen de connaître la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7f650-118">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="7f650-119">Si vous utilisez ce message, appelez tout d’abord le message qui passe **null** dans *lParam*, ce qui renvoie le nombre de caractères, à l’exception de la **valeur null** requise.</span><span class="sxs-lookup"><span data-stu-id="7f650-119">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="7f650-120">Ensuite, appelez le message une seconde fois pour récupérer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="7f650-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="7f650-121">Vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="7f650-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="7f650-122">La *chaîne de recherche incrémentielle* correspond à la séquence de caractères que l’utilisateur tape lorsque l’affichage de liste a le focus d’entrée.</span><span class="sxs-lookup"><span data-stu-id="7f650-122">The *incremental search string* is the character sequence that the user types while the list view has the input focus.</span></span> <span data-ttu-id="7f650-123">Chaque fois que l’utilisateur tape un caractère, le système ajoute le caractère à la chaîne de recherche, puis recherche un élément correspondant.</span><span class="sxs-lookup"><span data-stu-id="7f650-123">Each time the user types a character, the system appends the character to the search string and then searches for a matching item.</span></span> <span data-ttu-id="7f650-124">Si le système trouve une correspondance, il sélectionne l’élément et, si nécessaire, le fait défiler dans la vue.</span><span class="sxs-lookup"><span data-stu-id="7f650-124">If the system finds a match, it selects the item and, if necessary, scrolls it into view.</span></span>

<span data-ttu-id="7f650-125">Un délai d’attente est associé à chaque caractère que l’utilisateur tape.</span><span class="sxs-lookup"><span data-stu-id="7f650-125">A time-out period is associated with each character that the user types.</span></span> <span data-ttu-id="7f650-126">Si le délai d’attente s’écoule avant que l’utilisateur ne tape un autre caractère, la chaîne de recherche incrémentielle est réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="7f650-126">If the time-out period elapses before the user types another character, the incremental search string is reset.</span></span>

<span data-ttu-id="7f650-127">Assurez-vous que la mémoire tampon est suffisamment grande pour contenir la chaîne et le caractère NULL de fin.</span><span class="sxs-lookup"><span data-stu-id="7f650-127">Make sure that the buffer is large enough to hold the string and the terminating NULL character.</span></span> <span data-ttu-id="7f650-128">S’il est trop petit, une erreur de page non valide est générée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="7f650-128">If it is too small, an immediate invalid page fault will result.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f650-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f650-129">Requirements</span></span>



| <span data-ttu-id="7f650-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f650-130">Requirement</span></span> | <span data-ttu-id="7f650-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f650-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f650-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f650-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7f650-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f650-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7f650-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f650-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7f650-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f650-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f650-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f650-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f650-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f650-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7f650-138">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="7f650-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7f650-139">**LVM \_ GETISEARCHSTRINGW** (Unicode) et **LVM \_ GETISEARCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7f650-139">**LVM\_GETISEARCHSTRINGW** (Unicode) and **LVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





