---
description: Vous pouvez mettre à jour les valeurs des propriétés non-clés des instances de classe de vue Union. Les modifications que vous apportez à l’instance de la classe de vue seront propagées vers les instances de la classe source qui forment la classe d’affichage Union.
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: Mise à jour d’une vue Union
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b051147ab40aacbf9032c5a0998d5894148985c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114843"
---
# <a name="updating-a-union-view"></a><span data-ttu-id="9c77d-104">Mise à jour d’une vue Union</span><span class="sxs-lookup"><span data-stu-id="9c77d-104">Updating a Union View</span></span>

<span data-ttu-id="9c77d-105">Vous pouvez mettre à jour les valeurs des propriétés non-clés des instances de classe de vue Union.</span><span class="sxs-lookup"><span data-stu-id="9c77d-105">You can update the values of nonkey properties of union view class instances.</span></span> <span data-ttu-id="9c77d-106">Les modifications que vous apportez à l’instance de la classe de vue seront propagées vers les instances de la classe source qui forment la classe d’affichage Union.</span><span class="sxs-lookup"><span data-stu-id="9c77d-106">The changes you make to the view class instance will be propagated back to the source class instances that form the union view class.</span></span>

<span data-ttu-id="9c77d-107">Les restrictions suivantes s’appliquent aux modifications apportées aux instances de classe de vue :</span><span class="sxs-lookup"><span data-stu-id="9c77d-107">The following restrictions apply to changes to view class instances:</span></span>

-   <span data-ttu-id="9c77d-108">Vous ne pouvez pas créer de nouvelles instances de classes d’affichage.</span><span class="sxs-lookup"><span data-stu-id="9c77d-108">You cannot create new instances of view classes.</span></span>
-   <span data-ttu-id="9c77d-109">Seules les classes d’Union prennent en charge les mises à jour ; les vues de jointure et d’association créent des instances de vue en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9c77d-109">Only union classes support updates; join and association views create read-only view instances.</span></span>
-   <span data-ttu-id="9c77d-110">La réussite d’une mise à jour varie selon qu’une instance source peut être mise à jour ou non.</span><span class="sxs-lookup"><span data-stu-id="9c77d-110">Success of an update depends on whether a source instance is updateable.</span></span> <span data-ttu-id="9c77d-111">Si une propriété d’instance de vue est mappée à une propriété en lecture seule d’une instance source, les tentatives de modification de la propriété de vue échouent.</span><span class="sxs-lookup"><span data-stu-id="9c77d-111">If a view instance property maps to a read-only property of a source instance, attempts to modify the view property fail.</span></span>

 

 



