---
description: La méthode SelectParentalLevel définit le niveau parental spécifié pour la lecture suivante.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Méthode SelectParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb00172b8e61f353c45981af628eb396bca7a7df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521271"
---
# <a name="selectparentallevel-method"></a><span data-ttu-id="d4d60-103">Méthode SelectParentalLevel</span><span class="sxs-lookup"><span data-stu-id="d4d60-103">SelectParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="d4d60-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d4d60-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d4d60-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d4d60-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d4d60-106">La `SelectParentalLevel` méthode définit le niveau parental spécifié pour la lecture suivante.</span><span class="sxs-lookup"><span data-stu-id="d4d60-106">The `SelectParentalLevel` method sets the specified parental level for subsequent playback.</span></span>

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="d4d60-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4d60-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d60-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span><span class="sxs-lookup"><span data-stu-id="d4d60-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="d4d60-109">Spécifie le niveau de gestion parental sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="d4d60-109">Specifies the parental management level as an Integer.</span></span> <span data-ttu-id="d4d60-110">Pour activer la gestion parentale, le paramètre *iLevel* doit être compris entre 1 et 8.</span><span class="sxs-lookup"><span data-stu-id="d4d60-110">To enable the parental management, the *iLevel* parameter must range from 1 through 8.</span></span> <span data-ttu-id="d4d60-111">Pour désactiver la gestion parentale, affectez la valeur-1 à *iLevel* .</span><span class="sxs-lookup"><span data-stu-id="d4d60-111">To disable the parental management, set *iLevel* to -1.</span></span>

</dd> <dt>

<span data-ttu-id="d4d60-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="d4d60-112"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="d4d60-113">Spécifie l’utilisateur actuel en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="d4d60-113">Specifies the current user as a String.</span></span> <span data-ttu-id="d4d60-114">(Actuellement ignoré.)</span><span class="sxs-lookup"><span data-stu-id="d4d60-114">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="d4d60-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="d4d60-115"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="d4d60-116">Spécifie le mot de passe actuellement stocké dans le Registre sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d4d60-116">Specifies the password currently stored in the registry as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4d60-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d4d60-117">Return Value</span></span>

<span data-ttu-id="d4d60-118">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="d4d60-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4d60-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d4d60-119">Remarks</span></span>

<span data-ttu-id="d4d60-120">Cette méthode définit le niveau d’accès dans l’objet MSWebDVD, qui détermine le contenu que l’utilisateur peut relire.</span><span class="sxs-lookup"><span data-stu-id="d4d60-120">This method sets the access level in the MSWebDVD object, which determines what content the user can play back.</span></span> <span data-ttu-id="d4d60-121">Les niveaux plus élevés peuvent lire du contenu de niveau inférieur, mais les niveaux inférieurs ne peuvent pas lire du contenu de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="d4d60-121">Higher levels can play lower-level content but lower levels can't play higher-level content.</span></span> <span data-ttu-id="d4d60-122">La signification exacte des huit niveaux de gestion parentale des DVD varie en fonction du pays ou de la région.</span><span class="sxs-lookup"><span data-stu-id="d4d60-122">The exact meaning of the eight DVD parental management levels varies depending on the country/region.</span></span> <span data-ttu-id="d4d60-123">Au États-Unis et au Canada, les niveaux sont mappés aux catégories d’évaluation MPAA (motion image Association of America).</span><span class="sxs-lookup"><span data-stu-id="d4d60-123">In the United States and Canada, the levels are mapped to the Motion Picture Association of America (MPAA) rating categories.</span></span> <span data-ttu-id="d4d60-124">La gestion du contrôle parental dans le navigateur DVD est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="d4d60-124">Parental management in the DVD Navigator is disabled by default.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4d60-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4d60-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d60-126">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="d4d60-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="d4d60-127">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="d4d60-127">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="d4d60-128">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="d4d60-128">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="d4d60-129">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="d4d60-129">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="d4d60-130">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="d4d60-130">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="d4d60-131">**AcceptParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="d4d60-131">**AcceptParentalLevelChange**</span></span>](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



