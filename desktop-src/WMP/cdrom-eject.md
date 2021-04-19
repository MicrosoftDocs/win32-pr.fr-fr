---
title: Cdrom. EJECT, méthode
description: La méthode EJECT éjecte le CD ou DVD du lecteur. | Cdrom. EJECT, méthode
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- méthode EJECT lecteur Windows Media
- EJECT, méthode lecteur Windows Media, classe cdrom
- Classe cdrom lecteur Windows Media, méthode EJECT
topic_type:
- apiref
api_name:
- Cdrom.eject
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78326ca57dcf097344fc073681fae772222ea9ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531491"
---
# <a name="cdromeject-method"></a><span data-ttu-id="73052-107">Cdrom. EJECT, méthode</span><span class="sxs-lookup"><span data-stu-id="73052-107">Cdrom.eject method</span></span>

<span data-ttu-id="73052-108">La méthode **EJECT** éjecte le CD ou DVD du lecteur.</span><span class="sxs-lookup"><span data-stu-id="73052-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="73052-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73052-109">Syntax</span></span>


```JScript
Cdrom.eject()
```



## <a name="parameters"></a><span data-ttu-id="73052-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73052-110">Parameters</span></span>

<span data-ttu-id="73052-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="73052-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="73052-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73052-112">Return value</span></span>

<span data-ttu-id="73052-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="73052-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="73052-114">Notes</span><span class="sxs-lookup"><span data-stu-id="73052-114">Remarks</span></span>

<span data-ttu-id="73052-115">Si le loquet du lecteur est ouvert, cette méthode ferme la porte.</span><span class="sxs-lookup"><span data-stu-id="73052-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="73052-116">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="73052-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="73052-117">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="73052-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="73052-118">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="73052-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="73052-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="73052-119">Examples</span></span>

<span data-ttu-id="73052-120">L’exemple suivant crée un élément Button HTML qui utilise *cdrom*. **éjectez** pour ouvrir la porte du lecteur qui a l’index de spécificateur de lecteur zéro.</span><span class="sxs-lookup"><span data-stu-id="73052-120">The following example creates an HTML button element that uses *Cdrom*.**eject** to open the door of the drive that has drive specifier index zero.</span></span> <span data-ttu-id="73052-121">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="73052-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"
       NAME = "EJECTBUTTON"
       VALUE = "EJECT"
       OnClick =  "Player.cdromCollection.item(0).eject()"
>
```



## <a name="requirements"></a><span data-ttu-id="73052-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73052-122">Requirements</span></span>



| <span data-ttu-id="73052-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73052-123">Requirement</span></span> | <span data-ttu-id="73052-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="73052-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73052-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73052-125">Minimum supported client</span></span><br/> | <span data-ttu-id="73052-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73052-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73052-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73052-127">Minimum supported server</span></span><br/> | <span data-ttu-id="73052-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73052-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="73052-129">Version</span><span class="sxs-lookup"><span data-stu-id="73052-129">Version</span></span><br/>                  | <span data-ttu-id="73052-130">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="73052-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="73052-131">DLL</span><span class="sxs-lookup"><span data-stu-id="73052-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73052-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73052-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73052-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73052-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73052-134">**Objet cdrom**</span><span class="sxs-lookup"><span data-stu-id="73052-134">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="73052-135">**Player. lecture**</span><span class="sxs-lookup"><span data-stu-id="73052-135">**Player.playState**</span></span>](player-playstate.md)
</dt> <dt>

[<span data-ttu-id="73052-136">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="73052-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="73052-137">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="73052-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





