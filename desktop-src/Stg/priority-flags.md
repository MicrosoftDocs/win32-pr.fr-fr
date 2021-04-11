---
title: Indicateurs de priorité
description: L’indicateur Priority ouvre un objet de stockage en mode de priorité.
ms.assetid: 85f2df6f-9219-4752-8c17-f219c37a4037
keywords:
- Indicateurs de priorité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f4af04174ddb6c0ac459a6f7e6841e061b03c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029893"
---
# <a name="priority-flags"></a><span data-ttu-id="dfcee-104">Indicateurs de priorité</span><span class="sxs-lookup"><span data-stu-id="dfcee-104">Priority Flags</span></span>

<span data-ttu-id="dfcee-105">L’indicateur Priority ouvre un objet de stockage en mode de priorité.</span><span class="sxs-lookup"><span data-stu-id="dfcee-105">The priority flag opens a storage object in priority mode.</span></span> <span data-ttu-id="dfcee-106">Lorsqu’il ouvre un objet, une application fonctionne généralement à partir d’une copie d’instantané, car d’autres applications peuvent également utiliser l’objet en même temps.</span><span class="sxs-lookup"><span data-stu-id="dfcee-106">When it opens an object, an application usually works from a snapshot copy because other applications may also be using the object at the same time.</span></span> <span data-ttu-id="dfcee-107">Toutefois, lors de l’ouverture d’un objet de stockage en mode de priorité, l’application dispose des droits exclusifs pour valider les modifications apportées à l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfcee-107">When opening a storage object in priority mode, however, the application has exclusive rights to commit changes to the object.</span></span>

<span data-ttu-id="dfcee-108">Le mode priorité permet à une application de lire des flux à partir du stockage avant d’ouvrir l’objet dans un mode qui nécessiterait le système pour effectuer une copie d’instantané.</span><span class="sxs-lookup"><span data-stu-id="dfcee-108">Priority mode enables an application to read some streams from storage before opening the object in a mode that would require the system to make a snapshot copy.</span></span> <span data-ttu-id="dfcee-109">Étant donné que l’application dispose d’un accès exclusif, elle n’a pas besoin de créer une copie d’instantané de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfcee-109">Because the application has exclusive access, it does not have to make a snapshot copy of the object.</span></span> <span data-ttu-id="dfcee-110">Lorsque l’application ouvre par la suite l’objet dans un mode dans lequel une copie d’instantané est requise, l’application peut exclure les flux qu’elle a déjà lus à partir de l’instantané, ce qui réduit la surcharge liée à l’ouverture de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dfcee-110">When the application subsequently opens the object in a mode where a snapshot copy is required, the application can exclude the streams it has already read from the snapshot, thereby reducing the overhead of opening the object.</span></span>

<span data-ttu-id="dfcee-111">Étant donné que les autres applications ne peuvent pas valider les modifications apportées à un objet pendant qu’il est ouvert en mode de priorité, les applications doivent garder l’objet dans ce mode aussi peu de temps que possible.</span><span class="sxs-lookup"><span data-stu-id="dfcee-111">Because other applications cannot commit changes to an object while it is open in priority mode, applications should keep the object in that mode for as short a time as possible.</span></span>

 

 




