---
title: Player. URL
description: La propriété URL spécifie ou récupère le nom de l’élément multimédia à lire.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Lecteur Windows Media Player. URL
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d4f0c75ac0dddeeaced0f1a3a6f1247df4ae36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532589"
---
# <a name="playerurl"></a><span data-ttu-id="9a275-104">Player. URL</span><span class="sxs-lookup"><span data-stu-id="9a275-104">Player.URL</span></span>

<span data-ttu-id="9a275-105">La propriété **URL** spécifie ou récupère le nom de l’élément multimédia à lire.</span><span class="sxs-lookup"><span data-stu-id="9a275-105">The **URL** property specifies or retrieves the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a275-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a275-106">Syntax</span></span>

<span data-ttu-id="9a275-107">*lecteur* . **URL**</span><span class="sxs-lookup"><span data-stu-id="9a275-107">*player* .**URL**</span></span>

## <a name="possible-values"></a><span data-ttu-id="9a275-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="9a275-108">Possible Values</span></span>

<span data-ttu-id="9a275-109">Cette propriété est une **chaîne** en lecture/écriture sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9a275-109">This property is a read/write **String** with no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a275-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9a275-110">Remarks</span></span>

<span data-ttu-id="9a275-111">Cette propriété peut uniquement être définie sur une URL dans une zone de sécurité identique ou moins restrictive que la zone de sécurité du programme ou de la page Web appelante.</span><span class="sxs-lookup"><span data-stu-id="9a275-111">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="9a275-112">Les applications qui ouvrent des éléments multimédias à partir d’un pare-feu offrent de meilleures performances si l’adresse est spécifiée à l’aide du nom DNS (Domain Name Server) au lieu de l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="9a275-112">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="9a275-113">N’appelez pas cette méthode à partir du code du gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="9a275-113">Do not call this method from event handler code.</span></span> <span data-ttu-id="9a275-114">Appelant *Player*. L' **URL** d’un gestionnaire d’événements peut produire des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="9a275-114">Calling *Player*.**URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="9a275-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="9a275-115">Examples</span></span>

<span data-ttu-id="9a275-116">L’exemple suivant crée un élément INPUT de texte HTML et un élément INPUT de bouton HTML.</span><span class="sxs-lookup"><span data-stu-id="9a275-116">The following example creates an HTML TEXT input element and an HTML BUTTON input element.</span></span> <span data-ttu-id="9a275-117">L’élément TEXT permet à l’utilisateur de taper un chemin d’accès pour spécifier un fichier multimédia numérique à lire.</span><span class="sxs-lookup"><span data-stu-id="9a275-117">The TEXT element allows the user to type a path to specify a digital media file to play.</span></span> <span data-ttu-id="9a275-118">L’élément BUTTON exécute JScript qui ouvre le fichier et démarre le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9a275-118">The BUTTON element executes JScript that opens the file and starts Windows Media Player.</span></span> <span data-ttu-id="9a275-119">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9a275-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="9a275-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a275-120">Requirements</span></span>



| <span data-ttu-id="9a275-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a275-121">Requirement</span></span> | <span data-ttu-id="9a275-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a275-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a275-123">Version</span><span class="sxs-lookup"><span data-stu-id="9a275-123">Version</span></span><br/> | <span data-ttu-id="9a275-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9a275-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9a275-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9a275-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="9a275-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a275-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a275-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a275-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a275-128">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="9a275-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





