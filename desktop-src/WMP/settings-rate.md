---
title: Settings. rate
description: La propriété rate spécifie ou récupère la vitesse de lecture actuelle des médias vidéo.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Paramètres. Vitesse du lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings.rate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61287789487fddbe7e77fba5fc033d3103aecb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539638"
---
# <a name="settingsrate"></a><span data-ttu-id="d7d21-104">Settings. rate</span><span class="sxs-lookup"><span data-stu-id="d7d21-104">Settings.rate</span></span>

<span data-ttu-id="d7d21-105">La propriété **rate** spécifie ou récupère la vitesse de lecture actuelle des médias vidéo.</span><span class="sxs-lookup"><span data-stu-id="d7d21-105">The **rate** property specifies or retrieves the current playback rate of video media.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7d21-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7d21-106">Syntax</span></span>

<span data-ttu-id="d7d21-107">Player. Settings. rate</span><span class="sxs-lookup"><span data-stu-id="d7d21-107">player.settings.rate</span></span>

## <a name="possible-values"></a><span data-ttu-id="d7d21-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="d7d21-108">Possible Values</span></span>

<span data-ttu-id="d7d21-109">Cette propriété est un **nombre** en lecture/écriture (**double**) avec une valeur par défaut de 1,0.</span><span class="sxs-lookup"><span data-stu-id="d7d21-109">This property is a read/write **Number** (**double**) with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7d21-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d7d21-110">Remarks</span></span>

<span data-ttu-id="d7d21-111">Cette propriété agit comme une valeur de multiplicateur qui vous permet de lire un clip à un débit plus rapide ou plus lent.</span><span class="sxs-lookup"><span data-stu-id="d7d21-111">This property acts as a multiplier value that allows you to play a clip at a faster or slower rate.</span></span> <span data-ttu-id="d7d21-112">La valeur par défaut 1,0 indique la vitesse créée.</span><span class="sxs-lookup"><span data-stu-id="d7d21-112">The default value of 1.0 indicates the authored speed.</span></span> <span data-ttu-id="d7d21-113">Notez qu’une piste audio devient difficile à comprendre à des vitesses inférieures à 0,5 ou supérieures à 1,5.</span><span class="sxs-lookup"><span data-stu-id="d7d21-113">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="d7d21-114">Un taux de lecture de 2 équivaut à deux fois la vitesse de lecture normale.</span><span class="sxs-lookup"><span data-stu-id="d7d21-114">A playback rate of 2 equates to twice the normal playback speed.</span></span>

<span data-ttu-id="d7d21-115">Le lecteur Windows Media tentera d’utiliser le plus efficace de quatre modes de lecture différents.</span><span class="sxs-lookup"><span data-stu-id="d7d21-115">Windows Media Player will attempt to use the most effective of four different playback modes.</span></span> <span data-ttu-id="d7d21-116">Il s’agit d’une lecture vidéo en douceur avec un son de conservation, une lecture vidéo en douceur avec un son non géré, une lecture vidéo fluide sans audio et une lecture vidéo d’image clé sans audio.</span><span class="sxs-lookup"><span data-stu-id="d7d21-116">These modes are smooth video playback with audio pitch maintained, smooth video playback with audio pitch not maintained, smooth video playback with no audio, and keyframe video playback with no audio.</span></span> <span data-ttu-id="d7d21-117">Le mode choisi par le joueur dépend de nombreux facteurs, notamment le type de fichier et l’emplacement, le système d’exploitation, le réseau et le serveur.</span><span class="sxs-lookup"><span data-stu-id="d7d21-117">The mode chosen by the Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="d7d21-118">D’autres considérations s’appliquent également, en fonction du type de média :</span><span class="sxs-lookup"><span data-stu-id="d7d21-118">Other considerations apply as well, depending on media type:</span></span>

