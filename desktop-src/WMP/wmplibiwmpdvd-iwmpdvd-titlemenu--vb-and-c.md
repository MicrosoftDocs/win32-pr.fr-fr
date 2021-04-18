---
title: Méthode IWMPDVD titleMenu
description: La méthode titleMenu arrête la lecture et affiche le menu du titre.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- méthode titleMenu lecteur Windows Media
- méthode titleMenu lecteur Windows Media, interface IWMPDVD
- Interface IWMPDVD lecteur Windows Media, méthode titleMenu
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0889a3f65ccefe4e09bb5ff47a66867681dcc801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526440"
---
# <a name="iwmpdvdtitlemenu-method"></a><span data-ttu-id="cf152-106">IWMPDVD :: titleMenu, méthode</span><span class="sxs-lookup"><span data-stu-id="cf152-106">IWMPDVD::titleMenu method</span></span>

<span data-ttu-id="cf152-107">La méthode **titleMenu** arrête la lecture et affiche le menu du titre.</span><span class="sxs-lookup"><span data-stu-id="cf152-107">The **titleMenu** method stops playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf152-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf152-108">Syntax</span></span>


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a><span data-ttu-id="cf152-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf152-109">Parameters</span></span>

<span data-ttu-id="cf152-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="cf152-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf152-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf152-111">Return value</span></span>

<span data-ttu-id="cf152-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cf152-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf152-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cf152-113">Remarks</span></span>

<span data-ttu-id="cf152-114">Chaque DVD est créé différemment.</span><span class="sxs-lookup"><span data-stu-id="cf152-114">Every DVD is authored differently.</span></span> <span data-ttu-id="cf152-115">Le DVD doit contenir un menu pour que cette méthode fonctionne.</span><span class="sxs-lookup"><span data-stu-id="cf152-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="cf152-116">Certains DVD sont créés afin que les méthodes **menu IWMPDVD.** et **titleMenu** ouvrent le même menu.</span><span class="sxs-lookup"><span data-stu-id="cf152-116">Some DVDs are authored so that the **IWMPDVD.topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="cf152-117">La méthode **titleMenu** appelle généralement le menu du titre, mais elle peut appeler le menu supérieur si aucun menu de titre n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="cf152-117">The **titleMenu** method usually invokes the title menu, but it may invoke the top menu if there is no title menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf152-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf152-118">Requirements</span></span>



| <span data-ttu-id="cf152-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf152-119">Requirement</span></span> | <span data-ttu-id="cf152-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf152-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf152-121">Version</span><span class="sxs-lookup"><span data-stu-id="cf152-121">Version</span></span><br/>   | <span data-ttu-id="cf152-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cf152-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cf152-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cf152-123">Namespace</span></span><br/> | <span data-ttu-id="cf152-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cf152-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cf152-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="cf152-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cf152-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cf152-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf152-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf152-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf152-128">**Interface IWMPDVD (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cf152-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf152-129">**Menu IWMPDVD. (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cf152-129">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





