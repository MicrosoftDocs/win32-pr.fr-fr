---
title: Player. launchURL, méthode
description: La méthode launchURL envoie une URL au navigateur par défaut de l’utilisateur à restituer. | Player. launchURL, méthode
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- méthode launchURL lecteur Windows Media
- méthode launchURL lecteur Windows Media, classe Player
- Classe player lecteur Windows Media, méthode launchURL
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527296"
---
# <a name="playerlaunchurl-method"></a><span data-ttu-id="d5148-107">Player. launchURL, méthode</span><span class="sxs-lookup"><span data-stu-id="d5148-107">Player.launchURL method</span></span>

<span data-ttu-id="d5148-108">La méthode **launchURL** envoie une URL au navigateur par défaut de l’utilisateur à restituer.</span><span class="sxs-lookup"><span data-stu-id="d5148-108">The **launchURL** method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5148-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5148-109">Syntax</span></span>


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="d5148-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5148-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5148-111">*URL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5148-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5148-112">Valeur de **chaîne** représentant l’URL à lancer.</span><span class="sxs-lookup"><span data-stu-id="d5148-112">**String** value representing the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5148-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5148-113">Return value</span></span>

<span data-ttu-id="d5148-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d5148-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5148-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d5148-115">Remarks</span></span>

<span data-ttu-id="d5148-116">Cette méthode ouvre uniquement les pages Web à l’aide des protocoles HTTP ou HTTPs.</span><span class="sxs-lookup"><span data-stu-id="d5148-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="d5148-117">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d5148-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="d5148-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="d5148-118">Examples</span></span>

<span data-ttu-id="d5148-119">L’exemple suivant crée un élément bouton HTML qui, lorsque vous cliquez dessus, affiche le site Web Microsoft dans une nouvelle fenêtre de navigateur.</span><span class="sxs-lookup"><span data-stu-id="d5148-119">The following example creates an HTML BUTTON element that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="d5148-120">L’élément **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d5148-120">The **Player** element was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
">

```



## <a name="requirements"></a><span data-ttu-id="d5148-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5148-121">Requirements</span></span>



| <span data-ttu-id="d5148-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5148-122">Requirement</span></span> | <span data-ttu-id="d5148-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5148-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5148-124">Version</span><span class="sxs-lookup"><span data-stu-id="d5148-124">Version</span></span><br/> | <span data-ttu-id="d5148-125">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d5148-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d5148-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d5148-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="d5148-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5148-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5148-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5148-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5148-129">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="d5148-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





