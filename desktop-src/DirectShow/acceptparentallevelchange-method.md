---
description: La méthode AcceptParentalLevelChange accepte ou rejette le nouveau niveau de gestion parental temporaire.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: Méthode AcceptParentalLevelChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b2e81d1d82c4ede14580ed65d88566738dac1b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515543"
---
# <a name="acceptparentallevelchange-method"></a><span data-ttu-id="15883-103">Méthode AcceptParentalLevelChange</span><span class="sxs-lookup"><span data-stu-id="15883-103">AcceptParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="15883-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="15883-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="15883-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="15883-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="15883-106">La méthode AcceptParentalLevelChange accepte ou rejette le nouveau niveau de gestion parental temporaire.</span><span class="sxs-lookup"><span data-stu-id="15883-106">The AcceptParentalLevelChange method accepts or rejects the new temporary parental management level.</span></span>

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a><span data-ttu-id="15883-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15883-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15883-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*</span><span class="sxs-lookup"><span data-stu-id="15883-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*</span></span>
</dt> <dd>

<span data-ttu-id="15883-109">Spécifie le nouveau niveau parental en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="15883-109">Specifies the new parental level as a Boolean value.</span></span>



| <span data-ttu-id="15883-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="15883-110">Value</span></span> | <span data-ttu-id="15883-111">Description</span><span class="sxs-lookup"><span data-stu-id="15883-111">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="15883-112">true</span><span class="sxs-lookup"><span data-stu-id="15883-112">true</span></span>  | <span data-ttu-id="15883-113">Acceptez le nouveau niveau de gestion parental.</span><span class="sxs-lookup"><span data-stu-id="15883-113">Accept the new parental management level.</span></span> |
| <span data-ttu-id="15883-114">false</span><span class="sxs-lookup"><span data-stu-id="15883-114">false</span></span> | <span data-ttu-id="15883-115">Rejetez le nouveau niveau de gestion parental.</span><span class="sxs-lookup"><span data-stu-id="15883-115">Reject the new parental management level.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15883-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="15883-116">Return Value</span></span>

<span data-ttu-id="15883-117">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="15883-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15883-118">Notes</span><span class="sxs-lookup"><span data-stu-id="15883-118">Remarks</span></span>

<span data-ttu-id="15883-119">Appelez cette méthode en réponse à une \_ notification d’événement de modification du niveau parental du DVD EC \_ \_ \_ pour spécifier si le navigateur DVD doit lire le contenu avec le nouveau niveau parental, ou créer une branche vers l’emplacement où le disque spécifie si le nouveau niveau est rejeté.</span><span class="sxs-lookup"><span data-stu-id="15883-119">Call this method in response to an EC\_DVD\_PARENTAL\_LEVEL\_CHANGE event notification to specify whether the DVD Navigator should play the content with the new parental level, or branch to where the disc specifies if the new level is rejected.</span></span>

## <a name="see-also"></a><span data-ttu-id="15883-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15883-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15883-121">Application des niveaux de gestion parentale</span><span class="sxs-lookup"><span data-stu-id="15883-121">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
</dt> <dt>

[<span data-ttu-id="15883-122">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="15883-122">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="15883-123">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="15883-123">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="15883-124">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="15883-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="15883-125">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="15883-125">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="15883-126">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="15883-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="15883-127">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="15883-127">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



