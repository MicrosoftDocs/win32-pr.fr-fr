---
description: La méthode DVDTimeCode2bstr récupère une chaîne indiquant l’heure actuelle sur le disque.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: Méthode DVDTimeCode2bstr
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513097"
---
# <a name="dvdtimecode2bstr-method"></a><span data-ttu-id="276cf-103">Méthode DVDTimeCode2bstr</span><span class="sxs-lookup"><span data-stu-id="276cf-103">DVDTimeCode2bstr Method</span></span>

> [!Note]  
> <span data-ttu-id="276cf-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="276cf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="276cf-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="276cf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="276cf-106">La `DVDTimeCode2bstr` méthode récupère une chaîne indiquant l’heure actuelle sur le disque.</span><span class="sxs-lookup"><span data-stu-id="276cf-106">The `DVDTimeCode2bstr` method retrieves a string indicating the current time on the disc.</span></span>

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a><span data-ttu-id="276cf-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="276cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="276cf-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*</span><span class="sxs-lookup"><span data-stu-id="276cf-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="276cf-109">Spécifie l’heure actuelle sur le disque par rapport au début du titre sous la forme d’un nombre obtenu par le biais de l’événement [**\_ HMSF de \_ \_ \_ temps actuel du DVD**](ec-dvd-current-hmsf-time.md) .</span><span class="sxs-lookup"><span data-stu-id="276cf-109">Specifies the current time on the disc relative to the start of the title as a Number obtained through the [**EC\_DVD\_CURRENT\_HMSF\_TIME**](ec-dvd-current-hmsf-time.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="276cf-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="276cf-110">Return Value</span></span>

<span data-ttu-id="276cf-111">Retourne une chaîne de 11 caractères au format "HH : mm : SS : FF" représentant les heures, les minutes, les secondes et les frames qui définissent l’heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="276cf-111">Returns an 11-character String in the format "hh:mm:ss:ff" representing the hours, minutes, seconds and frames that define the current time.</span></span>

## <a name="remarks"></a><span data-ttu-id="276cf-112">Notes</span><span class="sxs-lookup"><span data-stu-id="276cf-112">Remarks</span></span>

<span data-ttu-id="276cf-113">Cette méthode est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="276cf-113">This method is read only.</span></span>

## <a name="see-also"></a><span data-ttu-id="276cf-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="276cf-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="276cf-115">Gestion des notifications d’événements DVD</span><span class="sxs-lookup"><span data-stu-id="276cf-115">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



