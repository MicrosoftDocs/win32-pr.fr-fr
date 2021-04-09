---
description: La propriété DVDUniqueID récupère un numéro généré par le système qui identifie de façon unique le disque actuel.
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: Propriété DVDUniqueID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23138f348ef1ec71f1506c8892532bd42f1c807d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846341"
---
# <a name="dvduniqueid-property"></a><span data-ttu-id="03f33-103">Propriété DVDUniqueID</span><span class="sxs-lookup"><span data-stu-id="03f33-103">DVDUniqueID Property</span></span>

> [!Note]  
> <span data-ttu-id="03f33-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="03f33-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="03f33-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="03f33-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="03f33-106">La `DVDUniqueID` propriété récupère un numéro généré par le système qui identifie de façon unique le disque actuel.</span><span class="sxs-lookup"><span data-stu-id="03f33-106">The `DVDUniqueID` property retrieves a system-generated number that uniquely identifies the current disc.</span></span>

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a><span data-ttu-id="03f33-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="03f33-107">Return Value</span></span>

<span data-ttu-id="03f33-108">Retourne une valeur entière qui identifie de façon unique le disque actuel.</span><span class="sxs-lookup"><span data-stu-id="03f33-108">Returns an integer value that uniquely identifies the current disc.</span></span>

## <a name="remarks"></a><span data-ttu-id="03f33-109">Notes</span><span class="sxs-lookup"><span data-stu-id="03f33-109">Remarks</span></span>

<span data-ttu-id="03f33-110">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="03f33-110">This property is read-only with no default value.</span></span> <span data-ttu-id="03f33-111">Le numéro d’identificateur (ID) n’est pas absolument unique, mais il est unique dans tous les cas pratiques.</span><span class="sxs-lookup"><span data-stu-id="03f33-111">The identifier (ID) number is not absolutely unique, but it is unique for all practical purposes.</span></span> <span data-ttu-id="03f33-112">L’ID s’applique à toutes les copies répliquées d’un disque. En d’autres termes, toutes les copies d’un film spécifique ont le même ID.</span><span class="sxs-lookup"><span data-stu-id="03f33-112">The ID applies to all replicated copies of a disc. In other words, all copies of a specific movie have the same ID.</span></span> <span data-ttu-id="03f33-113">L’ID est basé sur les tailles de fichier, les dates et d’autres informations, et non sur la valeur BCA.</span><span class="sxs-lookup"><span data-stu-id="03f33-113">The ID is based on file sizes, dates, and other information, and not the BCA value.</span></span>

 

 