-   <span data-ttu-id="d7d21-119">Fichiers WMV (Windows Media Format) et ASF : les valeurs optimales pour cette propriété sont comprises entre 1 et 10, ou entre 1 et 10 pour la lecture inversée.</span><span class="sxs-lookup"><span data-stu-id="d7d21-119">Windows Media Format (WMV) and ASF files: Optimal values for this property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="d7d21-120">Les valeurs comprises entre 0,5 et 1,0 ou de-0,5 à-1,0 peuvent également fonctionner correctement dans les cas où la tonalité audio peut être conservée, par exemple, lors de la lecture de fichiers situés sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d7d21-120">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, for example, when playing files located on the local computer.</span></span> <span data-ttu-id="d7d21-121">Les valeurs avec une magnitude absolue supérieure à 10 sont autorisées, mais elles ne sont pas très explicites.</span><span class="sxs-lookup"><span data-stu-id="d7d21-121">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="d7d21-122">Autres types de médias vidéo : cette propriété peut être comprise entre 0 et 9.</span><span class="sxs-lookup"><span data-stu-id="d7d21-122">Other Video Media Types: This property can range from 0 to 9.</span></span> <span data-ttu-id="d7d21-123">Les valeurs négatives ne sont pas autorisées.</span><span class="sxs-lookup"><span data-stu-id="d7d21-123">Negative values are not allowed.</span></span> <span data-ttu-id="d7d21-124">Les valeurs inférieures à 1 représentent un mouvement lent.</span><span class="sxs-lookup"><span data-stu-id="d7d21-124">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="d7d21-125">Les valeurs supérieures à 9 sont autorisées, mais elles ne sont pas très explicites.</span><span class="sxs-lookup"><span data-stu-id="d7d21-125">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="d7d21-126">*Contrôles*. la méthode **fastForward** remplace la valeur de **rate** par 5,0, tandis que les *contrôles*. la méthode **fastReverse** change le **taux** sur 5,0.</span><span class="sxs-lookup"><span data-stu-id="d7d21-126">The *Controls*.**fastForward** method changes the value of **rate** to 5.0, while the *Controls*.**fastReverse** method changes **rate** to  5.0.</span></span>

<span data-ttu-id="d7d21-127">La vitesse de lecture de certains types de média ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="d7d21-127">The playback rate of some media types cannot be altered.</span></span> <span data-ttu-id="d7d21-128">Utilisez les *paramètres*. méthode **isAvailable** pour déterminer si cette propriété peut être spécifiée pour un élément multimédia particulier.</span><span class="sxs-lookup"><span data-stu-id="d7d21-128">Use the *Settings*.**isAvailable** method to determine whether this property can be specified for a particular media item.</span></span>

<span data-ttu-id="d7d21-129">**Windows Media Player 10 Mobile**: cette propriété accepte ou retourne uniquement les valeurs-5,0, 1,0 ou 5,0.</span><span class="sxs-lookup"><span data-stu-id="d7d21-129">**Windows Media Player 10 Mobile**: This property only accepts or returns values of -5.0, 1.0, or 5.0.</span></span>

## <a name="examples"></a><span data-ttu-id="d7d21-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="d7d21-130">Examples</span></span>

<span data-ttu-id="d7d21-131">L’exemple suivant crée un élément SELECT HTML qui permet à l’utilisateur de modifier la vitesse de lecture du média actuel.</span><span class="sxs-lookup"><span data-stu-id="d7d21-131">The following example creates an HTML SELECT element that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="d7d21-132">Les options de sélection offrent des taux de lecture à vitesse normale, à demi-vitesse et à vitesse double.</span><span class="sxs-lookup"><span data-stu-id="d7d21-132">The SELECT options offer normal speed, half -speed and double-speed playback rates.</span></span> <span data-ttu-id="d7d21-133">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d7d21-133">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create the HTML SELECT element. -->
<SELECT  ID = pbRATE  NAME = "pbRATE"  LANGUAGE="JScript"
         onChange="
                   /* Test whether playback rate can be set. */
                   if(Player.settings.IsAvailable('Rate'))

                   /* Set the playback rate based on the current
                      value of the SELECT element. */
                   Player.settings.rate = this.value
">

/* Create the OPTION list. */
<OPTION VALUE = 1>NORMAL</OPTION>
<OPTION VALUE = .5>half speed</OPTION>
<OPTION VALUE = 2>2 speed</OPTION>
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="d7d21-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7d21-134">Requirements</span></span>



| <span data-ttu-id="d7d21-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7d21-135">Requirement</span></span> | <span data-ttu-id="d7d21-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7d21-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d21-137">Version</span><span class="sxs-lookup"><span data-stu-id="d7d21-137">Version</span></span><br/> | <span data-ttu-id="d7d21-138">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d7d21-138">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d7d21-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d7d21-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="d7d21-140"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7d21-140"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7d21-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7d21-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7d21-142">**Controls. fastForward**</span><span class="sxs-lookup"><span data-stu-id="d7d21-142">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="d7d21-143">**Controls. fastReverse**</span><span class="sxs-lookup"><span data-stu-id="d7d21-143">**Controls.fastReverse**</span></span>](controls-fastreverse.md)
</dt> <dt>

[<span data-ttu-id="d7d21-144">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="d7d21-144">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="d7d21-145">**Settings. isAvailable**</span><span class="sxs-lookup"><span data-stu-id="d7d21-145">**Settings.isAvailable**</span></span>](settings-isavailable.md)
</dt> </dl>

 

 





