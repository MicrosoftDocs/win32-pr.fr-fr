---
title: Énumération TYPEMODE (Softkbdc. h)
description: Les éléments de l’énumération TYPEMODE sont utilisés pour spécifier les modes de type disponibles pour un clavier conditionnel.
ms.assetid: 7db0a4dd-0ee2-455d-aeb8-11cd1249134c
keywords:
- TYPEMODE énumération Text Services Framework
topic_type:
- apiref
api_name:
- TYPEMODE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24054443802d0b8a759841cb6b3fc3cb5d510024
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511745"
---
# <a name="typemode-enumeration"></a><span data-ttu-id="ee170-104">Énumération TYPEMODE</span><span class="sxs-lookup"><span data-stu-id="ee170-104">TYPEMODE enumeration</span></span>

<span data-ttu-id="ee170-105">Les éléments de l’énumération **TYPEMODE** sont utilisés pour spécifier les modes de type disponibles pour un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="ee170-105">Elements of the **TYPEMODE** enumeration are used to specify type modes that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee170-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee170-106">Syntax</span></span>


```C++
typedef enum tagTYPEMODE { 
  ClickMouse  = 0,
  Hover       = 1,
  Scanning    = 2
} TYPEMODE;
```



## <a name="constants"></a><span data-ttu-id="ee170-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="ee170-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ee170-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**</span><span class="sxs-lookup"><span data-stu-id="ee170-108"><span id="ClickMouse"></span><span id="clickmouse"></span><span id="CLICKMOUSE"></span>**ClickMouse**</span></span>
</dt> <dd>

<span data-ttu-id="ee170-109">L’utilisateur peut cliquer sur les touches à l’écran pour taper du texte.</span><span class="sxs-lookup"><span data-stu-id="ee170-109">The user can click the on-screen keys to type text.</span></span>

</dd> <dt>

<span data-ttu-id="ee170-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Pointez**</span><span class="sxs-lookup"><span data-stu-id="ee170-110"><span id="Hover"></span><span id="hover"></span><span id="HOVER"></span>**Hover**</span></span>
</dt> <dd>

<span data-ttu-id="ee170-111">L’utilisateur peut pointer vers une touche pour une période prédéfinie, et le caractère sélectionné est tapé automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ee170-111">The user can point to a key for a predefined period of time, and the selected character is typed automatically.</span></span>

</dd> <dt>

<span data-ttu-id="ee170-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Cour**</span><span class="sxs-lookup"><span data-stu-id="ee170-112"><span id="Scanning"></span><span id="scanning"></span><span id="SCANNING"></span>**Scanning**</span></span>
</dt> <dd>

<span data-ttu-id="ee170-113">Le clavier logiciel balaie continuellement la zone d’entrée et met en surbrillance les régions où l’utilisateur peut appuyer sur une touche de raccourci ou utiliser un périphérique d’entrée de commutateur.</span><span class="sxs-lookup"><span data-stu-id="ee170-113">The soft keyboard continually scans the input area and highlights regions where the user can press a shortcut key or use a switch-input device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee170-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee170-114">Requirements</span></span>



| <span data-ttu-id="ee170-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee170-115">Requirement</span></span> | <span data-ttu-id="ee170-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee170-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee170-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee170-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ee170-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee170-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ee170-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee170-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ee170-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee170-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ee170-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="ee170-121">Redistributable</span></span><br/>          | <span data-ttu-id="ee170-122">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="ee170-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="ee170-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee170-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee170-124"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee170-124"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="ee170-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="ee170-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ee170-126"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ee170-126"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





