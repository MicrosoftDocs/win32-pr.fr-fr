---
title: Méthode IWMPCdromBurn refreshStatus
description: La méthode refreshStatus met à jour les informations d’état de la sélection de gravure en cours.
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- méthode refreshStatus lecteur Windows Media
- méthode refreshStatus lecteur Windows Media, interface IWMPCdromBurn
- Interface IWMPCdromBurn lecteur Windows Media, méthode refreshStatus
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528808"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a><span data-ttu-id="68104-106">IWMPCdromBurn :: refreshStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="68104-106">IWMPCdromBurn::refreshStatus method</span></span>

<span data-ttu-id="68104-107">La méthode **refreshStatus** met à jour les informations d’état de la sélection de gravure en cours.</span><span class="sxs-lookup"><span data-stu-id="68104-107">The **refreshStatus** method updates the status information for the current burn playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="68104-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68104-108">Syntax</span></span>


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a><span data-ttu-id="68104-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68104-109">Parameters</span></span>

<span data-ttu-id="68104-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="68104-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68104-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="68104-111">Return value</span></span>

<span data-ttu-id="68104-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="68104-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68104-113">Notes</span><span class="sxs-lookup"><span data-stu-id="68104-113">Remarks</span></span>

<span data-ttu-id="68104-114">Vous devez appeler cette méthode après avoir créé ou modifié une sélection de gravure avant de lire les informations d’État ou de graver le CD.</span><span class="sxs-lookup"><span data-stu-id="68104-114">You should call this method after you create or change a burn playlist before reading status information or burning the CD.</span></span> <span data-ttu-id="68104-115">Vous pouvez tester si une actualisation est requise en obtenant la valeur de **burnState** et en vérifiant wmpbsRefreshStatusPending.</span><span class="sxs-lookup"><span data-stu-id="68104-115">You can test whether a refresh is required by getting the value of **burnState** and checking for wmpbsRefreshStatusPending.</span></span>

<span data-ttu-id="68104-116">L’actualisation de l’État est une opération synchrone.</span><span class="sxs-lookup"><span data-stu-id="68104-116">Refreshing the status is a synchronous operation.</span></span> <span data-ttu-id="68104-117">Cela signifie qu’une longue période de temps peut s’écouler avant que cette méthode ne retourne si la sélection de gravure actuelle est volumineuse et contient de nombreuses modifications.</span><span class="sxs-lookup"><span data-stu-id="68104-117">This means that a lengthy period of time might elapse before this method returns if the current burn playlist is large and contains many changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="68104-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68104-118">Requirements</span></span>



| <span data-ttu-id="68104-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68104-119">Requirement</span></span> | <span data-ttu-id="68104-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="68104-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68104-121">Version</span><span class="sxs-lookup"><span data-stu-id="68104-121">Version</span></span><br/>   | <span data-ttu-id="68104-122">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="68104-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="68104-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="68104-123">Namespace</span></span><br/> | <span data-ttu-id="68104-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="68104-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="68104-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="68104-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="68104-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="68104-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68104-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68104-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68104-128">**Interface IWMPCdromBurn (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="68104-128">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="68104-129">**IWMPCdromBurn. burnState (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="68104-129">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="68104-130">**WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="68104-130">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





