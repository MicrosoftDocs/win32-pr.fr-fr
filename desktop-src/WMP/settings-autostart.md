---
title: Paramètres. démarrage automatique
description: La propriété AutoStart spécifie ou récupère une valeur indiquant si l’élément multimédia actuel commence à être lu automatiquement.
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- Paramètres. démarrage automatique du lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings.autoStart
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d08b8f84f4a0b51225ed5692a25fa41cab809ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523493"
---
# <a name="settingsautostart"></a><span data-ttu-id="d604d-104">Paramètres. démarrage automatique</span><span class="sxs-lookup"><span data-stu-id="d604d-104">Settings.autoStart</span></span>

<span data-ttu-id="d604d-105">La propriété **AutoStart** spécifie ou récupère une valeur indiquant si l’élément multimédia actuel commence à être lu automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d604d-105">The **autoStart** property specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="d604d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d604d-106">Syntax</span></span>

<span data-ttu-id="d604d-107">Player. Settings. AutoStart</span><span class="sxs-lookup"><span data-stu-id="d604d-107">player.settings.autoStart</span></span>

## <a name="possible-values"></a><span data-ttu-id="d604d-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="d604d-108">Possible Values</span></span>

<span data-ttu-id="d604d-109">Cette propriété est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d604d-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="d604d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="d604d-110">Value</span></span> | <span data-ttu-id="d604d-111">Description</span><span class="sxs-lookup"><span data-stu-id="d604d-111">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="d604d-112">true</span><span class="sxs-lookup"><span data-stu-id="d604d-112">true</span></span>  | <span data-ttu-id="d604d-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="d604d-113">Default.</span></span> <span data-ttu-id="d604d-114">La diffusion de l’élément multimédia commence automatiquement (consultez la section Notes).</span><span class="sxs-lookup"><span data-stu-id="d604d-114">The media item begins playing automatically (see Remarks).</span></span> |
| <span data-ttu-id="d604d-115">false</span><span class="sxs-lookup"><span data-stu-id="d604d-115">false</span></span> | <span data-ttu-id="d604d-116">La diffusion de l’élément multimédia ne commence pas automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d604d-116">The media item does not begin playing automatically.</span></span>                |



 

## <a name="remarks"></a><span data-ttu-id="d604d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d604d-117">Remarks</span></span>

<span data-ttu-id="d604d-118">Si le **démarrage automatique** est défini sur true, l’élément multimédia commence à s’exécuter quand *joueur*. **URL**, *Player*. **currentPlaylist** ou *Player*. **currentMedia** est défini.</span><span class="sxs-lookup"><span data-stu-id="d604d-118">If **autoStart** is set to true, the media item will begin playing when *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** is set.</span></span> <span data-ttu-id="d604d-119">Dans le cas contraire, il ne démarrera pas avant les *contrôles*. la méthode **Play** est appelée.</span><span class="sxs-lookup"><span data-stu-id="d604d-119">Otherwise, it will not start playing until the *Controls*.**play** method is called.</span></span>

<span data-ttu-id="d604d-120">Étant donné que la propriété **AutoStart** pour le mode complet du lecteur Windows Media peut être définie globalement par des événements externes (tels que le chargement d’un CD), il n’existe pas de valeur par défaut fiable pour les apparences et les contrôles de lecteur à distance.</span><span class="sxs-lookup"><span data-stu-id="d604d-120">Because the **autoStart** property for the full mode of Windows Media Player can be set globally by external events (such as loading a CD), there is no reliable default value for skins and remoted Player controls.</span></span> <span data-ttu-id="d604d-121">Cela est dû au fait que le moteur de lecture du lecteur en mode complet est utilisé dans les deux cas.</span><span class="sxs-lookup"><span data-stu-id="d604d-121">This is because the playback engine of the full mode Player is used in both cases.</span></span>

<span data-ttu-id="d604d-122">Vous devez définir **AutoStart** sur false immédiatement avant de définir *Player*. **URL**, *Player*. **currentPlaylist** ou *Player*. **currentMedia** dans les apparences et les contrôles du lecteur Windows Media à distance si vous souhaitez vous assurer que l’élément multimédia ne démarre pas immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d604d-122">You should set **autoStart** to false immediately before you set *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** in skins and remoted Windows Media Player controls if you want to ensure that the media item does not start playing immediately.</span></span> <span data-ttu-id="d604d-123">En outre, sauf si vous définissez **AutoStart** sur true juste avant de spécifier un élément multimédia, vous ne devez pas compter sur ce paramètre en remplacement de l’utilisation des *contrôles*. méthode **Play** .</span><span class="sxs-lookup"><span data-stu-id="d604d-123">Also, unless you set **autostart** to true immediately before specifying a media item, you should not rely on this setting as a substitute for using the *Controls*.**play** method.</span></span>

## <a name="examples"></a><span data-ttu-id="d604d-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="d604d-124">Examples</span></span>

<span data-ttu-id="d604d-125">L’exemple suivant crée un élément de case à cocher HTML qui permet à l’utilisateur de spécifier si le contrôle du lecteur doit lire l’élément multimédia en cours automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d604d-125">The following example creates an HTML CHECKBOX element that allows the user to specify whether the Player control plays the current media item automatically.</span></span> <span data-ttu-id="d604d-126">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d604d-126">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX" ID = AS
              onClick = "
    /* Use the CHECKBOX state to specify the value 
       of the autoStart property. */
    Player.settings.autoStart = AS.checked;
"> 

```



## <a name="requirements"></a><span data-ttu-id="d604d-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d604d-127">Requirements</span></span>



| <span data-ttu-id="d604d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d604d-128">Requirement</span></span> | <span data-ttu-id="d604d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="d604d-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d604d-130">Version</span><span class="sxs-lookup"><span data-stu-id="d604d-130">Version</span></span><br/> | <span data-ttu-id="d604d-131">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d604d-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d604d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d604d-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="d604d-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d604d-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d604d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d604d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d604d-135">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="d604d-135">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="d604d-136">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="d604d-136">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="d604d-137">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="d604d-137">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





