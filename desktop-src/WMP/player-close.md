---
title: Player. Close, méthode
description: La méthode Close libère les ressources du lecteur Windows Media.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- méthode Close lecteur Windows Media
- méthode Close lecteur Windows Media, classe Player
- Classe player lecteur Windows Media, méthode Close
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542634"
---
# <a name="playerclose-method"></a><span data-ttu-id="61e21-106">Player. Close, méthode</span><span class="sxs-lookup"><span data-stu-id="61e21-106">Player.close method</span></span>

<span data-ttu-id="61e21-107">La méthode **Close** libère les ressources du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="61e21-107">The **close** method releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="61e21-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61e21-108">Syntax</span></span>


```JScript
Player.close()
```



## <a name="parameters"></a><span data-ttu-id="61e21-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61e21-109">Parameters</span></span>

<span data-ttu-id="61e21-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="61e21-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="61e21-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61e21-111">Return value</span></span>

<span data-ttu-id="61e21-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="61e21-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61e21-113">Notes</span><span class="sxs-lookup"><span data-stu-id="61e21-113">Remarks</span></span>

<span data-ttu-id="61e21-114">Cette méthode ferme le fichier multimédia numérique en cours, et non le lecteur Windows Media lui-même.</span><span class="sxs-lookup"><span data-stu-id="61e21-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="61e21-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="61e21-115">Examples</span></span>

<span data-ttu-id="61e21-116">L’exemple suivant crée un élément bouton HTML qui, lorsque vous cliquez dessus, arrête la lecture dans le lecteur Windows Media et libère les ressources en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="61e21-116">The following example creates an HTML BUTTON element that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="61e21-117">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="61e21-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a><span data-ttu-id="61e21-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61e21-118">Requirements</span></span>



| <span data-ttu-id="61e21-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61e21-119">Requirement</span></span> | <span data-ttu-id="61e21-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="61e21-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="61e21-121">Version</span><span class="sxs-lookup"><span data-stu-id="61e21-121">Version</span></span><br/> | <span data-ttu-id="61e21-122">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="61e21-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="61e21-123">DLL</span><span class="sxs-lookup"><span data-stu-id="61e21-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="61e21-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61e21-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61e21-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61e21-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61e21-126">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="61e21-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





