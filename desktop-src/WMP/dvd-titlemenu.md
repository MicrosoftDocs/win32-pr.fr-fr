---
title: Méthode DVD. titleMenu
description: La méthode titleMenu arrête la lecture du titre et affiche le menu du titre.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- méthode titleMenu lecteur Windows Media
- méthode titleMenu lecteur Windows Media, DVD, classe
- Classe DVD lecteur Windows Media, méthode titleMenu
topic_type:
- apiref
api_name:
- DVD.titleMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9351603d5307415f57610422a83d3586067bdcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317213"
---
# <a name="dvdtitlemenu-method"></a><span data-ttu-id="f3b71-106">Méthode DVD. titleMenu</span><span class="sxs-lookup"><span data-stu-id="f3b71-106">DVD.titleMenu method</span></span>

<span data-ttu-id="f3b71-107">La méthode **titleMenu** arrête la lecture du titre et affiche le menu du titre.</span><span class="sxs-lookup"><span data-stu-id="f3b71-107">The **titleMenu** method stops title playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b71-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3b71-108">Syntax</span></span>


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a><span data-ttu-id="f3b71-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3b71-109">Parameters</span></span>

<span data-ttu-id="f3b71-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f3b71-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3b71-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3b71-111">Return value</span></span>

<span data-ttu-id="f3b71-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f3b71-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3b71-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f3b71-113">Remarks</span></span>

<span data-ttu-id="f3b71-114">Chaque DVD est créé différemment.</span><span class="sxs-lookup"><span data-stu-id="f3b71-114">Every DVD is authored differently.</span></span> <span data-ttu-id="f3b71-115">Le DVD doit contenir un menu pour que cette méthode fonctionne.</span><span class="sxs-lookup"><span data-stu-id="f3b71-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="f3b71-116">Certains DVD sont créés afin que les méthodes **menu** et **titleMenu** ouvrent le même menu.</span><span class="sxs-lookup"><span data-stu-id="f3b71-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="f3b71-117">La méthode **titleMenu** appelle généralement le menu de titre, mais elle peut appeler le menu supérieur à la place, si aucun menu de titre n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="f3b71-117">The **titleMenu** method usually invokes the title menu but it may invoke the top menu instead, if there is no title menu available.</span></span>

<span data-ttu-id="f3b71-118">**Lecteur Windows Media 10 Mobile :** Cette méthode fonctionne toujours, mais n’effectue pas l’opération prévue.</span><span class="sxs-lookup"><span data-stu-id="f3b71-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b71-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3b71-119">Requirements</span></span>



| <span data-ttu-id="f3b71-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3b71-120">Requirement</span></span> | <span data-ttu-id="f3b71-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3b71-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b71-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3b71-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b71-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3b71-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f3b71-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3b71-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b71-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3b71-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f3b71-126">Version</span><span class="sxs-lookup"><span data-stu-id="f3b71-126">Version</span></span><br/>                  | <span data-ttu-id="f3b71-127">Lecteur Windows Media pour Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f3b71-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="f3b71-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f3b71-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3b71-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3b71-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3b71-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3b71-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b71-131">**Objet DVD**</span><span class="sxs-lookup"><span data-stu-id="f3b71-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="f3b71-132">**Menu DVD.**</span><span class="sxs-lookup"><span data-stu-id="f3b71-132">**DVD.topMenu**</span></span>](dvd-topmenu.md)
</dt> </dl>

 

 





