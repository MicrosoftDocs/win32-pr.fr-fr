---
description: La propriété DVDAdm. DefaultSubpictureLCID définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux de sous-image.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Propriété DefaultSubpictureLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f52227dc220bef474e872cbd695c78dc65f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522783"
---
# <a name="defaultsubpicturelcid-property"></a><span data-ttu-id="cb0df-103">Propriété DefaultSubpictureLCID</span><span class="sxs-lookup"><span data-stu-id="cb0df-103">DefaultSubpictureLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="cb0df-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cb0df-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="cb0df-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="cb0df-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="cb0df-106">La `DVDAdm.DefaultSubpictureLCID` propriété définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour le flux de sous-image.</span><span class="sxs-lookup"><span data-stu-id="cb0df-106">The `DVDAdm.DefaultSubpictureLCID` property sets or retrieves the registry setting for the user-specified default LCID for the subpicture stream.</span></span>

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a><span data-ttu-id="cb0df-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cb0df-107">Return Value</span></span>

<span data-ttu-id="cb0df-108">Retourne une valeur entière représentant le LCID de sous-image par défaut spécifié par l’utilisateur, tel qu’il est stocké dans les paramètres du Registre pour l’application DVD.</span><span class="sxs-lookup"><span data-stu-id="cb0df-108">Returns an Integer value representing the user-specified default subpicture LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="cb0df-109">Cette valeur n’est pas nécessairement identique au flux de sous-image par défaut tel qu’il a été créé sur le DVD.</span><span class="sxs-lookup"><span data-stu-id="cb0df-109">This value is not necessarily the same as the default subpicture stream as authored on the DVD.</span></span> <span data-ttu-id="cb0df-110">Pour connaître la plage de LCID valides, consultez la documentation Win32 dans le kit de développement logiciel (SDK) de plateforme.</span><span class="sxs-lookup"><span data-stu-id="cb0df-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb0df-111">Notes</span><span class="sxs-lookup"><span data-stu-id="cb0df-111">Remarks</span></span>

<span data-ttu-id="cb0df-112">Cette propriété est en lecture/écriture sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="cb0df-112">This property is read/write with no default value.</span></span> <span data-ttu-id="cb0df-113">Si aucun LCID de sous-image par défaut n’est spécifié, l’objet MSDVDAdm lira le flux de sous-image qui est marqué comme flux par défaut sur le disque.</span><span class="sxs-lookup"><span data-stu-id="cb0df-113">If no default subpicture LCID is specified, the MSDVDAdm object will play the subpicture stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb0df-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb0df-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb0df-115">Objet MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="cb0df-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



