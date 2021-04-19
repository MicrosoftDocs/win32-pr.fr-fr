---
title: COLORTYPE, énumération (Softkbdc. h)
description: Les éléments de l’énumération COLORTYPE sont utilisés pour spécifier les types de couleurs disponibles pour un clavier conditionnel.
ms.assetid: 63a51f67-d85c-4017-a569-03df164198db
keywords:
- COLORTYPE, énumération Text Services Framework
topic_type:
- apiref
api_name:
- COLORTYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28f3b4111973e9676a34c548db566b1c95ac43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510161"
---
# <a name="colortype-enumeration"></a><span data-ttu-id="80435-104">COLORTYPE, énumération</span><span class="sxs-lookup"><span data-stu-id="80435-104">COLORTYPE enumeration</span></span>

<span data-ttu-id="80435-105">Les éléments de l’énumération **COLORTYPE** sont utilisés pour spécifier les types de couleurs disponibles pour un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="80435-105">Elements of the **COLORTYPE** enumeration are used to specify types of colors that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="80435-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80435-106">Syntax</span></span>


```C++
typedef enum tagCOLORTYPE { 
  bkcolor         = 0,
  UnSelForeColor  = 1,
  UnSelTextColor  = 2,
  SelForeColor    = 3,
  SelTextColor    = 4,
  Max_color_Type  = 5
} COLORTYPE;
```



## <a name="constants"></a><span data-ttu-id="80435-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="80435-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="80435-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**</span><span class="sxs-lookup"><span data-stu-id="80435-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**</span></span>
</dt> <dd>

<span data-ttu-id="80435-109">Couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="80435-109">Background color.</span></span>

</dd> <dt>

<span data-ttu-id="80435-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**</span><span class="sxs-lookup"><span data-stu-id="80435-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="80435-111">Couleur de premier plan non sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="80435-111">Unselected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="80435-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**</span><span class="sxs-lookup"><span data-stu-id="80435-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="80435-113">Couleur de texte non sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="80435-113">Unselected text color.</span></span>

</dd> <dt>

<span data-ttu-id="80435-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**</span><span class="sxs-lookup"><span data-stu-id="80435-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="80435-115">Couleur de premier plan sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="80435-115">Selected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="80435-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**</span><span class="sxs-lookup"><span data-stu-id="80435-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="80435-117">Couleur du texte sélectionné.</span><span class="sxs-lookup"><span data-stu-id="80435-117">Selected text color.</span></span>

</dd> <dt>

<span data-ttu-id="80435-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**\_Type de couleur max. \_**</span><span class="sxs-lookup"><span data-stu-id="80435-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**Max\_color\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="80435-119">Type de couleur maximal.</span><span class="sxs-lookup"><span data-stu-id="80435-119">Maximum color type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80435-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80435-120">Requirements</span></span>



| <span data-ttu-id="80435-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80435-121">Requirement</span></span> | <span data-ttu-id="80435-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="80435-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80435-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80435-123">Minimum supported client</span></span><br/> | <span data-ttu-id="80435-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80435-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="80435-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80435-125">Minimum supported server</span></span><br/> | <span data-ttu-id="80435-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80435-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="80435-127">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="80435-127">Redistributable</span></span><br/>          | <span data-ttu-id="80435-128">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="80435-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="80435-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="80435-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="80435-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="80435-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="80435-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="80435-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80435-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="80435-132"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





