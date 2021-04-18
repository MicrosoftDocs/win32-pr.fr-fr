---
title: Player. windowlessVideo
description: La propriété windowlessVideo spécifie ou récupère une valeur indiquant si le contrôle du lecteur Windows Media affiche la vidéo en mode sans fenêtre.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Lecteur Windows Media Player. windowlessVideo
topic_type:
- apiref
api_name:
- Player.windowlessVideo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93f4a8a2b70a42cd0893d463eccca0427dde6c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532829"
---
# <a name="playerwindowlessvideo"></a><span data-ttu-id="adb70-104">Player. windowlessVideo</span><span class="sxs-lookup"><span data-stu-id="adb70-104">Player.windowlessVideo</span></span>

<span data-ttu-id="adb70-105">La propriété **windowlessVideo** spécifie ou récupère une valeur indiquant si le contrôle du lecteur Windows Media affiche la vidéo en mode sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="adb70-105">The **windowlessVideo** property specifies or retrieves a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="adb70-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adb70-106">Syntax</span></span>

<span data-ttu-id="adb70-107">*lecteur*. **windowlessVideo**</span><span class="sxs-lookup"><span data-stu-id="adb70-107">*player*.**windowlessVideo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="adb70-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="adb70-108">Possible Values</span></span>

<span data-ttu-id="adb70-109">Cette propriété est une **valeur booléenne** qui est spécifiée au moment de la conception et est en lecture seule par la suite.</span><span class="sxs-lookup"><span data-stu-id="adb70-109">This property is a **Boolean** that is specified at design time and is read-only thereafter.</span></span>



| <span data-ttu-id="adb70-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="adb70-110">Value</span></span> | <span data-ttu-id="adb70-111">Description</span><span class="sxs-lookup"><span data-stu-id="adb70-111">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="adb70-112">true</span><span class="sxs-lookup"><span data-stu-id="adb70-112">true</span></span>  | <span data-ttu-id="adb70-113">La vidéo est rendue en mode sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="adb70-113">The video is rendered in windowless mode.</span></span>        |
| <span data-ttu-id="adb70-114">false</span><span class="sxs-lookup"><span data-stu-id="adb70-114">false</span></span> | <span data-ttu-id="adb70-115">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="adb70-115">Default.</span></span> <span data-ttu-id="adb70-116">La vidéo est rendue en mode fenêtre.</span><span class="sxs-lookup"><span data-stu-id="adb70-116">The video is rendered in windowed mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="adb70-117">Notes</span><span class="sxs-lookup"><span data-stu-id="adb70-117">Remarks</span></span>

<span data-ttu-id="adb70-118">Par défaut, un contrôle du lecteur Windows Media incorporé affiche la vidéo dans sa propre fenêtre au sein de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="adb70-118">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="adb70-119">Quand **windowlessVideo** a la valeur true, le contrôle du lecteur affiche la vidéo directement dans la zone cliente, ce qui vous permet d’appliquer des effets spéciaux ou de coucher la vidéo avec du texte.</span><span class="sxs-lookup"><span data-stu-id="adb70-119">When **windowlessVideo** is set to true, the Player control renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="adb70-120">Dans Windows Vista, le rendu de la vidéo en mode sans fenêtre peut dégrader les performances.</span><span class="sxs-lookup"><span data-stu-id="adb70-120">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="adb70-121">La propriété **windowlessVideo** n’est pas prise en charge pour Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="adb70-121">The **windowlessVideo** property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="adb70-122">La définition d’une valeur pour cette propriété dans le navigateur peut donner des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="adb70-122">Setting a value for this property in Navigator may yield unexpected results.</span></span>

<span data-ttu-id="adb70-123">**Lecteur Windows Media 10 Mobile :** Cette propriété n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="adb70-123">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="adb70-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adb70-124">Requirements</span></span>



| <span data-ttu-id="adb70-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adb70-125">Requirement</span></span> | <span data-ttu-id="adb70-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="adb70-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="adb70-127">Version</span><span class="sxs-lookup"><span data-stu-id="adb70-127">Version</span></span><br/> | <span data-ttu-id="adb70-128">Lecteur Windows Media pour Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="adb70-128">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="adb70-129">DLL</span><span class="sxs-lookup"><span data-stu-id="adb70-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="adb70-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adb70-130"><dt>Wmp.dll</dt></span></span> </dl> |



 

 





