---
title: Message ICM_GETINFO (VFW. h)
description: Le \_ message ICM GETINFO interroge un pilote de compression vidéo pour retourner une description de lui-même dans une structure ICINFO.
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- Message ICM_GETINFO Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634803b7dd9a3b8900c35fabedcadb99908c2b31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511156"
---
# <a name="icm_getinfo-message"></a><span data-ttu-id="3b6c0-104">\_Message ICM GETINFO</span><span class="sxs-lookup"><span data-stu-id="3b6c0-104">ICM\_GETINFO message</span></span>

<span data-ttu-id="3b6c0-105">Le message **ICM \_ GETINFO** interroge un pilote de compression vidéo pour retourner une description de lui-même dans une structure [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) .</span><span class="sxs-lookup"><span data-stu-id="3b6c0-105">The **ICM\_GETINFO** message queries a video compression driver to return a description of itself in an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure.</span></span>


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a><span data-ttu-id="3b6c0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b6c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b6c0-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*</span><span class="sxs-lookup"><span data-stu-id="3b6c0-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*</span></span>
</dt> <dd>

<span data-ttu-id="3b6c0-108">Pointeur vers une structure **ICINFO** pour contenir des informations.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-108">Pointer to an **ICINFO** structure to contain information.</span></span>

</dd> <dt>

<span data-ttu-id="3b6c0-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b6c0-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="3b6c0-110">Taille, en octets, de **ICINFO**.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-110">Size, in bytes, of **ICINFO**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b6c0-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3b6c0-111">Return Value</span></span>

<span data-ttu-id="3b6c0-112">Retourne la taille, en octets, de [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) ou zéro si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-112">Returns the size, in bytes, of [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) or zero if an error occurs..</span></span>

## <a name="remarks"></a><span data-ttu-id="3b6c0-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3b6c0-113">Remarks</span></span>

<span data-ttu-id="3b6c0-114">En règle générale, les applications envoient ce message pour afficher la liste des compresseurs installés.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-114">Typically, applications send this message to display a list of the installed compressors.</span></span>

<span data-ttu-id="3b6c0-115">Le pilote doit remplir tous les membres de la structure [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) , à l’exception de **szDriver**.</span><span class="sxs-lookup"><span data-stu-id="3b6c0-115">The driver should fill all members of the [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure except **szDriver**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b6c0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b6c0-116">Requirements</span></span>



| <span data-ttu-id="3b6c0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b6c0-117">Requirement</span></span> | <span data-ttu-id="3b6c0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b6c0-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3b6c0-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b6c0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3b6c0-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b6c0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3b6c0-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b6c0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3b6c0-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b6c0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3b6c0-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b6c0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b6c0-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b6c0-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b6c0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b6c0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b6c0-126">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="3b6c0-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3b6c0-127">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="3b6c0-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





