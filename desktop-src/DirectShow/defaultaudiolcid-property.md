---
description: La propriété DVDAdm. DefaultAudioLCID définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux audio.
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: Propriété DefaultAudioLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe302adaa555d59b2c1dcd50d749e9afdc2de740
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515752"
---
# <a name="defaultaudiolcid-property"></a><span data-ttu-id="2792e-103">Propriété DefaultAudioLCID</span><span class="sxs-lookup"><span data-stu-id="2792e-103">DefaultAudioLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="2792e-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2792e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2792e-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="2792e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2792e-106">La `DVDAdm.DefaultAudioLCID` propriété définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="2792e-106">The `DVDAdm.DefaultAudioLCID` property sets or retrieves the registry setting for the user-specified default LCID for the audio stream.</span></span>

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a><span data-ttu-id="2792e-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2792e-107">Return Value</span></span>

<span data-ttu-id="2792e-108">Retourne une valeur entière représentant le LCID audio par défaut spécifié par l’utilisateur, tel qu’il est stocké dans les paramètres du Registre pour l’application DVD.</span><span class="sxs-lookup"><span data-stu-id="2792e-108">Returns an Integer value representing the user-specified default audio LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="2792e-109">Cette valeur n’est pas nécessairement identique à celle du flux audio par défaut tel qu’il a été créé sur le DVD.</span><span class="sxs-lookup"><span data-stu-id="2792e-109">This value is not necessarily the same as the default audio stream as authored on the DVD.</span></span>

## <a name="remarks"></a><span data-ttu-id="2792e-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2792e-110">Remarks</span></span>

<span data-ttu-id="2792e-111">Cette propriété est en lecture/écriture sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="2792e-111">This property is read/write with no default value.</span></span> <span data-ttu-id="2792e-112">Si aucun LCID audio par défaut n’est spécifié, l’objet MSDVDAdm lira le flux audio qui est marqué comme flux par défaut sur le disque.</span><span class="sxs-lookup"><span data-stu-id="2792e-112">If no default audio LCID is specified, the MSDVDAdm object will play the audio stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="2792e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2792e-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2792e-114">Objet MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="2792e-114">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



