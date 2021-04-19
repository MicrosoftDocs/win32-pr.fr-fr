---
title: IWMPCdromBurn, méthode d’effacement
description: La méthode Erase efface le CD actuel.
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- méthode Erase Windows Media Player
- méthode Erase lecteur Windows Media, interface IWMPCdromBurn
- Interface IWMPCdromBurn lecteur Windows Media, méthode Erase
topic_type:
- apiref
api_name:
- IWMPCdromBurn.erase
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4e168142a6ee77081871bb7dbefa79de8031d71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521607"
---
# <a name="iwmpcdromburnerase-method"></a><span data-ttu-id="69bcd-106">IWMPCdromBurn :: Erase, méthode</span><span class="sxs-lookup"><span data-stu-id="69bcd-106">IWMPCdromBurn::erase method</span></span>

<span data-ttu-id="69bcd-107">La méthode **Erase** efface le CD actuel.</span><span class="sxs-lookup"><span data-stu-id="69bcd-107">The **erase** method erases the current CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="69bcd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69bcd-108">Syntax</span></span>


```CSharp
public void erase();
```


```VB

Public Sub erase()
Implements IWMPCdromBurn.erase
```





## <a name="parameters"></a><span data-ttu-id="69bcd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69bcd-109">Parameters</span></span>

<span data-ttu-id="69bcd-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="69bcd-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="69bcd-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69bcd-111">Return value</span></span>

<span data-ttu-id="69bcd-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="69bcd-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69bcd-113">Notes</span><span class="sxs-lookup"><span data-stu-id="69bcd-113">Remarks</span></span>

<span data-ttu-id="69bcd-114">Cette méthode ne fonctionne pas si le disque du lecteur n’est pas réinscriptible.</span><span class="sxs-lookup"><span data-stu-id="69bcd-114">This method will not work if the disc in the drive is not rewritable.</span></span> <span data-ttu-id="69bcd-115">Utilisez [IWMPCdromBurn. isAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) pour déterminer si un CD peut être effacé.</span><span class="sxs-lookup"><span data-stu-id="69bcd-115">Use [IWMPCdromBurn.isAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) to determine whether a CD can be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="69bcd-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69bcd-116">Requirements</span></span>



| <span data-ttu-id="69bcd-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69bcd-117">Requirement</span></span> | <span data-ttu-id="69bcd-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="69bcd-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69bcd-119">Version</span><span class="sxs-lookup"><span data-stu-id="69bcd-119">Version</span></span><br/>   | <span data-ttu-id="69bcd-120">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="69bcd-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="69bcd-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="69bcd-121">Namespace</span></span><br/> | <span data-ttu-id="69bcd-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="69bcd-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="69bcd-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="69bcd-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="69bcd-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="69bcd-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69bcd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69bcd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69bcd-126">**Interface IWMPCdromBurn (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="69bcd-126">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





