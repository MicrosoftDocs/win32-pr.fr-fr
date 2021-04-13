---
title: DVD. up, méthode de menu
description: La méthode de menu principal arrête la lecture du titre et affiche le menu supérieur (ou racine) du titre actuel.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- méthode du menu vers le lecteur Windows Media
- méthode menu du lecteur Windows Media, DVD, classe
- Classe DVD lecteur Windows Media, méthode de menu
topic_type:
- apiref
api_name:
- DVD.topMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be2b0fdafb10039b24f1d77e65f4b105889da85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465750"
---
# <a name="dvdtopmenu-method"></a><span data-ttu-id="f4fe2-106">DVD. up, méthode de menu</span><span class="sxs-lookup"><span data-stu-id="f4fe2-106">DVD.topMenu method</span></span>

<span data-ttu-id="f4fe2-107">La méthode de **menu** principal arrête la lecture du titre et affiche le menu supérieur (ou racine) du titre actuel.</span><span class="sxs-lookup"><span data-stu-id="f4fe2-107">The **topMenu** method stops title playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4fe2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4fe2-108">Syntax</span></span>


```JScript
DVD.topMenu()
```



## <a name="parameters"></a><span data-ttu-id="f4fe2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4fe2-109">Parameters</span></span>

<span data-ttu-id="f4fe2-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f4fe2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4fe2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4fe2-111">Return value</span></span>

<span data-ttu-id="f4fe2-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f4fe2-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4fe2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f4fe2-113">Remarks</span></span>

<span data-ttu-id="f4fe2-114">Chaque DVD est créé différemment.</span><span class="sxs-lookup"><span data-stu-id="f4fe2-114">Every DVD is authored differently.</span></span> <span data-ttu-id="f4fe2-115">Le DVD doit contenir un menu pour que cette méthode fonctionne.</span><span class="sxs-lookup"><span data-stu-id="f4fe2-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="f4fe2-116">Certains DVD sont créés afin que les méthodes **menu** et **titleMenu** ouvrent le même menu.</span><span class="sxs-lookup"><span data-stu-id="f4fe2-116">Some DVDs are authored so that the **topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="f4fe2-117">La méthode de **menu** principal appelle généralement le menu supérieur (ou racine), mais elle peut appeler le menu titre à la place, si aucun menu racine n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="f4fe2-117">The **topMenu** method usually invokes the top (or root) menu but it may invoke the title menu instead, if there is no root menu available.</span></span>

<span data-ttu-id="f4fe2-118">**Lecteur Windows Media 10 Mobile :** Cette méthode fonctionne toujours, mais n’effectue pas l’opération prévue.</span><span class="sxs-lookup"><span data-stu-id="f4fe2-118">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4fe2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4fe2-119">Requirements</span></span>



| <span data-ttu-id="f4fe2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4fe2-120">Requirement</span></span> | <span data-ttu-id="f4fe2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4fe2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4fe2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4fe2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f4fe2-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4fe2-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4fe2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4fe2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f4fe2-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4fe2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f4fe2-126">Version</span><span class="sxs-lookup"><span data-stu-id="f4fe2-126">Version</span></span><br/>                  | <span data-ttu-id="f4fe2-127">Lecteur Windows Media pour Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f4fe2-127">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="f4fe2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f4fe2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4fe2-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4fe2-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4fe2-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4fe2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4fe2-131">**Objet DVD**</span><span class="sxs-lookup"><span data-stu-id="f4fe2-131">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="f4fe2-132">**DVD. titleMenu**</span><span class="sxs-lookup"><span data-stu-id="f4fe2-132">**DVD.titleMenu**</span></span>](dvd-titlemenu.md)
</dt> </dl>

 

 





