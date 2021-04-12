---
title: Constantes TF_MOD_ (msctf. h)
description: Les \_ \_ constantes TF mod \ spécifient des modificateurs de clé dans la \_ structure PRESERVEDKEY TF.
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032821"
---
# <a name="tf_mod_-constants"></a><span data-ttu-id="0755f-103">\_ \_ \* CONSTANTEs mod TF</span><span class="sxs-lookup"><span data-stu-id="0755f-103">TF\_MOD\_\* Constants</span></span>

<span data-ttu-id="0755f-104">Les \_ \_ \* constantes TF mod spécifient des modificateurs de clé dans la structure [ \_ PRESERVEDKEY TF](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) .</span><span class="sxs-lookup"><span data-stu-id="0755f-104">The TF\_MOD\_\* constants specify key modifiers in the [TF\_PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) structure.</span></span>



| <span data-ttu-id="0755f-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="0755f-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="0755f-106">Description</span><span class="sxs-lookup"><span data-stu-id="0755f-106">Description</span></span>                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <span data-ttu-id="0755f-107"><dt>**Tf \_ MOD \_ ALT**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="0755f-107"><dt>**TF\_MOD\_ALT**</dt> <dt>0x0001</dt></span></span> </dl>                                                   | <span data-ttu-id="0755f-108">L’une des touches ALT est enfoncée</span><span class="sxs-lookup"><span data-stu-id="0755f-108">Either of the ALT keys is pressed</span></span><br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <span data-ttu-id="0755f-109"><dt>**Tf \_ 0x0002 \_ contrôle Mod**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0755f-109"><dt>**TF\_MOD\_CONTROL**</dt> <dt>0x0002</dt></span></span> </dl>                                       | <span data-ttu-id="0755f-110">L’une des touches CTRL est enfoncée</span><span class="sxs-lookup"><span data-stu-id="0755f-110">Either of the CTRL keys is pressed</span></span><br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <span data-ttu-id="0755f-111"><dt>**Tf \_ MOD \_ Shift**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="0755f-111"><dt>**TF\_MOD\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>                                             | <span data-ttu-id="0755f-112">L’une des touches MAJ est enfoncée</span><span class="sxs-lookup"><span data-stu-id="0755f-112">Either of the SHIFT keys is pressed</span></span><br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <span data-ttu-id="0755f-113"><dt>**Tf \_ MOD \_ Ralt**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="0755f-113"><dt>**TF\_MOD\_RALT**</dt> <dt>0x0008</dt></span></span> </dl>                                                | <span data-ttu-id="0755f-114">La touche ALT de droite est enfoncée</span><span class="sxs-lookup"><span data-stu-id="0755f-114">The right ALT key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <span data-ttu-id="0755f-115"><dt>**Tf \_ MOD \_ RCONTROL**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="0755f-115"><dt>**TF\_MOD\_RCONTROL**</dt> <dt>0x0010</dt></span></span> </dl>                                    | <span data-ttu-id="0755f-116">La touche CTRL de droite est enfoncée</span><span class="sxs-lookup"><span data-stu-id="0755f-116">The right CTRL key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <span data-ttu-id="0755f-117"><dt>**Tf \_ MOD \_ RSHIFT**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="0755f-117"><dt>**TF\_MOD\_RSHIFT**</dt> <dt>0x0020</dt></span></span> </dl>                                          | <span data-ttu-id="0755f-118">La touche Maj droite est enfoncée</span><span class="sxs-lookup"><span data-stu-id="0755f-118">The right SHIFT key is pressed</span></span><br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <span data-ttu-id="0755f-119"><dt>**Tf \_ MOD \_ LALT**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="0755f-119"><dt>**TF\_MOD\_LALT**</dt> <dt>0x0040</dt></span></span> </dl>                                                | <span data-ttu-id="0755f-120">La touche ALT de gauche est enfoncée</span><span class="sxs-lookup"><span data-stu-id="0755f-120">The left ALT key is pressed</span></span><br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <span data-ttu-id="0755f-121"><dt>**Tf \_ MOD \_ LCONTROL**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="0755f-121"><dt>**TF\_MOD\_LCONTROL**</dt> <dt>0x0080</dt></span></span> </dl>                                    | <span data-ttu-id="0755f-122">La touche CTRL de gauche est enfoncée</span><span class="sxs-lookup"><span data-stu-id="0755f-122">The left CTRL key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <span data-ttu-id="0755f-123"><dt>**Tf \_ MOD \_ LSHIFT**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="0755f-123"><dt>**TF\_MOD\_LSHIFT**</dt> <dt>0x0100</dt></span></span> </dl>                                          | <span data-ttu-id="0755f-124">La touche Maj de gauche est enfoncée</span><span class="sxs-lookup"><span data-stu-id="0755f-124">The left SHIFT key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <span data-ttu-id="0755f-125"><dt>**Tf \_ MOD \_ on \_ KEYUP**</dt> <dt>0x0200</dt></span><span class="sxs-lookup"><span data-stu-id="0755f-125"><dt>**TF\_MOD\_ON\_KEYUP**</dt> <dt>0x0200</dt></span></span> </dl>                                   | <span data-ttu-id="0755f-126">L’événement est déclenché lorsque la touche est relâchée.</span><span class="sxs-lookup"><span data-stu-id="0755f-126">The event will be fired when the key is released.</span></span> <span data-ttu-id="0755f-127">Sans cet indicateur, l’événement est déclenché lorsque la touche est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="0755f-127">Without this flag, the event is fired when the key is pressed.</span></span><br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <span data-ttu-id="0755f-128"><dt>**Tf \_ MOD \_ ignore \_ tous les \_ modificateurs**</dt> <dt>0x0400</dt></span><span class="sxs-lookup"><span data-stu-id="0755f-128"><dt>**TF\_MOD\_IGNORE\_ALL\_MODIFIER**</dt> <dt>0x0400</dt></span></span> </dl> | <span data-ttu-id="0755f-129">L’état des touches ALT, CTRL et Maj est ignoré.</span><span class="sxs-lookup"><span data-stu-id="0755f-129">The state of the ALT, CTRL, and SHIFT keys is ignored.</span></span> <span data-ttu-id="0755f-130">Cela signifie que l’événement est déclenché lorsque la touche virtuelle est enfoncée, quelles que soient les touches de modification enfoncées.</span><span class="sxs-lookup"><span data-stu-id="0755f-130">This means the event will be fired when the virtual key is pressed, regardless of which modifier keys are pressed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0755f-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0755f-131">Requirements</span></span>



| <span data-ttu-id="0755f-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0755f-132">Requirement</span></span> | <span data-ttu-id="0755f-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0755f-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0755f-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0755f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0755f-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0755f-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0755f-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0755f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0755f-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0755f-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0755f-138">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="0755f-138">Redistributable</span></span><br/>          | <span data-ttu-id="0755f-139">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="0755f-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="0755f-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="0755f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0755f-141"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="0755f-141"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="0755f-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="0755f-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0755f-143"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0755f-143"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0755f-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0755f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0755f-145">TF \_ PRESERVEDKEY</span><span class="sxs-lookup"><span data-stu-id="0755f-145">TF\_PRESERVEDKEY</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





