---
description: Le GetPlayerParentalLevel récupère le niveau de gestion parental défini dans l’objet MSWebDVD.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Méthode GetPlayerParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bac51e776a45e0d1fa748fc995240292474e902
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108499"
---
# <a name="getplayerparentallevel-method"></a><span data-ttu-id="a76fe-103">Méthode GetPlayerParentalLevel</span><span class="sxs-lookup"><span data-stu-id="a76fe-103">GetPlayerParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="a76fe-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a76fe-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a76fe-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a76fe-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a76fe-106">Le `GetPlayerParentalLevel` récupère le niveau de gestion parental défini dans l’objet **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="a76fe-106">The `GetPlayerParentalLevel` retrieves the parental management level set in the **MSWebDVD** object.</span></span>

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="a76fe-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a76fe-107">Return Value</span></span>

<span data-ttu-id="a76fe-108">Retourne une valeur entière spécifiant le niveau parental actuel dans le navigateur DVD, ou-1 si la gestion parentale est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a76fe-108">Returns an integer value specifying the current parental level in the DVD Navigator, or -1 if parental management is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="a76fe-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a76fe-109">Remarks</span></span>

<span data-ttu-id="a76fe-110">Une application de lecteur est chargée d’appliquer les contrôles de contrôle parental.</span><span class="sxs-lookup"><span data-stu-id="a76fe-110">A player application is responsible for enforcing parental controls.</span></span> <span data-ttu-id="a76fe-111">Le niveau parental du joueur est une valeur définie par une application qui peut être utilisée pour indiquer le niveau parental le plus élevé que l’utilisateur actuel peut afficher.</span><span class="sxs-lookup"><span data-stu-id="a76fe-111">The player parental level is a value set by an application than can be used to indicate the highest parental level the current user can view.</span></span> <span data-ttu-id="a76fe-112">Lorsque le navigateur DVD rencontre un nouveau niveau parental, utilisez cette méthode pour déterminer si le nouveau niveau est supérieur au niveau défini par l’application via [**SelectParentalLevel**](selectparentallevel-method.md).</span><span class="sxs-lookup"><span data-stu-id="a76fe-112">When the DVD Navigator encounters a new parental level, use this method to determine whether the new level is greater than the level that was set by the application through [**SelectParentalLevel**](selectparentallevel-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a76fe-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a76fe-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a76fe-114">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="a76fe-114">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="a76fe-115">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="a76fe-115">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="a76fe-116">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="a76fe-116">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="a76fe-117">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="a76fe-117">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



