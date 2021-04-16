---
description: La méthode SelectParentalCountry définit le pays ou la région parente spécifiés pour la lecture suivante.
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: Méthode SelectParentalCountry
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2216d2b2ed72436aca003b42cbf811c8a01bd8fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522180"
---
# <a name="selectparentalcountry-method"></a><span data-ttu-id="5eb26-103">Méthode SelectParentalCountry</span><span class="sxs-lookup"><span data-stu-id="5eb26-103">SelectParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="5eb26-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5eb26-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5eb26-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5eb26-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5eb26-106">La `SelectParentalCountry` méthode définit le pays ou la région parente spécifiés pour la lecture suivante.</span><span class="sxs-lookup"><span data-stu-id="5eb26-106">The `SelectParentalCountry` method sets the specified parental country/region for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="5eb26-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5eb26-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eb26-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span><span class="sxs-lookup"><span data-stu-id="5eb26-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="5eb26-109">Spécifie le pays ou la région sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="5eb26-109">Specifies the country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="5eb26-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="5eb26-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="5eb26-111">Spécifie l’utilisateur actuellement connecté en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="5eb26-111">Specifies the current logged-on user as a String.</span></span> <span data-ttu-id="5eb26-112">(Actuellement ignoré.)</span><span class="sxs-lookup"><span data-stu-id="5eb26-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="5eb26-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="5eb26-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="5eb26-114">Spécifie la chaîne de mot de passe de l’application.</span><span class="sxs-lookup"><span data-stu-id="5eb26-114">Specifies the application password String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5eb26-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5eb26-115">Return Value</span></span>

<span data-ttu-id="5eb26-116">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5eb26-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eb26-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5eb26-117">Remarks</span></span>

<span data-ttu-id="5eb26-118">Le pays/région parental détermine la façon dont les niveaux de contrôle parental sont interprétés.</span><span class="sxs-lookup"><span data-stu-id="5eb26-118">The parental country/region determines how the parental levels are interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="5eb26-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5eb26-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eb26-120">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="5eb26-120">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="5eb26-121">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="5eb26-121">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="5eb26-122">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="5eb26-122">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="5eb26-123">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="5eb26-123">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="5eb26-124">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="5eb26-124">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="5eb26-125">**AcceptParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="5eb26-125">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



