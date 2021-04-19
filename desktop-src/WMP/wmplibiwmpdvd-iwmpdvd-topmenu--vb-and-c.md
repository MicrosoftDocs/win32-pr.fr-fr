---
title: IWMPDVD, méthode de menu
description: La méthode de menu principal arrête la lecture et affiche le menu supérieur (ou racine) du titre actuel.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- méthode du menu vers le lecteur Windows Media
- méthode menu du lecteur Windows Media, interface IWMPDVD
- Interface IWMPDVD lecteur Windows Media, méthode de menu
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531098"
---
# <a name="iwmpdvdtopmenu-method"></a><span data-ttu-id="c38f1-106">IWMPDVD :: keymenu, méthode</span><span class="sxs-lookup"><span data-stu-id="c38f1-106">IWMPDVD::topMenu method</span></span>

<span data-ttu-id="c38f1-107">La méthode de **menu** principal arrête la lecture et affiche le menu supérieur (ou racine) du titre actuel.</span><span class="sxs-lookup"><span data-stu-id="c38f1-107">The **topMenu** method stops playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="c38f1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c38f1-108">Syntax</span></span>


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a><span data-ttu-id="c38f1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c38f1-109">Parameters</span></span>

<span data-ttu-id="c38f1-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c38f1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c38f1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c38f1-111">Return value</span></span>

<span data-ttu-id="c38f1-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c38f1-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c38f1-113">Notes</span><span class="sxs-lookup"><span data-stu-id="c38f1-113">Remarks</span></span>

<span data-ttu-id="c38f1-114">Chaque DVD est créé différemment.</span><span class="sxs-lookup"><span data-stu-id="c38f1-114">Every DVD is authored differently.</span></span> <span data-ttu-id="c38f1-115">Le DVD doit contenir un menu pour que cette méthode fonctionne.</span><span class="sxs-lookup"><span data-stu-id="c38f1-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="c38f1-116">Certains DVD sont créés afin que les méthodes **menu** et **IWMPDVD. titleMenu** ouvrent le même menu.</span><span class="sxs-lookup"><span data-stu-id="c38f1-116">Some DVDs are authored so that the **topMenu** and **IWMPDVD.titleMenu** methods open the same menu.</span></span> <span data-ttu-id="c38f1-117">La méthode de **menu** principal appelle généralement le menu supérieur (ou racine), mais elle peut appeler le menu de titre si aucun menu racine n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="c38f1-117">The **topMenu** method usually invokes the top (or root) menu, but it may invoke the title menu if there is no root menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="c38f1-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c38f1-118">Requirements</span></span>



| <span data-ttu-id="c38f1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c38f1-119">Requirement</span></span> | <span data-ttu-id="c38f1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="c38f1-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c38f1-121">Version</span><span class="sxs-lookup"><span data-stu-id="c38f1-121">Version</span></span><br/>   | <span data-ttu-id="c38f1-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c38f1-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c38f1-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c38f1-123">Namespace</span></span><br/> | <span data-ttu-id="c38f1-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c38f1-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c38f1-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="c38f1-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c38f1-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c38f1-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c38f1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c38f1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c38f1-128">**Interface IWMPDVD (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c38f1-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c38f1-129">**IWMPDVD. titleMenu (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c38f1-129">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





