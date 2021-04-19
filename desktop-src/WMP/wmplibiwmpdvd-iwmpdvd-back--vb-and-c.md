---
title: IWMPDVD méthode back
description: La méthode back remplace l’affichage d’un sous-menu par son menu parent.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- méthode back du lecteur Windows Media
- méthode back du lecteur Windows Media, interface IWMPDVD
- Interface IWMPDVD lecteur Windows Media, méthode back
topic_type:
- apiref
api_name:
- IWMPDVD.back
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cd31cd6365843a6905760c4447ea679e15e70ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542742"
---
# <a name="iwmpdvdback-method"></a><span data-ttu-id="b6815-106">IWMPDVD :: Back, méthode</span><span class="sxs-lookup"><span data-stu-id="b6815-106">IWMPDVD::back method</span></span>

<span data-ttu-id="b6815-107">La méthode **Back** remplace l’affichage d’un sous-menu par son menu parent.</span><span class="sxs-lookup"><span data-stu-id="b6815-107">The **back** method changes the display from a submenu to its parent menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6815-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6815-108">Syntax</span></span>


```CSharp
public void back();
```


```VB

Public Sub back()
Implements IWMPDVD.back
```





## <a name="parameters"></a><span data-ttu-id="b6815-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6815-109">Parameters</span></span>

<span data-ttu-id="b6815-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b6815-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6815-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6815-111">Return value</span></span>

<span data-ttu-id="b6815-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b6815-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6815-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b6815-113">Remarks</span></span>

<span data-ttu-id="b6815-114">Chaque DVD est créé différemment.</span><span class="sxs-lookup"><span data-stu-id="b6815-114">Every DVD is authored differently.</span></span> <span data-ttu-id="b6815-115">Certains DVD sont créés afin que la `back` méthode soit disponible dans le menu racine, mais lorsqu’elle est appelée, elle ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="b6815-115">Some DVDs are authored so that the `back` method is available from the root menu, but when invoked, it will do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6815-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6815-116">Requirements</span></span>



| <span data-ttu-id="b6815-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6815-117">Requirement</span></span> | <span data-ttu-id="b6815-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6815-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6815-119">Version</span><span class="sxs-lookup"><span data-stu-id="b6815-119">Version</span></span><br/>   | <span data-ttu-id="b6815-120">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b6815-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b6815-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b6815-121">Namespace</span></span><br/> | <span data-ttu-id="b6815-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b6815-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b6815-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="b6815-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b6815-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b6815-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6815-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6815-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6815-126">**Interface IWMPDVD (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b6815-126">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





