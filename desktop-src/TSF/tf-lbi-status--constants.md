---
title: Constantes TF_LBI_STATUS_ (Ctfutb. h)
description: Les \_ \_ constantes TF IFA status \_ indiquent l’état d’un élément de barre de langue. Ces valeurs sont utilisées avec la méthode GetStatus ITfLangBarItem.
ms.assetid: 5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc
topic_type:
- apiref
api_name:
- TF_LBI_STATUS_HIDDEN
- TF_LBI_STATUS_DISABLED
- TF_LBI_STATUS_BTN_TOGGLED
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de9dcf0272eaf79fd001461aa555d78c9d6ae30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742924"
---
# <a name="tf_lbi_status_-constants"></a><span data-ttu-id="b17d9-104">\_ \_ Constantes d’état de l’État IFA TF \_ \*</span><span class="sxs-lookup"><span data-stu-id="b17d9-104">TF\_LBI\_STATUS\_\* Constants</span></span>

<span data-ttu-id="b17d9-105">Les constantes \**tf \_ IFA \_ Status \_ \** _ indiquent l’état d’un élément de barre de langue.</span><span class="sxs-lookup"><span data-stu-id="b17d9-105">The \**TF\_LBI\_STATUS\_\** _ constants indicate the status of a language bar item.</span></span> <span data-ttu-id="b17d9-106">Ces valeurs sont utilisées avec la méthode [ITfLangBarItem :: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) .</span><span class="sxs-lookup"><span data-stu-id="b17d9-106">These values are used with the [ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) method.</span></span>



| <span data-ttu-id="b17d9-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="b17d9-107">Constant/value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="b17d9-108">Description</span><span class="sxs-lookup"><span data-stu-id="b17d9-108">Description</span></span>                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STATUS_HIDDEN"></span><span id="tf_lbi_status_hidden"></span><dl> <span data-ttu-id="b17d9-109"><dt>_ \* TF \_ \_État IFA \_ masqué \* \*</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b17d9-109"><dt>_\*TF\_LBI\_STATUS\_HIDDEN\*\*</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="b17d9-110">L’élément est masqué.</span><span class="sxs-lookup"><span data-stu-id="b17d9-110">The item is hidden.</span></span> <span data-ttu-id="b17d9-111">Ce style est ignoré si l’élément n’inclut pas le \_ \_ style HIDDENSTATUSCONTROL TF IFA style \_ .</span><span class="sxs-lookup"><span data-stu-id="b17d9-111">This style is ignored if the item does not include the TF\_LBI\_STYLE\_HIDDENSTATUSCONTROL style.</span></span><br/>                  |
| <span id="TF_LBI_STATUS_DISABLED"></span><span id="tf_lbi_status_disabled"></span><dl> <span data-ttu-id="b17d9-112"><dt>**Tf \_ \_État IFA \_ désactivé**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="b17d9-112"><dt>**TF\_LBI\_STATUS\_DISABLED**</dt> <dt>0x00000002</dt></span></span> </dl>           | <span data-ttu-id="b17d9-113">L’élément est désactivé.</span><span class="sxs-lookup"><span data-stu-id="b17d9-113">The item is disabled.</span></span><br/>                                                                                                                  |
| <span id="TF_LBI_STATUS_BTN_TOGGLED"></span><span id="tf_lbi_status_btn_toggled"></span><dl> <span data-ttu-id="b17d9-114"><dt>**Tf \_ \_État IFA \_ 0x00010000 \_ bascule**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b17d9-114"><dt>**TF\_LBI\_STATUS\_BTN\_TOGGLED**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="b17d9-115">L’élément est à l’état activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="b17d9-115">The item is in the toggled or pressed state.</span></span> <span data-ttu-id="b17d9-116">Ce style est ignoré si l’élément n’inclut pas le \_ style de \_ \_ basculement de style d’un type d’élément à la ligne TF IFA \_ .</span><span class="sxs-lookup"><span data-stu-id="b17d9-116">This style is ignored if the item does not include the TF\_LBI\_STYLE\_BTN\_TOGGLE style.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b17d9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b17d9-117">Requirements</span></span>



| <span data-ttu-id="b17d9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b17d9-118">Requirement</span></span> | <span data-ttu-id="b17d9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b17d9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b17d9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b17d9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b17d9-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b17d9-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b17d9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b17d9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b17d9-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b17d9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b17d9-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="b17d9-124">Redistributable</span></span><br/>          | <span data-ttu-id="b17d9-125">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="b17d9-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="b17d9-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b17d9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b17d9-127"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b17d9-127"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b17d9-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="b17d9-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b17d9-129"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b17d9-129"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b17d9-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b17d9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b17d9-131">ITfLangBarItem :: GetStatus</span><span class="sxs-lookup"><span data-stu-id="b17d9-131">ITfLangBarItem::GetStatus</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





