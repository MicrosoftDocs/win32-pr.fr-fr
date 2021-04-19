---
title: Énumération TITLEBAR_TYPE (Softkbdc. h)
description: Les éléments de l' \_ énumération de type TITLEBAR sont utilisés pour spécifier les types de titlebars qui sont disponibles pour une fenêtre de clavier temporaire.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- TITLEBAR_TYPE l’infrastructure des services de texte d’énumération
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510326"
---
# <a name="titlebar_type-enumeration"></a><span data-ttu-id="1c6fb-104">\_Énumération de type TITLEBAR</span><span class="sxs-lookup"><span data-stu-id="1c6fb-104">TITLEBAR\_TYPE enumeration</span></span>

<span data-ttu-id="1c6fb-105">Les éléments de l’énumération de **\_ type TITLEBAR** sont utilisés pour spécifier les types de titlebars qui sont disponibles pour une fenêtre de clavier temporaire.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-105">Elements of the **TITLEBAR\_TYPE** enumeration are used to specify types of titlebars that are available for a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c6fb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c6fb-106">Syntax</span></span>


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a><span data-ttu-id="1c6fb-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="1c6fb-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1c6fb-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="1c6fb-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="1c6fb-109">La fenêtre du clavier logiciel n’utilise pas de TitleBar.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-109">The soft keyboard window uses no titlebar.</span></span>

</dd> <dt>

<span data-ttu-id="1c6fb-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**préhension de TITLEBAR \_ \_ horizontale \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="1c6fb-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**TITLEBAR\_GRIPPER\_HORIZ\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="1c6fb-111">La fenêtre de clavier temporaire utilise uniquement une barre de redimensionnement horizontale.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-111">The soft keyboard window uses a horizontal gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="1c6fb-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**redimensionnement de TITLEBAR vers le \_ \_ vert \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="1c6fb-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**TITLEBAR\_GRIPPER\_VERTI\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="1c6fb-113">La fenêtre de clavier temporaire utilise uniquement une barre de redimensionnement verticale.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-113">The soft keyboard window uses a vertical gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="1c6fb-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**\_bouton de redimensionnement de la TITLEBAR \_**</span><span class="sxs-lookup"><span data-stu-id="1c6fb-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**TITLEBAR\_GRIPPER\_BUTTON**</span></span>
</dt> <dd>

<span data-ttu-id="1c6fb-115">La fenêtre de clavier temporaire utilise uniquement un bouton de manipulation.</span><span class="sxs-lookup"><span data-stu-id="1c6fb-115">The soft keyboard window uses a gripper button only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c6fb-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c6fb-116">Requirements</span></span>



| <span data-ttu-id="1c6fb-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c6fb-117">Requirement</span></span> | <span data-ttu-id="1c6fb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c6fb-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c6fb-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c6fb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1c6fb-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c6fb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1c6fb-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c6fb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1c6fb-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c6fb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1c6fb-123">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1c6fb-123">Redistributable</span></span><br/>          | <span data-ttu-id="1c6fb-124">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="1c6fb-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="1c6fb-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c6fb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c6fb-126"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c6fb-126"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="1c6fb-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="1c6fb-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1c6fb-128"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c6fb-128"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





