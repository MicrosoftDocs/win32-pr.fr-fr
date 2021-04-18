---
description: La méthode StillOff reprend la lecture, en annulant le mode toujours.
ms.assetid: 62091aad-8a78-4543-a844-a4227aed81df
title: Méthode StillOff
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8986b62585768b83fc5737012a924e6cf33daf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520015"
---
# <a name="stilloff-method"></a><span data-ttu-id="2f537-103">Méthode StillOff</span><span class="sxs-lookup"><span data-stu-id="2f537-103">StillOff Method</span></span>

> [!Note]  
> <span data-ttu-id="2f537-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2f537-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2f537-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2f537-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2f537-106">La `StillOff` méthode reprend la lecture, en annulant le mode toujours.</span><span class="sxs-lookup"><span data-stu-id="2f537-106">The `StillOff` method resumes playback, canceling still mode.</span></span>

``` syntax
MSWebDVD.StillOff()
```

## <a name="return-value"></a><span data-ttu-id="2f537-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2f537-107">Return Value</span></span>

<span data-ttu-id="2f537-108">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="2f537-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f537-109">Notes</span><span class="sxs-lookup"><span data-stu-id="2f537-109">Remarks</span></span>

<span data-ttu-id="2f537-110">Le [navigateur DVD](dvd-navigator-filter.md) passe en mode toujours lorsqu’il rencontre une image toujours créée sur le disque. Il indique à votre application d’envoyer un \_ DVD ce \_ toujours \_ sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="2f537-110">The [DVD Navigator](dvd-navigator-filter.md) goes into still mode when it encounters a still frame authored on the disc. It notifies your application by sending an EC\_DVD\_STILL\_ON event.</span></span> <span data-ttu-id="2f537-111">Le mode toujours est différent du navigateur DVD qui se trouve dans un état suspendu en raison d’une opération utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2f537-111">Still mode is different from the DVD Navigator being in a paused state because of a user operation.</span></span> <span data-ttu-id="2f537-112">`StillOff`L’appel de reprend la lecture en mode toujours, mais ne redémarre pas le navigateur DVD lorsqu’il est dans un état suspendu.</span><span class="sxs-lookup"><span data-stu-id="2f537-112">Calling `StillOff` resumes playback from still mode but does not restart the DVD Navigator when it is in a paused state.</span></span>

 

 



