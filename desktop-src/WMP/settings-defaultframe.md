---
title: Paramètres. defaultFrame
description: La propriété defaultFrame spécifie ou récupère le nom du frame utilisé pour afficher une URL reçue dans un événement commande.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Settings. defaultFrame Windows Media Player
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528515"
---
# <a name="settingsdefaultframe"></a><span data-ttu-id="4c4cf-104">Paramètres. defaultFrame</span><span class="sxs-lookup"><span data-stu-id="4c4cf-104">Settings.defaultFrame</span></span>

<span data-ttu-id="4c4cf-105">La propriété **defaultFrame** spécifie ou récupère le nom du frame utilisé pour afficher une URL reçue dans un événement **commande** .</span><span class="sxs-lookup"><span data-stu-id="4c4cf-105">The **defaultFrame** property specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c4cf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c4cf-106">Syntax</span></span>

<span data-ttu-id="4c4cf-107">Player. Settings. defaultFrame</span><span class="sxs-lookup"><span data-stu-id="4c4cf-107">player.settings.defaultFrame</span></span>

## <a name="possible-values"></a><span data-ttu-id="4c4cf-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="4c4cf-108">Possible Values</span></span>

<span data-ttu-id="4c4cf-109">Cette propriété est une **chaîne** en lecture/écriture qui correspond à la valeur de l’attribut **Name** de l’élément Frame cible.</span><span class="sxs-lookup"><span data-stu-id="4c4cf-109">This property is a read/write **String** corresponding to the value of the **name** attribute of the target FRAME element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c4cf-110">Notes</span><span class="sxs-lookup"><span data-stu-id="4c4cf-110">Remarks</span></span>

<span data-ttu-id="4c4cf-111">Si un frame cible est spécifié dans l’événement **commande** lui-même, cette propriété est ignorée.</span><span class="sxs-lookup"><span data-stu-id="4c4cf-111">If a target frame is specified in the **ScriptCommand** event itself, this property is ignored.</span></span>

<span data-ttu-id="4c4cf-112">Cette propriété est ignorée lors de l’utilisation de l’applet Java de Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="4c4cf-112">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="4c4cf-113">Dans le navigateur, chaque commande de script d’URL reçue affiche l’URL dans une nouvelle fenêtre de navigateur, quelle que soit la valeur des *paramètres*. **defaultFrame**.</span><span class="sxs-lookup"><span data-stu-id="4c4cf-113">In Navigator, each URL script command received displays the URL in a new browser window, regardless of the value of *Settings*.**defaultFrame**.</span></span>

<span data-ttu-id="4c4cf-114">**Windows Media Player 10 Mobile**: cette propriété est en lecture seule et retourne toujours une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="4c4cf-114">**Windows Media Player 10 Mobile**: This property is read only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c4cf-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c4cf-115">Requirements</span></span>



| <span data-ttu-id="4c4cf-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c4cf-116">Requirement</span></span> | <span data-ttu-id="4c4cf-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c4cf-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c4cf-118">Version</span><span class="sxs-lookup"><span data-stu-id="4c4cf-118">Version</span></span><br/> | <span data-ttu-id="4c4cf-119">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4c4cf-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4c4cf-120">DLL</span><span class="sxs-lookup"><span data-stu-id="4c4cf-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="4c4cf-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c4cf-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c4cf-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c4cf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c4cf-123">**Événement Player. commande**</span><span class="sxs-lookup"><span data-stu-id="4c4cf-123">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="4c4cf-124">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="4c4cf-124">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="4c4cf-125">**Utilisation de Windows Media Player avec Netscape 7.1**</span><span class="sxs-lookup"><span data-stu-id="4c4cf-125">**Using Windows Media Player with Netscape 7.1**</span></span>](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





