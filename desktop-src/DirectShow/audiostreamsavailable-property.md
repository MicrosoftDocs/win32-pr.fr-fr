---
description: La propriété AudioStreamsAvailable récupère le nombre de flux audio disponibles dans le titre actuel.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Propriété AudioStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb68020b30f4349fcbbb464150624d75250a0dbf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846181"
---
# <a name="audiostreamsavailable-property"></a><span data-ttu-id="8ac05-103">Propriété AudioStreamsAvailable</span><span class="sxs-lookup"><span data-stu-id="8ac05-103">AudioStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="8ac05-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8ac05-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8ac05-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8ac05-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8ac05-106">La `AudioStreamsAvailable` propriété récupère le nombre de flux audio disponibles dans le titre actuel.</span><span class="sxs-lookup"><span data-stu-id="8ac05-106">The `AudioStreamsAvailable` property retrieves the number of audio streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="8ac05-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8ac05-107">Return Value</span></span>

<span data-ttu-id="8ac05-108">Retourne une valeur entière comprise entre 1 et 8 représentant le nombre de flux audio disponibles dans le titre actuel.</span><span class="sxs-lookup"><span data-stu-id="8ac05-108">Returns an integer value from 1 through 8 representing the number of audio streams available in the current title.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ac05-109">Notes</span><span class="sxs-lookup"><span data-stu-id="8ac05-109">Remarks</span></span>

<span data-ttu-id="8ac05-110">Cette propriété est en lecture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="8ac05-110">This property is read-only with no default value.</span></span> <span data-ttu-id="8ac05-111">L’utilisation principale de plusieurs flux audio consiste à fournir des pistes vidéo dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="8ac05-111">The primary use of multiple audio streams is to provide movie soundtracks in more than one language.</span></span> <span data-ttu-id="8ac05-112">En règle générale, tous les flux audio ne sont pas activés sur un disque.</span><span class="sxs-lookup"><span data-stu-id="8ac05-112">Typically, not every title on a disc has all audio streams enabled.</span></span> <span data-ttu-id="8ac05-113">Par exemple, le film de fonctionnalité peut comporter des pistes audio dans trois langues différentes, mais les codes de fin ne peuvent avoir qu’une seule bande anglaise.</span><span class="sxs-lookup"><span data-stu-id="8ac05-113">For example, the feature movie might have soundtracks in three different languages, but the trailers might have only an English soundtrack.</span></span> <span data-ttu-id="8ac05-114">Pour qu’un utilisateur puisse sélectionner un flux, l’application doit déterminer les flux disponibles dans le titre en cours.</span><span class="sxs-lookup"><span data-stu-id="8ac05-114">Before a user can select a stream, the application must determine which streams are available within the current title.</span></span> <span data-ttu-id="8ac05-115">Notez que des flux particuliers sont identifiés par un index de 0 à 7.</span><span class="sxs-lookup"><span data-stu-id="8ac05-115">Note that particular streams are identified by an index from zero through 7.</span></span>

<span data-ttu-id="8ac05-116">Les disques présentent généralement un menu présentant les bandes-son disponibles, ce qui permet à l’utilisateur de sélectionner le flux audio à activer.</span><span class="sxs-lookup"><span data-stu-id="8ac05-116">Discs generally present a menu showing the available soundtracks, enabling the user to select the audio stream to enable.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ac05-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ac05-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ac05-118">**GetAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="8ac05-118">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> </dl>

 

 



