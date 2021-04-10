---
description: La propriété PreferredSubpictureStream récupère le flux de sous-image préféré pour la session d’affichage en cours.
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: Propriété PreferredSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23377d74d3632c665b001ae415dc151ca73bd148
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846289"
---
# <a name="preferredsubpicturestream-property"></a><span data-ttu-id="ff3d6-103">Propriété PreferredSubpictureStream</span><span class="sxs-lookup"><span data-stu-id="ff3d6-103">PreferredSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="ff3d6-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ff3d6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ff3d6-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ff3d6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ff3d6-106">La `PreferredSubpictureStream` propriété récupère le flux de sous-image préféré pour la session d’affichage en cours.</span><span class="sxs-lookup"><span data-stu-id="ff3d6-106">The `PreferredSubpictureStream` property retrieves the preferred subpicture stream for the current viewing session.</span></span>

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="ff3d6-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ff3d6-107">Return Value</span></span>

<span data-ttu-id="ff3d6-108">Retourne une valeur entière représentant le flux de sous-image préféré actuel dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="ff3d6-108">Returns an Integer value representing the current preferred subpicture stream in the system registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff3d6-109">Notes</span><span class="sxs-lookup"><span data-stu-id="ff3d6-109">Remarks</span></span>

<span data-ttu-id="ff3d6-110">Le flux de sous-image par défaut est défini avec [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md)de l’objet [MSDVDAdm](msdvdadm-object.md) .</span><span class="sxs-lookup"><span data-stu-id="ff3d6-110">The preferred subpicture stream is set with [MSDVDAdm](msdvdadm-object.md) object's [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md).</span></span>

 

 



