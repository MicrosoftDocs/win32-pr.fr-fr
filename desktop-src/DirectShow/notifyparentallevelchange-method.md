---
description: La méthode NotifyParentalLevelChange active ou désactive la gestion des événements pour les commandes de niveau de gestion parental temporaire.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Méthode NotifyParentalLevelChange (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc47b7d78af8cfdd32aa63361411e769c375ddf1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537503"
---
# <a name="notifyparentallevelchange-method"></a><span data-ttu-id="05960-103">Méthode NotifyParentalLevelChange</span><span class="sxs-lookup"><span data-stu-id="05960-103">NotifyParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="05960-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="05960-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="05960-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="05960-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="05960-106">La `NotifyParentalLevelChange` méthode active ou désactive la gestion des événements pour les commandes de niveau de gestion parental temporaire.</span><span class="sxs-lookup"><span data-stu-id="05960-106">The `NotifyParentalLevelChange` method enables or disables the event handling for temporary parental management level commands.</span></span>

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a><span data-ttu-id="05960-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05960-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05960-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*</span><span class="sxs-lookup"><span data-stu-id="05960-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*</span></span>
</dt> <dd>

<span data-ttu-id="05960-109">Spécifie une valeur booléenne indiquant si l’application est notifiée ou non lorsque l’objet MSWebDVD rencontre des segments vidéo avec une évaluation plus restrictive que l’évaluation générale du disque.</span><span class="sxs-lookup"><span data-stu-id="05960-109">Specifies a Boolean value indicating whether or not the application is notified when the MSWebDVD object encounters video segments with a rating more restrictive than the overall rating for the disc.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05960-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="05960-110">Return Value</span></span>

<span data-ttu-id="05960-111">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="05960-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05960-112">Notes</span><span class="sxs-lookup"><span data-stu-id="05960-112">Remarks</span></span>

<span data-ttu-id="05960-113">Les notifications de gestion parentale sont désactivées par défaut.</span><span class="sxs-lookup"><span data-stu-id="05960-113">Parental management notifications are disabled by default.</span></span> <span data-ttu-id="05960-114">Cela signifie que les commandes parentales temporaires du disque sont autorisées mais ignorées et que le disque est lu sans interruption.</span><span class="sxs-lookup"><span data-stu-id="05960-114">This means that temporary parental commands from the disc are allowed but ignored and disc will play without interruption.</span></span> <span data-ttu-id="05960-115">Appelez cette méthode lors de l’initialisation de votre application si vous devez gérer les commandes de niveau de gestion parental temporaire à partir du disque. Pour désactiver la gestion parentale une fois qu’elle est activée, appelez cette méthode avec un argument ayant la valeur false.</span><span class="sxs-lookup"><span data-stu-id="05960-115">Call this method during initialization of your application if you need to handle temporary parental management level commands from the disc. To disable parental management after it is enabled, call this method with an argument of false.</span></span> <span data-ttu-id="05960-116">Pour plus d’informations sur la gestion parentale, consultez [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).</span><span class="sxs-lookup"><span data-stu-id="05960-116">For more details on parental management, see [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05960-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05960-117">Requirements</span></span>



| <span data-ttu-id="05960-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05960-118">Requirement</span></span> | <span data-ttu-id="05960-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="05960-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="05960-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="05960-120">Header</span></span><br/> | <dl> <span data-ttu-id="05960-121"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="05960-121"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05960-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05960-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05960-123">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="05960-123">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="05960-124">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="05960-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="05960-125">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="05960-125">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="05960-126">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="05960-126">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="05960-127">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="05960-127">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 




