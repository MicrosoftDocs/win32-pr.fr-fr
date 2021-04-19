---
description: La propriété AnglesAvailable récupère le nombre d’angles actuellement disponibles.
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: Propriété AnglesAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b9d27806b314d89c68fcc4d1476a9918cd4446
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515539"
---
# <a name="anglesavailable-property"></a><span data-ttu-id="d3968-103">Propriété AnglesAvailable</span><span class="sxs-lookup"><span data-stu-id="d3968-103">AnglesAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="d3968-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d3968-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="d3968-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d3968-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="d3968-106">La `AnglesAvailable` propriété récupère le nombre d’angles actuellement disponibles.</span><span class="sxs-lookup"><span data-stu-id="d3968-106">The `AnglesAvailable` property retrieves the number of angles currently available.</span></span>

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a><span data-ttu-id="d3968-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d3968-107">Return Value</span></span>

<span data-ttu-id="d3968-108">Retourne une valeur entière comprise entre 1 et 9 représentant le nombre d’angles actuellement disponibles.</span><span class="sxs-lookup"><span data-stu-id="d3968-108">Returns an integer value from 1 through 9 representing the number of angles currently available.</span></span> <span data-ttu-id="d3968-109">Si</span><span class="sxs-lookup"><span data-stu-id="d3968-109">If</span></span>


```
iAngles
```



<span data-ttu-id="d3968-110">= 1, il n’y a aucun bloc d’angle à l’emplacement actuel.</span><span class="sxs-lookup"><span data-stu-id="d3968-110">= 1, there is no angle block at the current location.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3968-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d3968-111">Remarks</span></span>

<span data-ttu-id="d3968-112">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d3968-112">This property is read-only with no default value.</span></span> <span data-ttu-id="d3968-113">Un *bloc angulaire* est un segment vidéo qui a été capturé à partir de plusieurs angles d’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="d3968-113">An *angle block* is a video segment that was shot from more than one camera angle.</span></span> <span data-ttu-id="d3968-114">Un bloc angle peut comporter jusqu’à neuf angles, numérotés de 1 à 9.</span><span class="sxs-lookup"><span data-stu-id="d3968-114">There can be up to nine angles in an angle block, numbered from 1 through 9.</span></span> <span data-ttu-id="d3968-115">Lorsque le navigateur DVD entre pour la première fois dans un bloc angle, il envoie à votre application une \_ notification d’événement d’angles de DVD EC \_ \_ disponible avec le nombre d’angles dans *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="d3968-115">When the DVD Navigator first enters an angle block, it sends your application an EC\_DVD\_ANGLES\_AVAILABLE event notification with the number of angles in *lParam1*.</span></span> <span data-ttu-id="d3968-116">Un disque peut être créé pour afficher automatiquement un menu pour les angles disponibles lorsqu’il entre dans un bloc angle, mais, en général, une application doit déterminer le nombre d’angles disponibles et offrir à l’utilisateur un moyen d’en sélectionner un.</span><span class="sxs-lookup"><span data-stu-id="d3968-116">A disc can be authored to automatically show a menu for available angles when it enters an angle block, but generally an application must determine the number of angles available and offer the user a way to select one.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3968-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3968-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3968-118">**CurrentAngle**</span><span class="sxs-lookup"><span data-stu-id="d3968-118">**CurrentAngle**</span></span>](currentangle-property.md)
</dt> </dl>

 

 



