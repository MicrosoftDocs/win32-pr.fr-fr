---
description: La méthode GetDVDTextNumberOfStrings récupère le nombre de chaînes de texte disponibles pour la langue spécifiée.
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: Méthode GetDVDTextNumberOfStrings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c9c4fadfd28d6cddc8b9013a6e426aebe9f816
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513107"
---
# <a name="getdvdtextnumberofstrings-method"></a><span data-ttu-id="57065-103">Méthode GetDVDTextNumberOfStrings</span><span class="sxs-lookup"><span data-stu-id="57065-103">GetDVDTextNumberOfStrings Method</span></span>

> [!Note]  
> <span data-ttu-id="57065-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="57065-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="57065-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="57065-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="57065-106">La `GetDVDTextNumberOfStrings` méthode récupère le nombre de chaînes de texte disponibles pour la langue spécifiée.</span><span class="sxs-lookup"><span data-stu-id="57065-106">The `GetDVDTextNumberOfStrings` method retrieves the number of text strings available for the specified language.</span></span>

``` syntax
[ iStrings = ] MSWebDVD.GetDVDTextNumberOfStrings(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="57065-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57065-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57065-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span><span class="sxs-lookup"><span data-stu-id="57065-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="57065-109">Spécifie la langue sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="57065-109">Specifies the language as an Integer.</span></span> <span data-ttu-id="57065-110">La valeur doit être comprise entre zéro et une valeur inférieure à la valeur retournée par [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span><span class="sxs-lookup"><span data-stu-id="57065-110">The value must range from zero through one less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57065-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="57065-111">Return Value</span></span>

<span data-ttu-id="57065-112">Retourne une valeur entière spécifiant le nombre de chaînes contenues dans le disque dans la langue spécifiée.</span><span class="sxs-lookup"><span data-stu-id="57065-112">Returns an integer value specifying how many strings the disc contains in the specified language.</span></span>

## <a name="see-also"></a><span data-ttu-id="57065-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57065-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57065-114">Objet MSWebDVD</span><span class="sxs-lookup"><span data-stu-id="57065-114">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> </dl>

 

 



