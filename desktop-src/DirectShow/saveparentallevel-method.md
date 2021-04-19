---
description: La méthode DVDAdm. SaveParentalLevel enregistre un nouveau niveau parental par défaut dans le registre.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Méthode SaveParentalLevel (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537094"
---
# <a name="saveparentallevel-method"></a><span data-ttu-id="5a1f6-103">Méthode SaveParentalLevel</span><span class="sxs-lookup"><span data-stu-id="5a1f6-103">SaveParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="5a1f6-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="5a1f6-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="5a1f6-106">La méthode **DVDAdm. SaveParentalLevel** enregistre un nouveau niveau parental par défaut dans le registre.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-106">The **DVDAdm.SaveParentalLevel** method saves a new default parental level to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="5a1f6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a1f6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a1f6-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span><span class="sxs-lookup"><span data-stu-id="5a1f6-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="5a1f6-109">Spécifie le niveau parental comme valeur anInteger comprise entre 1 et 8.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-109">Specifies the parental level as anInteger value from 1 through 8.</span></span>

</dd> <dt>

<span data-ttu-id="5a1f6-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="5a1f6-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="5a1f6-111">Spécifie le nom d’utilisateur sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-111">Specifies the user name as a String.</span></span> <span data-ttu-id="5a1f6-112">(Actuellement ignoré.)</span><span class="sxs-lookup"><span data-stu-id="5a1f6-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="5a1f6-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="5a1f6-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="5a1f6-114">Spécifie le mot de passe sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a1f6-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5a1f6-115">Return Value</span></span>

<span data-ttu-id="5a1f6-116">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a1f6-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5a1f6-117">Remarks</span></span>

<span data-ttu-id="5a1f6-118">Cette méthode permet à un utilisateur qui connaît le mot de passe actuel d’enregistrer un nouveau paramètre de niveau parental dans le registre.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-118">This method enables a user who knows the current password to save a new parental level setting to the registry.</span></span> <span data-ttu-id="5a1f6-119">Comme avec toutes les méthodes de **MSDVDAdm**, cette méthode n’affecte pas le niveau actuel dans le lecteur ; il modifie uniquement le paramètre du Registre, de sorte que la prochaine fois que l’objet MSWebDVD est démarré, il s’ouvre avec le nouveau niveau.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is started, it will open with the new level.</span></span> <span data-ttu-id="5a1f6-120">Spécifiez-1 pour désactiver la gestion parentale.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-120">Specify -1 to disable parental management.</span></span> <span data-ttu-id="5a1f6-121">Pour modifier le niveau parental dans le lecteur, appelez [**SelectParentalLevel**](selectparentallevel-method.md), qui ne modifie pas le paramètre de registre.</span><span class="sxs-lookup"><span data-stu-id="5a1f6-121">To change the parental level in the player, call [**SelectParentalLevel**](selectparentallevel-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a1f6-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a1f6-122">Requirements</span></span>



| <span data-ttu-id="5a1f6-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a1f6-123">Requirement</span></span> | <span data-ttu-id="5a1f6-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a1f6-124">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1f6-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a1f6-125">Header</span></span><br/> | <dl> <span data-ttu-id="5a1f6-126"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a1f6-126"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a1f6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a1f6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a1f6-128">Objet MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="5a1f6-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




