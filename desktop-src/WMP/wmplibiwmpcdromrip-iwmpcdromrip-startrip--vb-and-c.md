---
title: Méthode IWMPCdromRip startRip
description: La méthode startRip RIP le CD.
ms.assetid: 3569e29c-e593-4bdd-8afb-74e39721cf80
keywords:
- méthode startRip lecteur Windows Media
- méthode startRip lecteur Windows Media, interface IWMPCdromRip
- Interface IWMPCdromRip lecteur Windows Media, méthode startRip
topic_type:
- apiref
api_name:
- IWMPCdromRip.startRip
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327ac9009cf1b8fb9ccfbcc460cde78ef40b3802
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529872"
---
# <a name="iwmpcdromripstartrip-method"></a><span data-ttu-id="b0509-106">IWMPCdromRip :: startRip, méthode</span><span class="sxs-lookup"><span data-stu-id="b0509-106">IWMPCdromRip::startRip method</span></span>

<span data-ttu-id="b0509-107">La méthode **startRip** RIP le CD.</span><span class="sxs-lookup"><span data-stu-id="b0509-107">The **startRip** method rips the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0509-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0509-108">Syntax</span></span>


```CSharp
public void startRip();
```


```VB

Public Sub startRip()
Implements IWMPCdromRip.startRip
```





## <a name="parameters"></a><span data-ttu-id="b0509-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0509-109">Parameters</span></span>

<span data-ttu-id="b0509-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b0509-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0509-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0509-111">Return value</span></span>

<span data-ttu-id="b0509-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b0509-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0509-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b0509-113">Remarks</span></span>

<span data-ttu-id="b0509-114">L’extraction d’un CD à l’aide de l’interface **IWMPCdromRip** a le même effet que l’extraction de musique à l’aide de l’interface utilisateur du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b0509-114">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="b0509-115">Le contenu extrait est automatiquement ajouté à la bibliothèque en fonction des préférences de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b0509-115">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="b0509-116">Pour plus d’informations sur les préférences de l’utilisateur pour l’extraction de CD, consultez « extraction de musique à partir de CD » dans l’aide du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b0509-116">For more information about user preferences for CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0509-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0509-117">Requirements</span></span>



| <span data-ttu-id="b0509-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0509-118">Requirement</span></span> | <span data-ttu-id="b0509-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0509-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0509-120">Version</span><span class="sxs-lookup"><span data-stu-id="b0509-120">Version</span></span><br/>   | <span data-ttu-id="b0509-121">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="b0509-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="b0509-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b0509-122">Namespace</span></span><br/> | <span data-ttu-id="b0509-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b0509-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b0509-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="b0509-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b0509-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b0509-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0509-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0509-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0509-127">**Interface IWMPCdromRip (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b0509-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b0509-128">**IWMPCdromRip.stopRip**</span><span class="sxs-lookup"><span data-stu-id="b0509-128">**IWMPCdromRip.stopRip**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b0509-129">**Extraction d’un CD**</span><span class="sxs-lookup"><span data-stu-id="b0509-129">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





