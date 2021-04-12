---
title: Constantes diverses de la barre de langage (Ctfutb. h)
description: Les constantes diverses de la barre de langage définissent certaines propriétés des barres de langue.
ms.assetid: c1740636-7ba3-4748-9005-ee94d04dbb15
topic_type:
- apiref
api_name:
- TF_DTLBI_USEPROFILEICON
- TF_INVALIDMENUITEM
- TF_LBI_BMPF_VERTICAL
- TF_LBI_DESC_MAXLEN
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fd1a371581dea02226ba6539ca25a06ef98e75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385111"
---
# <a name="miscellaneous-language-bar-constants"></a><span data-ttu-id="66df1-103">Constantes diverses de la barre de langage</span><span class="sxs-lookup"><span data-stu-id="66df1-103">Miscellaneous Language Bar Constants</span></span>

<span data-ttu-id="66df1-104">Les constantes diverses de la barre de langage définissent certaines propriétés des barres de langue.</span><span class="sxs-lookup"><span data-stu-id="66df1-104">The miscellaneous language bar constants set certain properties of language bars.</span></span>



| <span data-ttu-id="66df1-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="66df1-105">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="66df1-106">Description</span><span class="sxs-lookup"><span data-stu-id="66df1-106">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DTLBI_USEPROFILEICON"></span><span id="tf_dtlbi_useprofileicon"></span><dl> <span data-ttu-id="66df1-107"><dt>**Tf \_ DTLBI \_ USEPROFILEICON**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="66df1-107"><dt>**TF\_DTLBI\_USEPROFILEICON**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="66df1-108">L’élément de la barre de langue système doit afficher l’icône spécifiée pour le profil de langue.</span><span class="sxs-lookup"><span data-stu-id="66df1-108">The system language bar item should display the icon specified for the language profile.</span></span> <span data-ttu-id="66df1-109">Utilisé dans les méthodes [ITfSystemDeviceTypeLangBarItem :: GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) et [ITfSystemDeviceTypeLangBarItem :: SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) .</span><span class="sxs-lookup"><span data-stu-id="66df1-109">Used in the [ITfSystemDeviceTypeLangBarItem::GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) and [ITfSystemDeviceTypeLangBarItem::SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) methods.</span></span><br/> |
| <span id="TF_INVALIDMENUITEM"></span><span id="tf_invalidmenuitem"></span><dl> <span data-ttu-id="66df1-110"><dt>**Tf \_ INVALIDMENUITEM**</dt> <dt>(uint) (-1)</dt></span><span class="sxs-lookup"><span data-stu-id="66df1-110"><dt>**TF\_INVALIDMENUITEM**</dt> <dt>(UINT)(-1)</dt></span></span> </dl>                 | <span data-ttu-id="66df1-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="66df1-111">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_BMPF_VERTICAL"></span><span id="tf_lbi_bmpf_vertical"></span><dl> <span data-ttu-id="66df1-112"><dt>**Tf \_ IFA \_ BMPF \_ vertical**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="66df1-112"><dt>**TF\_LBI\_BMPF\_VERTICAL**</dt> <dt>0x00000001</dt></span></span> </dl>         | <span data-ttu-id="66df1-113">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="66df1-113">Not used.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_DESC_MAXLEN"></span><span id="tf_lbi_desc_maxlen"></span><dl> <span data-ttu-id="66df1-114"><dt>**Tf \_ IFA \_ desc \_ MaxLen**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="66df1-114"><dt>**TF\_LBI\_DESC\_MAXLEN**</dt> <dt>32</dt></span></span> </dl>                       | <span data-ttu-id="66df1-115">Longueur, en caractères WCHAR, du membre de structure [tf \_ LANGBARITEMINFO. szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).</span><span class="sxs-lookup"><span data-stu-id="66df1-115">Length, in WCHAR characters, of structure member [TF\_LANGBARITEMINFO.szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo).</span></span><br/>                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="66df1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66df1-116">Requirements</span></span>



| <span data-ttu-id="66df1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66df1-117">Requirement</span></span> | <span data-ttu-id="66df1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="66df1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66df1-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66df1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="66df1-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66df1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="66df1-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66df1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="66df1-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66df1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66df1-123">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="66df1-123">Redistributable</span></span><br/>          | <span data-ttu-id="66df1-124">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="66df1-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="66df1-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="66df1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="66df1-126"><dt>Ctfutb. h</dt></span><span class="sxs-lookup"><span data-stu-id="66df1-126"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="66df1-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="66df1-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66df1-128"><dt>Ctfutb. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66df1-128"><dt>Ctfutb.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66df1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66df1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66df1-130">ITfSystemDeviceTypeLangBarItem::GetIconMode</span><span class="sxs-lookup"><span data-stu-id="66df1-130">ITfSystemDeviceTypeLangBarItem::GetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode)
</dt> <dt>

[<span data-ttu-id="66df1-131">ITfSystemDeviceTypeLangBarItem::SetIconMode</span><span class="sxs-lookup"><span data-stu-id="66df1-131">ITfSystemDeviceTypeLangBarItem::SetIconMode</span></span>](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)
</dt> <dt>

[<span data-ttu-id="66df1-132">TF \_ LANGBARITEMINFO</span><span class="sxs-lookup"><span data-stu-id="66df1-132">TF\_LANGBARITEMINFO</span></span>](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> </dl>

 

 





