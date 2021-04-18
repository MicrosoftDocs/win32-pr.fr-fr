---
description: La propriété CurrentAudioStream définit ou récupère le numéro du flux audio activé.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Propriété CurrentAudioStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512865"
---
# <a name="currentaudiostream-property"></a><span data-ttu-id="78e04-103">Propriété CurrentAudioStream</span><span class="sxs-lookup"><span data-stu-id="78e04-103">CurrentAudioStream Property</span></span>

> [!Note]  
> <span data-ttu-id="78e04-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="78e04-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="78e04-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="78e04-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="78e04-106">La `CurrentAudioStream` propriété définit ou récupère le numéro du flux audio activé.</span><span class="sxs-lookup"><span data-stu-id="78e04-106">The `CurrentAudioStream` property sets or retrieves the number of the enabled audio stream.</span></span>

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a><span data-ttu-id="78e04-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="78e04-107">Return Value</span></span>

<span data-ttu-id="78e04-108">Retourne une valeur entière comprise entre 0 et 7 indiquant le flux audio actuel.</span><span class="sxs-lookup"><span data-stu-id="78e04-108">Returns an integer value from 0 through 7 indicating the current audio stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="78e04-109">Notes</span><span class="sxs-lookup"><span data-stu-id="78e04-109">Remarks</span></span>

<span data-ttu-id="78e04-110">Cette propriété est en lecture/écriture sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="78e04-110">This property is read/write with no default value.</span></span> <span data-ttu-id="78e04-111">Avant de tenter de définir un nouveau flux audio, appelez [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) pour vérifier que le flux est disponible.</span><span class="sxs-lookup"><span data-stu-id="78e04-111">Before attempting to set a new audio stream, call [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) to verify that the stream is available.</span></span>

## <a name="see-also"></a><span data-ttu-id="78e04-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78e04-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78e04-113">**AudioStreamsAvailable**</span><span class="sxs-lookup"><span data-stu-id="78e04-113">**AudioStreamsAvailable**</span></span>](audiostreamsavailable-property.md)
</dt> </dl>

 

 



