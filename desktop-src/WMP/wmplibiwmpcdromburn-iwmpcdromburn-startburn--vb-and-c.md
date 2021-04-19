---
title: Méthode IWMPCdromBurn startBurn
description: La méthode startBurn grave le CD.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- méthode startBurn lecteur Windows Media
- méthode startBurn lecteur Windows Media, interface IWMPCdromBurn
- Interface IWMPCdromBurn lecteur Windows Media, méthode startBurn
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe185d8993286e4be3935b43f6c1e9757623309d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521606"
---
# <a name="iwmpcdromburnstartburn-method"></a><span data-ttu-id="d867a-106">IWMPCdromBurn :: startBurn, méthode</span><span class="sxs-lookup"><span data-stu-id="d867a-106">IWMPCdromBurn::startBurn method</span></span>

<span data-ttu-id="d867a-107">La méthode **startBurn** grave le CD.</span><span class="sxs-lookup"><span data-stu-id="d867a-107">The **startBurn** method burns the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="d867a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d867a-108">Syntax</span></span>


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a><span data-ttu-id="d867a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d867a-109">Parameters</span></span>

<span data-ttu-id="d867a-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d867a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d867a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d867a-111">Return value</span></span>

<span data-ttu-id="d867a-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d867a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d867a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d867a-113">Remarks</span></span>

<span data-ttu-id="d867a-114">La valeur de **burnstate** doit être WmpbsReady ou wmpbsStopped avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d867a-114">The value of **burnstate** should be wmpbsReady or wmpbsStopped before calling this method.</span></span>

<span data-ttu-id="d867a-115">Cette méthode ne fonctionne pas si le lecteur de CD n’est pas un graveur, ou si le disque du lecteur n’est pas accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="d867a-115">This method will not work if the CD drive is not a burner, or if the disc in the drive is not writable.</span></span> <span data-ttu-id="d867a-116">Utilisez **isAvailable** pour déterminer si un CD peut être gravé.</span><span class="sxs-lookup"><span data-stu-id="d867a-116">Use **isAvailable** to determine whether a CD can be burned.</span></span>

## <a name="requirements"></a><span data-ttu-id="d867a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d867a-117">Requirements</span></span>



| <span data-ttu-id="d867a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d867a-118">Requirement</span></span> | <span data-ttu-id="d867a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d867a-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d867a-120">Version</span><span class="sxs-lookup"><span data-stu-id="d867a-120">Version</span></span><br/>   | <span data-ttu-id="d867a-121">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="d867a-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="d867a-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d867a-122">Namespace</span></span><br/> | <span data-ttu-id="d867a-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d867a-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d867a-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="d867a-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d867a-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d867a-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d867a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d867a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d867a-127">**Interface IWMPCdromBurn (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d867a-127">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d867a-128">**IWMPCdromBurn. burnState (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d867a-128">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d867a-129">**IWMPCdromBurn. isAvailable (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d867a-129">**IWMPCdromBurn.isAvailable (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d867a-130">**IWMPCdromBurn. stopBurn (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d867a-130">**IWMPCdromBurn.stopBurn (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





