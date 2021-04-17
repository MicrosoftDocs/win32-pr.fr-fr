---
description: La méthode GetDVDTextLanguageLCID récupère l’identificateur de paramètres régionaux (LCID) pour le bloc de chaîne de texte spécifié.
ms.assetid: feaa1db8-2d33-4c32-8491-f3aa5555e3d3
title: Méthode GetDVDTextLanguageLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66d21b9870982b605d9deeb1e22882a525c5616
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520631"
---
# <a name="getdvdtextlanguagelcid-method"></a><span data-ttu-id="0509f-103">Méthode GetDVDTextLanguageLCID</span><span class="sxs-lookup"><span data-stu-id="0509f-103">GetDVDTextLanguageLCID Method</span></span>

> [!Note]  
> <span data-ttu-id="0509f-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0509f-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0509f-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0509f-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0509f-106">La `GetDVDTextLanguageLCID` méthode récupère l’identificateur de paramètres régionaux (LCID) pour le bloc de chaîne de texte spécifié.</span><span class="sxs-lookup"><span data-stu-id="0509f-106">The `GetDVDTextLanguageLCID` method retrieves the locale identifier (LCID) for the specified text string block.</span></span>

``` syntax
[ iLCID = ] MSWebDVD.GetDVDTextLanguageLCID(iLangIndex)
```

## <a name="parameters"></a><span data-ttu-id="0509f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0509f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0509f-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span><span class="sxs-lookup"><span data-stu-id="0509f-108"><span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*</span></span>
</dt> <dd>

<span data-ttu-id="0509f-109">Spécifie le bloc de langage de texte sur le disque sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="0509f-109">Specifies the text language block on the disc as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0509f-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0509f-110">Return Value</span></span>

<span data-ttu-id="0509f-111">Retourne une valeur LCID qui contient des informations spécifiant le langage dans lequel les chaînes sont écrites.</span><span class="sxs-lookup"><span data-stu-id="0509f-111">Returns an LCID value that contains information specifying the language the strings are written in.</span></span>

## <a name="remarks"></a><span data-ttu-id="0509f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0509f-112">Remarks</span></span>

<span data-ttu-id="0509f-113">Les chaînes de texte supplémentaires sont stockées dans des blocs contigus sur le disque. Chaque langage possède un bloc de chaînes.</span><span class="sxs-lookup"><span data-stu-id="0509f-113">Supplemental text strings are stored in contiguous blocks on the disc. Each language has one block of strings.</span></span> <span data-ttu-id="0509f-114">Une application spécifie ces blocs par un index, qui doit être inférieur à la valeur retournée par [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span><span class="sxs-lookup"><span data-stu-id="0509f-114">An application specifies these blocks by an index, which must be less than the value returned by [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0509f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0509f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0509f-116">Objet MSWebDVD</span><span class="sxs-lookup"><span data-stu-id="0509f-116">MSWebDVD Object</span></span>](mswebdvd-object.md)
</dt> <dt>

[<span data-ttu-id="0509f-117">**GetLangFromLangID**</span><span class="sxs-lookup"><span data-stu-id="0509f-117">**GetLangFromLangID**</span></span>](getlangfromlangid-method.md)
</dt> </dl>

 

 



