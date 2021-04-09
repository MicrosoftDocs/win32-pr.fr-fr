---
title: Message TB_CHANGEBITMAP (commctrl. h)
description: Modifie l’image bitmap d’un bouton dans une barre d’outils.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- TB_CHANGEBITMAP les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_CHANGEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367a2a1b4e35d6f52bf1e7a0be42f1e75daa7ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844454"
---
# <a name="tb_changebitmap-message"></a><span data-ttu-id="49395-104">TO \_ CHANGEBITMAP message</span><span class="sxs-lookup"><span data-stu-id="49395-104">TB\_CHANGEBITMAP message</span></span>

<span data-ttu-id="49395-105">Modifie l’image bitmap d’un bouton dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="49395-105">Changes the bitmap for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="49395-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49395-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49395-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49395-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49395-108">Identificateur de commande du bouton qui doit recevoir une nouvelle image bitmap.</span><span class="sxs-lookup"><span data-stu-id="49395-108">Command identifier of the button that is to receive a new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="49395-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49395-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49395-110">Index de base zéro d’une image dans la liste d’images de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="49395-110">Zero-based index of an image in the toolbar's image list.</span></span> <span data-ttu-id="49395-111">Le système affiche l’image spécifiée dans le bouton.</span><span class="sxs-lookup"><span data-stu-id="49395-111">The system displays the specified image in the button.</span></span> <span data-ttu-id="49395-112">Affectez à ce paramètre la valeur I \_ IMAGECALLBACK et la barre d’outils enverra la notification [**\_ GETDISPINFO TBN**](tbn-getdispinfo.md) pour récupérer l’index d’image quand il est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="49395-112">Set this parameter to I\_IMAGECALLBACK, and the toolbar will send the [**TBN\_GETDISPINFO**](tbn-getdispinfo.md) notification to retrieve the image index when it is needed.</span></span>

<span data-ttu-id="49395-113">[Version 5,81](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="49395-113">[Version 5.81](common-control-versions.md).</span></span> <span data-ttu-id="49395-114">Affectez à ce paramètre \_ la valeur I IMAGENONE pour indiquer que le bouton n’a pas d’image.</span><span class="sxs-lookup"><span data-stu-id="49395-114">Set this parameter to I\_IMAGENONE to indicate that the button does not have an image.</span></span> <span data-ttu-id="49395-115">La disposition du bouton n’inclut pas d’espace pour une image bitmap, uniquement du texte.</span><span class="sxs-lookup"><span data-stu-id="49395-115">The button layout will not include any space for a bitmap, only text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49395-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49395-116">Return value</span></span>

<span data-ttu-id="49395-117">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="49395-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="49395-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49395-118">Requirements</span></span>



| <span data-ttu-id="49395-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49395-119">Requirement</span></span> | <span data-ttu-id="49395-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="49395-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49395-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49395-121">Minimum supported client</span></span><br/> | <span data-ttu-id="49395-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49395-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49395-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49395-123">Minimum supported server</span></span><br/> | <span data-ttu-id="49395-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49395-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49395-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="49395-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="49395-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49395-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





