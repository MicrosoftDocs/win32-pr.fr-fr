---
title: Paramètres. invokeURLs
description: La propriété invokeURLs spécifie ou récupère une valeur indiquant si les événements d’URL doivent lancer un navigateur Web.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Settings. invokeURLs Windows Media Player
topic_type:
- apiref
api_name:
- Settings.invokeURLs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb55bb61243e6905a51a943a26adc120511335c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535963"
---
# <a name="settingsinvokeurls"></a><span data-ttu-id="894a0-104">Paramètres. invokeURLs</span><span class="sxs-lookup"><span data-stu-id="894a0-104">Settings.invokeURLs</span></span>

<span data-ttu-id="894a0-105">La propriété **invokeURLs** spécifie ou récupère une valeur indiquant si les événements d’URL doivent lancer un navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="894a0-105">The **invokeURLs** property specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="894a0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="894a0-106">Syntax</span></span>

<span data-ttu-id="894a0-107">Player. Settings. invokeURLs</span><span class="sxs-lookup"><span data-stu-id="894a0-107">player.settings.invokeURLs</span></span>

## <a name="possible-values"></a><span data-ttu-id="894a0-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="894a0-108">Possible Values</span></span>

<span data-ttu-id="894a0-109">Cette propriété est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="894a0-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="894a0-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="894a0-110">Value</span></span> | <span data-ttu-id="894a0-111">Description</span><span class="sxs-lookup"><span data-stu-id="894a0-111">Description</span></span>                                  |
|-------|----------------------------------------------|
| <span data-ttu-id="894a0-112">true</span><span class="sxs-lookup"><span data-stu-id="894a0-112">true</span></span>  | <span data-ttu-id="894a0-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="894a0-113">Default.</span></span> <span data-ttu-id="894a0-114">Les événements d’URL doivent lancer un navigateur.</span><span class="sxs-lookup"><span data-stu-id="894a0-114">URL events should launch a browser.</span></span> |
| <span data-ttu-id="894a0-115">false</span><span class="sxs-lookup"><span data-stu-id="894a0-115">false</span></span> | <span data-ttu-id="894a0-116">Les événements d’URL ne doivent pas lancer de navigateur.</span><span class="sxs-lookup"><span data-stu-id="894a0-116">URL events should not launch a browser.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="894a0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="894a0-117">Remarks</span></span>

<span data-ttu-id="894a0-118">Les fichiers multimédias peuvent contenir des URL.</span><span class="sxs-lookup"><span data-stu-id="894a0-118">Media files can contain URLs.</span></span> <span data-ttu-id="894a0-119">Quand une URL est envoyée au contrôle du lecteur Windows Media, elle est d’abord transmise au gestionnaire d’événements **commande** , quelle que soit la valeur de **invokeURLs**.</span><span class="sxs-lookup"><span data-stu-id="894a0-119">When a URL is sent to the Windows Media Player control, it is passed first to the **ScriptCommand** event handler regardless of the value in **invokeURLs**.</span></span> <span data-ttu-id="894a0-120">Après la sortie de **commande** , le lecteur Windows Media vérifie **invokeURLs** pour déterminer s’il faut lancer le navigateur Internet par défaut avec l’URL.</span><span class="sxs-lookup"><span data-stu-id="894a0-120">After **ScriptCommand** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Internet browser with the URL.</span></span> <span data-ttu-id="894a0-121">Vous pouvez afficher des URL de manière sélective en les vérifiant dans **commande** et en définissant **invokeURLs** comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="894a0-121">You can selectively display URLs by checking them in **ScriptCommand** and setting **invokeURLs** as desired.</span></span>

<span data-ttu-id="894a0-122">**Windows Media Player 10 Mobile**: cette propriété accepte ou retourne la valeur false uniquement.</span><span class="sxs-lookup"><span data-stu-id="894a0-122">**Windows Media Player 10 Mobile**: This property only accepts or returns false.</span></span>

## <a name="requirements"></a><span data-ttu-id="894a0-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="894a0-123">Requirements</span></span>



| <span data-ttu-id="894a0-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="894a0-124">Requirement</span></span> | <span data-ttu-id="894a0-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="894a0-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="894a0-126">Version</span><span class="sxs-lookup"><span data-stu-id="894a0-126">Version</span></span><br/> | <span data-ttu-id="894a0-127">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="894a0-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="894a0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="894a0-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="894a0-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="894a0-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="894a0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="894a0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="894a0-131">**Événement Player. commande**</span><span class="sxs-lookup"><span data-stu-id="894a0-131">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="894a0-132">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="894a0-132">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





