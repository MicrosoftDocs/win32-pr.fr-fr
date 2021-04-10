---
title: Message EM_DISPLAYBAND (RichEdit. h)
description: Affiche une partie du contenu d’un contrôle RichEdit, tel qu’il a été précédemment mis en forme pour un appareil à l’aide du \_ message em FormatRange.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- EM_DISPLAYBAND les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51896a9ba5603e799609ab52989681ecf7bcac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942387"
---
# <a name="em_displayband-message"></a><span data-ttu-id="1cc13-104">\_Message DISPLAYBAND em</span><span class="sxs-lookup"><span data-stu-id="1cc13-104">EM\_DISPLAYBAND message</span></span>

<span data-ttu-id="1cc13-105">Affiche une partie du contenu d’un contrôle RichEdit, tel qu’il a été précédemment mis en forme pour un appareil à l’aide du message [**em \_ FormatRange**](em-formatrange.md) .</span><span class="sxs-lookup"><span data-stu-id="1cc13-105">Displays a portion of the contents of a rich edit control, as previously formatted for a device using the [**EM\_FORMATRANGE**](em-formatrange.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="1cc13-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cc13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc13-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1cc13-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cc13-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="1cc13-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1cc13-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1cc13-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cc13-110">Une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) spécifiant la zone d’affichage de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="1cc13-110">A [**RECT**](/previous-versions//dd162897(v=vs.85)) structure specifying the display area of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc13-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cc13-111">Return value</span></span>

<span data-ttu-id="1cc13-112">Si l’opération a échoué, la valeur de retour est **true**.</span><span class="sxs-lookup"><span data-stu-id="1cc13-112">If the operation succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="1cc13-113">Si l’opération échoue, la valeur de retour est **false**.</span><span class="sxs-lookup"><span data-stu-id="1cc13-113">If the operation fails, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cc13-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1cc13-114">Remarks</span></span>

<span data-ttu-id="1cc13-115">Les objets de texte et de modèle COM (Component Object Model) sont découpés par le rectangle.</span><span class="sxs-lookup"><span data-stu-id="1cc13-115">Text and Component Object Model (COM) objects are clipped by the rectangle.</span></span> <span data-ttu-id="1cc13-116">L’application n’a pas besoin de définir la zone de découpage.</span><span class="sxs-lookup"><span data-stu-id="1cc13-116">The application does not need to set the clipping region.</span></span>

<span data-ttu-id="1cc13-117">La bande est le processus par lequel une seule page de sortie est générée à l’aide d’un ou de plusieurs rectangles séparés, ou de bandes.</span><span class="sxs-lookup"><span data-stu-id="1cc13-117">Banding is the process by which a single page of output is generated using one or more separate rectangles, or bands.</span></span> <span data-ttu-id="1cc13-118">Lorsque toutes les bandes sont placées sur la page, une image complète les résultats.</span><span class="sxs-lookup"><span data-stu-id="1cc13-118">When all bands are placed on the page, a complete image results.</span></span> <span data-ttu-id="1cc13-119">Cette approche est souvent utilisée par les imprimantes raster qui ne disposent pas de suffisamment de mémoire ou de capacité à effectuer une image de page entière à la fois.</span><span class="sxs-lookup"><span data-stu-id="1cc13-119">This approach is often used by raster printers that do not have sufficient memory or ability to image a full page at one time.</span></span> <span data-ttu-id="1cc13-120">Les périphériques de bandes incluent la plupart des imprimantes matricielles, ainsi que certaines imprimantes laser.</span><span class="sxs-lookup"><span data-stu-id="1cc13-120">Banding devices include most dot matrix printers as well as some laser printers.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc13-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cc13-121">Requirements</span></span>



| <span data-ttu-id="1cc13-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cc13-122">Requirement</span></span> | <span data-ttu-id="1cc13-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cc13-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc13-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cc13-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1cc13-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cc13-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1cc13-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cc13-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1cc13-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cc13-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1cc13-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cc13-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cc13-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cc13-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cc13-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cc13-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc13-131">Impression de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="1cc13-131">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

