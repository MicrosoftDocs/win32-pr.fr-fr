---
title: Styles d’info-bulle (CommCtrl. h)
description: Cette section répertorie les styles de contrôle utilisés avec les contrôles ToolTip.
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8b89aed88caddceae815414b9f2b4d93a550c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543793"
---
# <a name="tooltip-styles"></a><span data-ttu-id="3475d-103">Styles d’info-bulle</span><span class="sxs-lookup"><span data-stu-id="3475d-103">Tooltip Styles</span></span>

<span data-ttu-id="3475d-104">Cette section répertorie les styles de contrôle utilisés avec les contrôles ToolTip.</span><span class="sxs-lookup"><span data-stu-id="3475d-104">This section lists the control styles used with tooltip controls.</span></span>



| <span data-ttu-id="3475d-105">Constante</span><span class="sxs-lookup"><span data-stu-id="3475d-105">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="3475d-106">Description</span><span class="sxs-lookup"><span data-stu-id="3475d-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <span data-ttu-id="3475d-107"><dt>**\_ALWAYSTIP TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="3475d-107"><dt>**TTS\_ALWAYSTIP**</dt></span></span> </dl>                | <span data-ttu-id="3475d-108">Indique que le contrôle ToolTip apparaît lorsque le curseur se trouve sur un outil, même si la fenêtre propriétaire du contrôle ToolTip est inactive.</span><span class="sxs-lookup"><span data-stu-id="3475d-108">Indicates that the tooltip control appears when the cursor is on a tool, even if the tooltip control's owner window is inactive.</span></span> <span data-ttu-id="3475d-109">Sans ce style, l’info-bulle s’affiche uniquement lorsque la fenêtre propriétaire de l’outil est active.</span><span class="sxs-lookup"><span data-stu-id="3475d-109">Without this style, the tooltip appears only when the tool's owner window is active.</span></span><br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <span data-ttu-id="3475d-110"><dt>**\_bulle TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="3475d-110"><dt>**TTS\_BALLOON**</dt></span></span> </dl>                      | <span data-ttu-id="3475d-111">[Version 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="3475d-111">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="3475d-112">Indique que le contrôle ToolTip a l’apparence d’un « ballon » animé, avec des angles arrondis et une tige pointant sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="3475d-112">Indicates that the tooltip control has the appearance of a cartoon "balloon," with rounded corners and a stem pointing to the item.</span></span> <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <span data-ttu-id="3475d-113"><dt>**\_fermeture TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="3475d-113"><dt>**TTS\_CLOSE**</dt></span></span> </dl>                            | <span data-ttu-id="3475d-114">Affiche un bouton **Fermer** dans l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="3475d-114">Displays a **Close** button on the tooltip.</span></span> <span data-ttu-id="3475d-115">Valide uniquement lorsque l’info-bulle a le \_ style de bulle TTS et un titre ; consultez [**atténuation \_ SETTITLE**](ttm-settitle.md).</span><span class="sxs-lookup"><span data-stu-id="3475d-115">Valid only when the tooltip has the TTS\_BALLOON style and a title; see [**TTM\_SETTITLE**](ttm-settitle.md).</span></span><br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <span data-ttu-id="3475d-116"><dt>**\_NOanimate TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="3475d-116"><dt>**TTS\_NOANIMATE**</dt></span></span> </dl>                | <span data-ttu-id="3475d-117">[Version 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="3475d-117">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="3475d-118">Désactive l’animation de l’info-bulle glissante sur les systèmes Windows 98 et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3475d-118">Disables sliding tooltip animation on Windows 98 and Windows 2000 systems.</span></span> <span data-ttu-id="3475d-119">Ce style est ignoré sur les systèmes précédents.</span><span class="sxs-lookup"><span data-stu-id="3475d-119">This style is ignored on earlier systems.</span></span><br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <span data-ttu-id="3475d-120"><dt>**TTS avec \_ fondu**</dt></span><span class="sxs-lookup"><span data-stu-id="3475d-120"><dt>**TTS\_NOFADE**</dt></span></span> </dl>                         | <span data-ttu-id="3475d-121">[Version 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="3475d-121">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="3475d-122">Désactive l’animation des info-bulles de fondu.</span><span class="sxs-lookup"><span data-stu-id="3475d-122">Disables fading tooltip animation.</span></span> <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <span data-ttu-id="3475d-123"><dt>**le \_ préfixe TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="3475d-123"><dt>**TTS\_NOPREFIX**</dt></span></span> </dl>                   | <span data-ttu-id="3475d-124">Empêche le système de commettre des caractères perluète d’une chaîne ou de terminer une chaîne au niveau d’un caractère de tabulation.</span><span class="sxs-lookup"><span data-stu-id="3475d-124">Prevents the system from stripping ampersand characters from a string or terminating a string at a tab character.</span></span> <span data-ttu-id="3475d-125">Sans ce style, le système supprime automatiquement les caractères perluète et met fin à une chaîne au premier caractère de tabulation.</span><span class="sxs-lookup"><span data-stu-id="3475d-125">Without this style, the system automatically strips ampersand characters and terminates a string at the first tab character.</span></span> <span data-ttu-id="3475d-126">Cela permet à une application d’utiliser la même chaîne qu’à la fois comme élément de menu et comme texte dans un contrôle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="3475d-126">This allows an application to use the same string as both a menu item and as text in a tooltip control.</span></span><br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <span data-ttu-id="3475d-127"><dt>**\_USEVISUALSTYLE TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="3475d-127"><dt>**TTS\_USEVISUALSTYLE**</dt></span></span> </dl> | <span data-ttu-id="3475d-128">Utilise des liens hypertexte à thème.</span><span class="sxs-lookup"><span data-stu-id="3475d-128">Uses themed hyperlinks.</span></span> <span data-ttu-id="3475d-129">Le thème définit les styles des liens dans l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="3475d-129">The theme will define the styles for any links in the tooltip.</span></span> <span data-ttu-id="3475d-130">Ce style requiert toujours la \_ définition de la PARSELINKS ttf.</span><span class="sxs-lookup"><span data-stu-id="3475d-130">This style always requires TTF\_PARSELINKS to be set.</span></span> <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="3475d-131">Notes</span><span class="sxs-lookup"><span data-stu-id="3475d-131">Remarks</span></span>

<span data-ttu-id="3475d-132">Un contrôle ToolTip a toujours les \_ styles de fenêtre popup et WS \_ ex \_ TOOLWINDOW, que vous les spécifiiez ou non lors de la création du contrôle.</span><span class="sxs-lookup"><span data-stu-id="3475d-132">A tooltip control always has the WS\_POPUP and WS\_EX\_TOOLWINDOW window styles, regardless of whether you specify them when creating the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="3475d-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3475d-133">Requirements</span></span>



| <span data-ttu-id="3475d-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3475d-134">Requirement</span></span> | <span data-ttu-id="3475d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="3475d-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3475d-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="3475d-136">Header</span></span><br/> | <dl> <span data-ttu-id="3475d-137"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3475d-137"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





