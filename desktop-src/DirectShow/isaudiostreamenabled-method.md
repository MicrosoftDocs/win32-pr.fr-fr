---
description: La méthode IsAudioStreamEnabled récupère une valeur indiquant si le flux audio spécifié est activé dans le titre actuel.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Méthode IsAudioStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92df59479e5729c392eb25b6c6c075a52b4835b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520396"
---
# <a name="isaudiostreamenabled-method"></a><span data-ttu-id="b32c9-103">Méthode IsAudioStreamEnabled</span><span class="sxs-lookup"><span data-stu-id="b32c9-103">IsAudioStreamEnabled Method</span></span>

> [!Note]  
> <span data-ttu-id="b32c9-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b32c9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b32c9-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="b32c9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b32c9-106">La `IsAudioStreamEnabled` méthode récupère une valeur indiquant si le flux audio spécifié est activé dans le titre actuel.</span><span class="sxs-lookup"><span data-stu-id="b32c9-106">The `IsAudioStreamEnabled` method retrieves a value indicating whether the specified audio stream is enabled in the current title.</span></span>

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a><span data-ttu-id="b32c9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b32c9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b32c9-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="b32c9-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="b32c9-109">Spécifie le flux audio sous la forme d’une valeur entière comprise entre 0 et 7.</span><span class="sxs-lookup"><span data-stu-id="b32c9-109">Specifies the audio stream as an Integer value from 0 through 7.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b32c9-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b32c9-110">Return Value</span></span>

<span data-ttu-id="b32c9-111">Retourne une valeur booléenne indiquant si le flux audio spécifié est disponible pour le titre actuel.</span><span class="sxs-lookup"><span data-stu-id="b32c9-111">Returns a Boolean value indicating whether the specified audio stream is available for the current title.</span></span> <span data-ttu-id="b32c9-112">True signifie qu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="b32c9-112">True means it is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="b32c9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b32c9-113">Remarks</span></span>

<span data-ttu-id="b32c9-114">Bien qu’un disque puisse contenir jusqu’à huit flux audio indépendants, chaque flux n’est pas nécessairement disponible pour chaque titre.</span><span class="sxs-lookup"><span data-stu-id="b32c9-114">Although a disc can contain up to eight independent audio streams, each stream is not necessarily available for each title.</span></span> <span data-ttu-id="b32c9-115">Par exemple, un titre de film principal peut avoir trois flux audio pour l’anglais, l’espagnol et le japonais, mais le titre « prochains attractions » peut avoir un seul flux audio en anglais.</span><span class="sxs-lookup"><span data-stu-id="b32c9-115">For example, a main movie title might have three audio streams for English, Spanish, and Japanese, but the "Coming Attractions" title might have only one audio stream in English.</span></span> <span data-ttu-id="b32c9-116">Vérifiez toujours qu’un flux est disponible pour un titre avant de définir la propriété [**CurrentAudioStream**](currentaudiostream-property.md) .</span><span class="sxs-lookup"><span data-stu-id="b32c9-116">Always verify that a stream is available for a title before setting the [**CurrentAudioStream**](currentaudiostream-property.md) property.</span></span>

 

 



