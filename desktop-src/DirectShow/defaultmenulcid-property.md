---
description: La propriété DVDAdm. DefaultMenuLCID définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour les menus.
ms.assetid: 49e64b89-5914-4797-8aa6-2e3f253e494a
title: Propriété DefaultMenuLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907fbef0d04306b5ddc4f9a59749c96573d05bb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109618"
---
# <a name="defaultmenulcid-property"></a><span data-ttu-id="9a1be-103">Propriété DefaultMenuLCID</span><span class="sxs-lookup"><span data-stu-id="9a1be-103">DefaultMenuLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="9a1be-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9a1be-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9a1be-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9a1be-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9a1be-106">La `DVDAdm.DefaultMenuLCID` propriété définit ou récupère le paramètre de Registre pour le LCID par défaut spécifié par l’utilisateur pour les menus.</span><span class="sxs-lookup"><span data-stu-id="9a1be-106">The `DVDAdm.DefaultMenuLCID` property sets or retrieves the registry setting for the user-specified default LCID for menus.</span></span>

``` syntax
[ iMenuLCID = ] DVD.DVDAdm.DefaultMenuLCID
```

## <a name="return-value"></a><span data-ttu-id="9a1be-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9a1be-107">Return Value</span></span>

<span data-ttu-id="9a1be-108">Retourne une valeur entière représentant le LCID tel qu’il est stocké dans les paramètres du Registre pour l’application DVD.</span><span class="sxs-lookup"><span data-stu-id="9a1be-108">Returns an Integer value representing the LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="9a1be-109">Cette valeur n’est pas nécessairement la même que la langue de menu par défaut créée sur le DVD.</span><span class="sxs-lookup"><span data-stu-id="9a1be-109">This value is not necessarily the same as the default menu language as authored on the DVD.</span></span> <span data-ttu-id="9a1be-110">Pour connaître la plage de LCID valides, consultez la documentation Win32 dans le kit de développement logiciel (SDK) de plateforme.</span><span class="sxs-lookup"><span data-stu-id="9a1be-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a1be-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9a1be-111">Remarks</span></span>

<span data-ttu-id="9a1be-112">Cette propriété est en lecture/écriture sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9a1be-112">This property is read/write with no default value.</span></span> <span data-ttu-id="9a1be-113">Si aucun LCID de menu par défaut n’est spécifié, l’objet MSDVDAdm utilise la langue qui est marquée en tant que langue de menu par défaut sur le disque.</span><span class="sxs-lookup"><span data-stu-id="9a1be-113">If no default menu LCID is specified, the MSDVDAdm object will use the language that is marked as the default menu language on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a1be-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a1be-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a1be-115">Objet MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="9a1be-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



