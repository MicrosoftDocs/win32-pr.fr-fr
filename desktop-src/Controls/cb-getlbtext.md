---
title: Message CB_GETLBTEXT (winuser. h)
description: Obtient une chaîne à partir de la liste d’une zone de liste déroulante.
ms.assetid: f84e302a-65bb-45c8-958b-1cb438fb5a7a
keywords:
- CB_GETLBTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETLBTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d26a964b463daedab1ad5d9f50888b3e0c1e0db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032853"
---
# <a name="cb_getlbtext-message"></a><span data-ttu-id="5e8c2-104">\_Message GETLBTEXT CB</span><span class="sxs-lookup"><span data-stu-id="5e8c2-104">CB\_GETLBTEXT message</span></span>

<span data-ttu-id="5e8c2-105">Obtient une chaîne à partir de la liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="5e8c2-105">Gets a string from the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e8c2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e8c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e8c2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e8c2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e8c2-108">Index de base zéro de la chaîne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="5e8c2-108">The zero-based index of the string to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="5e8c2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e8c2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e8c2-110">Pointeur vers la mémoire tampon qui reçoit la chaîne.</span><span class="sxs-lookup"><span data-stu-id="5e8c2-110">A pointer to the buffer that receives the string.</span></span> <span data-ttu-id="5e8c2-111">La mémoire tampon doit avoir suffisamment d’espace pour la chaîne et un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="5e8c2-111">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="5e8c2-112">Vous pouvez envoyer un message [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) avant le message **\_ GETLBTEXT CB** pour récupérer la longueur, dans **TCHAR** s, de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="5e8c2-112">You can send a [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) message prior to the **CB\_GETLBTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span> <span data-ttu-id="5e8c2-113">S’il s’agit d’une chaîne ANSI, il s’agit du nombre d’octets, mais s’il s’agit d’une chaîne Unicode, il s’agit du nombre de caractères.</span><span class="sxs-lookup"><span data-stu-id="5e8c2-113">If it is an ANSI string this is the number of bytes, but if it is a Unicode string this is the number of characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e8c2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e8c2-114">Return value</span></span>

<span data-ttu-id="5e8c2-115">La valeur de retour est la longueur de la chaîne, dans **TCHAR** s, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="5e8c2-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="5e8c2-116">Si *wParam* ne spécifie pas d’index valide, la valeur de retour est CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="5e8c2-116">If *wParam* does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e8c2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5e8c2-117">Remarks</span></span>

<span data-ttu-id="5e8c2-118">**Avertissement de sécurité :** L’utilisation incorrecte de ce message peut compromettre la sécurité de votre programme.</span><span class="sxs-lookup"><span data-stu-id="5e8c2-118">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="5e8c2-119">Ce message n’offre aucun moyen de connaître la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5e8c2-119">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="5e8c2-120">Si vous utilisez ce message, appelez d’abord [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) pour obtenir le nombre de caractères requis, puis appelez le message pour récupérer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="5e8c2-120">If you use this message, first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="5e8c2-121">Vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="5e8c2-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="5e8c2-122">Si vous créez la zone de liste déroulante avec un style owner-drawn mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , la mémoire tampon vers laquelle pointe *lParam* reçoit les données associées à l’élément.</span><span class="sxs-lookup"><span data-stu-id="5e8c2-122">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the buffer pointed to by *lParam* receives the data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e8c2-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e8c2-123">Requirements</span></span>



| <span data-ttu-id="5e8c2-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e8c2-124">Requirement</span></span> | <span data-ttu-id="5e8c2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e8c2-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e8c2-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e8c2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5e8c2-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e8c2-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5e8c2-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e8c2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5e8c2-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e8c2-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5e8c2-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e8c2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e8c2-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e8c2-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e8c2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e8c2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e8c2-133">**\_GETLBTEXTLEN CB**</span><span class="sxs-lookup"><span data-stu-id="5e8c2-133">**CB\_GETLBTEXTLEN**</span></span>](cb-getlbtextlen.md)
</dt> </dl>

 

 





