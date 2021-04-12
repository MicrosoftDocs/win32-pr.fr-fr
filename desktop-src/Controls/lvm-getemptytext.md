---
title: Message LVM_GETEMPTYTEXT (commctrl. h)
description: Obtient le texte à afficher lorsque le contrôle de liste s’affiche vide. Envoyez ce message explicitement ou à l’aide de la \_ macro ListView GetEmptyText.
ms.assetid: aa6cb0ae-0c6c-42b7-80c5-c086c9579c81
keywords:
- LVM_GETEMPTYTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- LVM_GETEMPTYTEXT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7549081ef7f158a6a6a061bcee9669ea62d52f68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464275"
---
# <a name="lvm_getemptytext-message"></a><span data-ttu-id="e3103-105">\_Message GETEMPTYTEXT LVM</span><span class="sxs-lookup"><span data-stu-id="e3103-105">LVM\_GETEMPTYTEXT message</span></span>

<span data-ttu-id="e3103-106">Obtient le texte à afficher lorsque le contrôle de liste s’affiche vide.</span><span class="sxs-lookup"><span data-stu-id="e3103-106">Gets the text meant for display when the list-view control appears empty.</span></span> <span data-ttu-id="e3103-107">Envoyez ce message explicitement ou à l’aide de la macro [**ListView \_ GetEmptyText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) .</span><span class="sxs-lookup"><span data-stu-id="e3103-107">Send this message explicitly or by using the [**ListView\_GetEmptyText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getemptytext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e3103-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3103-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3103-109">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e3103-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3103-110">Taille de la mémoire tampon vers laquelle pointe *lParam*, y compris le caractère **null** de fin.</span><span class="sxs-lookup"><span data-stu-id="e3103-110">The size of the buffer pointed to by *lParam*, including the terminating **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e3103-111">*lParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e3103-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3103-112">Pointeur vers une mémoire tampon Unicode, terminée par un caractère null, de taille spécifiée par *wParam* pour recevoir le texte.</span><span class="sxs-lookup"><span data-stu-id="e3103-112">A pointer to a null-terminated, Unicode buffer of size specified by *wParam* to receive the text.</span></span> <span data-ttu-id="e3103-113">L’appelant est chargé d’allouer la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e3103-113">The caller is responsible for allocating the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3103-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3103-114">Return value</span></span>

<span data-ttu-id="e3103-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e3103-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3103-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3103-116">Requirements</span></span>



| <span data-ttu-id="e3103-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3103-117">Requirement</span></span> | <span data-ttu-id="e3103-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3103-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3103-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3103-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e3103-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3103-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e3103-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3103-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e3103-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3103-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e3103-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3103-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3103-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3103-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





