---
title: DVD. Back, méthode
description: La méthode back retourne l’affichage d’un sous-menu à son menu parent.
ms.assetid: 4b6c3562-6484-4ef0-8c5c-c24d88e02096
keywords:
- méthode back du lecteur Windows Media
- méthode back lecteur Windows Media, DVD, classe
- Classe DVD lecteur Windows Media, méthode back
topic_type:
- apiref
api_name:
- DVD.back
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e656051d02ec5efc74aa7595d2ca6cb20e648f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384667"
---
# <a name="dvdback-method"></a><span data-ttu-id="28524-106">DVD. Back, méthode</span><span class="sxs-lookup"><span data-stu-id="28524-106">DVD.back method</span></span>

<span data-ttu-id="28524-107">La méthode **Back** retourne l’affichage d’un sous-menu à son menu parent.</span><span class="sxs-lookup"><span data-stu-id="28524-107">The **back** method returns the display from a submenu to its parent menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="28524-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28524-108">Syntax</span></span>


```JScript
DVD.back()
```



## <a name="parameters"></a><span data-ttu-id="28524-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28524-109">Parameters</span></span>

<span data-ttu-id="28524-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="28524-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28524-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28524-111">Return value</span></span>

<span data-ttu-id="28524-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="28524-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28524-113">Notes</span><span class="sxs-lookup"><span data-stu-id="28524-113">Remarks</span></span>

<span data-ttu-id="28524-114">Chaque DVD est créé différemment.</span><span class="sxs-lookup"><span data-stu-id="28524-114">Every DVD is authored differently.</span></span> <span data-ttu-id="28524-115">Certains DVD sont créés afin que la méthode **Back** soit disponible dans le menu racine, mais lorsqu’elle est appelée, elle ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="28524-115">Some DVDs are authored so that the **back** method is available from the root menu, but when invoked, it will do nothing.</span></span>

<span data-ttu-id="28524-116">**Lecteur Windows Media 10 Mobile :** Cette méthode fonctionne toujours, mais n’effectue pas l’opération prévue.</span><span class="sxs-lookup"><span data-stu-id="28524-116">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="28524-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28524-117">Requirements</span></span>



| <span data-ttu-id="28524-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28524-118">Requirement</span></span> | <span data-ttu-id="28524-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="28524-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28524-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28524-120">Minimum supported client</span></span><br/> | <span data-ttu-id="28524-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28524-121">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28524-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28524-122">Minimum supported server</span></span><br/> | <span data-ttu-id="28524-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28524-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="28524-124">Version</span><span class="sxs-lookup"><span data-stu-id="28524-124">Version</span></span><br/>                  | <span data-ttu-id="28524-125">Lecteur Windows Media pour Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="28524-125">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="28524-126">DLL</span><span class="sxs-lookup"><span data-stu-id="28524-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28524-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28524-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28524-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28524-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28524-129">**Objet DVD**</span><span class="sxs-lookup"><span data-stu-id="28524-129">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





