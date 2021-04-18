---
description: La méthode DVDAdm. SaveParentalCountry enregistre le nouveau pays ou la nouvelle région parente de l’application dans le registre.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Méthode SaveParentalCountry (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ca47a6ca10f25298b4eb10fdcf532c8d764b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532881"
---
# <a name="saveparentalcountry-method"></a><span data-ttu-id="8fb88-103">Méthode SaveParentalCountry</span><span class="sxs-lookup"><span data-stu-id="8fb88-103">SaveParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="8fb88-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8fb88-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8fb88-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8fb88-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8fb88-106">La `DVDAdm.SaveParentalCountry` méthode enregistre le nouveau pays ou la nouvelle région parente de l’application dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8fb88-106">The `DVDAdm.SaveParentalCountry` method saves the application's new parental country/region to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="8fb88-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fb88-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fb88-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span><span class="sxs-lookup"><span data-stu-id="8fb88-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="8fb88-109">Spécifie le pays ou la région parente sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="8fb88-109">Specifies the parental country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="8fb88-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="8fb88-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="8fb88-111">Spécifie le nom d’utilisateur sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="8fb88-111">Specifies the user name as a String.</span></span> <span data-ttu-id="8fb88-112">(Actuellement ignoré.)</span><span class="sxs-lookup"><span data-stu-id="8fb88-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="8fb88-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="8fb88-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="8fb88-114">Spécifie le mot de passe sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="8fb88-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fb88-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8fb88-115">Return value</span></span>

<span data-ttu-id="8fb88-116">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="8fb88-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fb88-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8fb88-117">Remarks</span></span>

<span data-ttu-id="8fb88-118">Cette méthode permet à un utilisateur qui connaît le mot de passe actuel d’enregistrer un nouveau paramètre de pays/région parental dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8fb88-118">This method enables a user who knows the current password to save a new parental country/region setting to the registry.</span></span> <span data-ttu-id="8fb88-119">Comme avec toutes les méthodes de **MSDVDAdm**, cette méthode n’affecte pas le niveau actuel dans le lecteur ; il modifie uniquement le paramètre du Registre, de sorte que la prochaine fois que l’objet MSWebDVD est créé, il s’ouvre avec le nouveau pays/région.</span><span class="sxs-lookup"><span data-stu-id="8fb88-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is created, it will open with the new country/region.</span></span> <span data-ttu-id="8fb88-120">Pour modifier le pays ou la région parente dans le lecteur, appelez [**SelectParentalCountry**](selectparentalcountry-method.md), qui ne modifie pas le paramètre de registre.</span><span class="sxs-lookup"><span data-stu-id="8fb88-120">To change the parental country/region in the player, call [**SelectParentalCountry**](selectparentalcountry-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fb88-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fb88-121">Requirements</span></span>



| <span data-ttu-id="8fb88-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fb88-122">Requirement</span></span> | <span data-ttu-id="8fb88-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fb88-123">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb88-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8fb88-124">Header</span></span><br/> | <dl> <span data-ttu-id="8fb88-125"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fb88-125"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fb88-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fb88-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb88-127">**SaveParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="8fb88-127">**SaveParentalLevel**</span></span>](saveparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="8fb88-128">Objet MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="8fb88-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




