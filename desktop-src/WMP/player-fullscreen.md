---
title: Player. fullScreen
description: La propriété fullScreen spécifie ou récupère une valeur indiquant si le contenu vidéo est lu en mode plein écran.
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Lecteur Windows Media Player. fullScreen
topic_type:
- apiref
api_name:
- Player.fullScreen
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3f71b4100c359effd95f79c574a52b5a5bae28c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542454"
---
# <a name="playerfullscreen"></a><span data-ttu-id="9c2f2-104">Player. fullScreen</span><span class="sxs-lookup"><span data-stu-id="9c2f2-104">Player.fullScreen</span></span>

<span data-ttu-id="9c2f2-105">La propriété **fullscreen** spécifie ou récupère une valeur indiquant si le contenu vidéo est lu en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-105">The **fullScreen** property specifies or retrieves a value indicating whether video content is played back in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c2f2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c2f2-106">Syntax</span></span>

<span data-ttu-id="9c2f2-107">*lecteur* . **plein écran**</span><span class="sxs-lookup"><span data-stu-id="9c2f2-107">*player* .**fullScreen**</span></span>

## <a name="possible-values"></a><span data-ttu-id="9c2f2-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="9c2f2-108">Possible Values</span></span>

<span data-ttu-id="9c2f2-109">Cette propriété est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="9c2f2-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c2f2-110">Value</span></span> | <span data-ttu-id="9c2f2-111">Description</span><span class="sxs-lookup"><span data-stu-id="9c2f2-111">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="9c2f2-112">true</span><span class="sxs-lookup"><span data-stu-id="9c2f2-112">true</span></span>  | <span data-ttu-id="9c2f2-113">Le contenu vidéo est lu en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-113">Video content is played back in full-screen mode.</span></span>              |
| <span data-ttu-id="9c2f2-114">false</span><span class="sxs-lookup"><span data-stu-id="9c2f2-114">false</span></span> | <span data-ttu-id="9c2f2-115">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-115">Default.</span></span> <span data-ttu-id="9c2f2-116">Le contenu vidéo n’est pas lu en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-116">Video content is not played back in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9c2f2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9c2f2-117">Remarks</span></span>

<span data-ttu-id="9c2f2-118">Pour que le mode plein écran fonctionne correctement quand vous incorporez le contrôle du lecteur Windows Media, la zone d’affichage de la vidéo doit avoir une hauteur et une largeur d’au moins un pixel.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-118">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="9c2f2-119">Si **UIMODE** a la valeur « mini » ou « Full », la hauteur du contrôle lui-même doit être supérieure ou égale à 65 pour s’adapter à la zone d’affichage vidéo en plus de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-119">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="9c2f2-120">Si **UIMODE** a la valeur « invisible », l’affectation de la valeur true à cette propriété génère une erreur et n’affecte pas le comportement du contrôle.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-120">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="9c2f2-121">Pendant la lecture en plein écran, le lecteur Windows Media masque le curseur de la souris quand **enableContextMenu** est égal à false et **UIMODE** est égal à « None ».</span><span class="sxs-lookup"><span data-stu-id="9c2f2-121">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="9c2f2-122">Si **UIMODE** a la valeur « Full » ou « mini », le lecteur Windows Media affiche les contrôles de transport en mode plein écran lorsque le curseur de la souris se déplace.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-122">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="9c2f2-123">Après un bref intervalle d’absence de mouvement de la souris, les contrôles de transport sont masqués.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-123">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="9c2f2-124">Si **UIMODE** a la valeur « None », aucun contrôle n’est affiché en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-124">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="9c2f2-125">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="9c2f2-125">**Note**</span></span>

<span data-ttu-id="9c2f2-126">L’affichage des contrôles de transport en mode plein écran nécessite le système d’exploitation Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-126">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

<span data-ttu-id="9c2f2-127">Si les contrôles de transport ne s’affichent pas en mode plein écran, le lecteur Windows Media quitte automatiquement le mode plein écran lorsque la lecture s’arrête.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-127">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

<span data-ttu-id="9c2f2-128">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="9c2f2-128">**Note**</span></span>

<span data-ttu-id="9c2f2-129">Veillez à toujours informer l’utilisateur sur la manière de revenir en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-129">Always be sure to inform the user how to return from full-screen mode.</span></span>

## <a name="examples"></a><span data-ttu-id="9c2f2-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="9c2f2-130">Examples</span></span>

<span data-ttu-id="9c2f2-131">L’exemple suivant crée un bouton d’entrée HTML qui utilise *Player*. **plein** écran pour faire basculer un objet lecteur incorporé en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-131">The following example creates an HTML input button that uses *Player*.**fullScreen** to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="9c2f2-132">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9c2f2-132">The **Player** object was created with ID = "Player".</span></span>


```
<INPUT type = button 
       value = "Full Screen" 
       name = FSBUTTON
       onclick = "
               /* Check to be sure the player is playing. */
               if (Player.playState == 3) 
                  Player.fullScreen = 'true';
               ">
```



## <a name="requirements"></a><span data-ttu-id="9c2f2-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9c2f2-133">Requirements</span></span>



| <span data-ttu-id="9c2f2-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9c2f2-134">Requirement</span></span> | <span data-ttu-id="9c2f2-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="9c2f2-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9c2f2-136">Version</span><span class="sxs-lookup"><span data-stu-id="9c2f2-136">Version</span></span><br/> | <span data-ttu-id="9c2f2-137">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9c2f2-137">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9c2f2-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9c2f2-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="9c2f2-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c2f2-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c2f2-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c2f2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c2f2-141">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="9c2f2-141">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





