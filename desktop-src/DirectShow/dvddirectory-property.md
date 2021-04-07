---
description: La propriété DVDDirectory définit ou récupère le répertoire actif du volume DVD actuel.
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: Propriété DVDDirectory
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36515c931fb8669db814886dfff12a4bf85bde28
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846345"
---
# <a name="dvddirectory-property"></a><span data-ttu-id="4fad3-103">Propriété DVDDirectory</span><span class="sxs-lookup"><span data-stu-id="4fad3-103">DVDDirectory Property</span></span>

> [!Note]  
> <span data-ttu-id="4fad3-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4fad3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4fad3-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="4fad3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4fad3-106">La `DVDDirectory` propriété définit ou récupère le répertoire actif du volume DVD actuel.</span><span class="sxs-lookup"><span data-stu-id="4fad3-106">The `DVDDirectory` property sets or retrieves the current directory of the current DVD volume.</span></span>

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a><span data-ttu-id="4fad3-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4fad3-107">Return Value</span></span>

<span data-ttu-id="4fad3-108">Retourne une valeur de chaîne indiquant le chemin d’accès au répertoire racine du DVD.</span><span class="sxs-lookup"><span data-stu-id="4fad3-108">Returns a string value indicating the path to the DVD root directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fad3-109">Notes</span><span class="sxs-lookup"><span data-stu-id="4fad3-109">Remarks</span></span>

<span data-ttu-id="4fad3-110">Cette propriété est en lecture/écriture sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="4fad3-110">This property is read/write with no default value.</span></span> <span data-ttu-id="4fad3-111">Utilisez cette méthode pour définir le chemin d’accès racine lorsqu’il y a plus d’un lecteur de DVD sur un système.</span><span class="sxs-lookup"><span data-stu-id="4fad3-111">Use this method to set the root path when there is more than one DVD drive on a system.</span></span> <span data-ttu-id="4fad3-112">Lorsqu’il n’y a qu’un seul lecteur sur le système et que sa lettre de lecteur est supérieure à « C », l’objet MSWebDVD le détecte automatiquement.</span><span class="sxs-lookup"><span data-stu-id="4fad3-112">When there is only one drive on the system and its drive letter is higher than "C", the MSWebDVD object finds it automatically.</span></span> <span data-ttu-id="4fad3-113">Pour un disque DVD-Video standard, le chemin racine doit inclure le \_ répertoire vidéo TS :</span><span class="sxs-lookup"><span data-stu-id="4fad3-113">For a standard DVD-Video disc, the root path should include the ts\_video directory:</span></span>


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



<span data-ttu-id="4fad3-114">Certains volumes de DVD peuvent avoir leur vidéo dans un répertoire nommé autre que « vidéo \_ TS ».</span><span class="sxs-lookup"><span data-stu-id="4fad3-114">Some DVD volumes may have their video in a directory named something other than "video\_ts."</span></span> <span data-ttu-id="4fad3-115">L’idée générale est qu’un « volume DVD » supplémentaire (le jeu de. IFO.</span><span class="sxs-lookup"><span data-stu-id="4fad3-115">The general idea is that an additional "DVD volume" (the set of .IFO.</span></span> <span data-ttu-id="4fad3-116">VOB et. Les fichiers BUP qui seraient normalement stockés dans le répertoire de la vidéo \_ TS) peuvent être placés dans un sous-répertoire du disque. En modifiant la racine pour pointer vers ce répertoire, MSWebDVD fonctionnera sur ce volume de DVD distinct.</span><span class="sxs-lookup"><span data-stu-id="4fad3-116">VOB, and .BUP files that would normally be stored in the VIDEO\_TS directory) can be placed in a subdirectory on the disc. By changing the root to point to this directory, MSWebDVD will operate on this separate DVD volume.</span></span> <span data-ttu-id="4fad3-117">Un nouvel ensemble de menus, titres, etc. sera disponible, indépendamment des titres dans la racine de la vidéo \_ TS, qui n’est plus accessible.</span><span class="sxs-lookup"><span data-stu-id="4fad3-117">A new set of menus, titles, and so on will be available, independent of the titles in the VIDEO\_TS root, which will no longer be accessible.</span></span> <span data-ttu-id="4fad3-118">Ces répertoires sont appelés « répertoires cachés ».</span><span class="sxs-lookup"><span data-stu-id="4fad3-118">Such directories are called "hidden directories."</span></span> <span data-ttu-id="4fad3-119">L’exemple suivant montre comment définir un répertoire masqué comme racine, où « Hidden » est un espace réservé pour le nom que les créateurs de disque ont donné au répertoire.</span><span class="sxs-lookup"><span data-stu-id="4fad3-119">The following example shows how to set a hidden directory as the root, where "hidden" is a placeholder for whatever name the disc authors have given to the directory.</span></span>


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



