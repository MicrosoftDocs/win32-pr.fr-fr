---
description: La méthode DVDAdm. GetParentalLevel récupère le niveau parental qui a été enregistré pour la dernière fois dans le registre.
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: Méthode GetParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfa2c2193a9d02249076b2be2225fc50cd1edd5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385564"
---
# <a name="getparentallevel-method"></a><span data-ttu-id="59ca5-103">Méthode GetParentalLevel</span><span class="sxs-lookup"><span data-stu-id="59ca5-103">GetParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="59ca5-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="59ca5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="59ca5-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="59ca5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="59ca5-106">La `DVDAdm.GetParentalLevel` méthode récupère le niveau parental précédemment enregistré dans le registre.</span><span class="sxs-lookup"><span data-stu-id="59ca5-106">The `DVDAdm.GetParentalLevel` method retrieves the parental level that was last saved to the registry.</span></span>

``` syntax
[ iParentalLevel = ] DVD.DVDAdm.GetParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="59ca5-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="59ca5-107">Return Value</span></span>

<span data-ttu-id="59ca5-108">Retourne un entier compris entre 1 et 8 indiquant le niveau parental par défaut.</span><span class="sxs-lookup"><span data-stu-id="59ca5-108">Returns an Integer from 1 through 8 indicating the default parental level.</span></span>

## <a name="remarks"></a><span data-ttu-id="59ca5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="59ca5-109">Remarks</span></span>

<span data-ttu-id="59ca5-110">Le niveau parental récupéré par cette méthode n’est pas nécessairement le même que celui qui est actuellement stocké dans le contrôle MSWebDVD. pour récupérer le niveau actuellement stocké dans le contrôle, appelez la méthode [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) .</span><span class="sxs-lookup"><span data-stu-id="59ca5-110">The parental level this method retrieves is not necessarily the same level currently stored in the MSWebDVD control; to get the level currently stored in the control, call the [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) method.</span></span> <span data-ttu-id="59ca5-111">La valeur-1 indique que la gestion parentale est désactivée.</span><span class="sxs-lookup"><span data-stu-id="59ca5-111">A value of -1 indicates that parental management is disabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="59ca5-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59ca5-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ca5-113">Objet MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="59ca5-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



