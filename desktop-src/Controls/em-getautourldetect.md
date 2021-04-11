---
title: Message EM_GETAUTOURLDETECT (RichEdit. h)
description: Indique si la détection d’URL automatique est activée dans le contrôle Rich Edit.
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- EM_GETAUTOURLDETECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e68e4f2991c5f8780cb587594289674e07ec992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032945"
---
# <a name="em_getautourldetect-message"></a><span data-ttu-id="98397-104">\_Message GETAUTOURLDETECT em</span><span class="sxs-lookup"><span data-stu-id="98397-104">EM\_GETAUTOURLDETECT message</span></span>

<span data-ttu-id="98397-105">Indique si la détection d’URL automatique est activée dans le contrôle Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="98397-105">Indicates whether the auto URL detection is turned on in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="98397-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98397-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98397-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98397-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98397-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="98397-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="98397-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98397-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98397-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="98397-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98397-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98397-111">Return value</span></span>

<span data-ttu-id="98397-112">Si la détection d’URL automatique est active, la valeur de retour est 1.</span><span class="sxs-lookup"><span data-stu-id="98397-112">If auto-URL detection is active, the return value is 1.</span></span>

<span data-ttu-id="98397-113">Si la détection d’URL automatique est inactive, la valeur de retour est 0.</span><span class="sxs-lookup"><span data-stu-id="98397-113">If auto-URL detection is inactive, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="98397-114">Notes</span><span class="sxs-lookup"><span data-stu-id="98397-114">Remarks</span></span>

<span data-ttu-id="98397-115">Lorsque la détection d’URL automatique est activée, la modification riche de Microsoft vérifie constamment le texte tapé pour une URL valide.</span><span class="sxs-lookup"><span data-stu-id="98397-115">When auto URL detection is on, Microsoft Rich Edit is constantly checking typed text for a valid URL.</span></span> <span data-ttu-id="98397-116">La modification complète reconnaît les URL qui commencent par ces préfixes :</span><span class="sxs-lookup"><span data-stu-id="98397-116">Rich Edit recognizes URLs that start with these prefixes:</span></span>

-   <span data-ttu-id="98397-117">http:</span><span class="sxs-lookup"><span data-stu-id="98397-117">http:</span></span>
-   <span data-ttu-id="98397-118">file :</span><span class="sxs-lookup"><span data-stu-id="98397-118">file:</span></span>
-   <span data-ttu-id="98397-119">mailto:</span><span class="sxs-lookup"><span data-stu-id="98397-119">mailto:</span></span>
-   <span data-ttu-id="98397-120">FTP</span><span class="sxs-lookup"><span data-stu-id="98397-120">ftp:</span></span>
-   <span data-ttu-id="98397-121">https</span><span class="sxs-lookup"><span data-stu-id="98397-121">https:</span></span>
-   <span data-ttu-id="98397-122">Gopher</span><span class="sxs-lookup"><span data-stu-id="98397-122">gopher:</span></span>
-   <span data-ttu-id="98397-123">NNTP</span><span class="sxs-lookup"><span data-stu-id="98397-123">nntp:</span></span>
-   <span data-ttu-id="98397-124">prospero:</span><span class="sxs-lookup"><span data-stu-id="98397-124">prospero:</span></span>
-   <span data-ttu-id="98397-125">Mission</span><span class="sxs-lookup"><span data-stu-id="98397-125">telnet:</span></span>
-   <span data-ttu-id="98397-126">concernant</span><span class="sxs-lookup"><span data-stu-id="98397-126">news:</span></span>
-   <span data-ttu-id="98397-127">WAIS</span><span class="sxs-lookup"><span data-stu-id="98397-127">wais:</span></span>
-   <span data-ttu-id="98397-128">programme</span><span class="sxs-lookup"><span data-stu-id="98397-128">outlook:</span></span>

<span data-ttu-id="98397-129">La modification complète reconnaît également les noms de chemins standard qui commencent par \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="98397-129">Rich Edit also recognizes standard path names that start with \\\\.</span></span> <span data-ttu-id="98397-130">Quand la modification complète localise une URL, elle modifie la couleur du texte de l’URL, souligne le texte et notifie le client à l’aide de l' [ \_ éditeur de liens](en-link.md).</span><span class="sxs-lookup"><span data-stu-id="98397-130">When Rich Edit locates a URL, it changes the URL text color, underlines the text, and notifies the client using [EN\_LINK](en-link.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98397-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98397-131">Requirements</span></span>



| <span data-ttu-id="98397-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98397-132">Requirement</span></span> | <span data-ttu-id="98397-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="98397-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98397-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98397-134">Minimum supported client</span></span><br/> | <span data-ttu-id="98397-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98397-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="98397-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98397-136">Minimum supported server</span></span><br/> | <span data-ttu-id="98397-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="98397-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="98397-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="98397-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="98397-139"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="98397-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98397-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98397-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98397-141">en \_ lien</span><span class="sxs-lookup"><span data-stu-id="98397-141">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 

 





