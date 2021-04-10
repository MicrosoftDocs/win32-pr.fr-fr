---
title: GUID de cohérence
description: Les GUID de cohérence sont une stratégie de détection qui permet à une application de détecter des mises à jour partielles.
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcfb25d0f04a459217811a2ff0393fac47e3206
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028504"
---
# <a name="consistency-guids"></a><span data-ttu-id="67df1-103">GUID de cohérence</span><span class="sxs-lookup"><span data-stu-id="67df1-103">Consistency GUIDs</span></span>

<span data-ttu-id="67df1-104">Les GUID de cohérence sont une stratégie de détection qui permet à une application de détecter des mises à jour partielles.</span><span class="sxs-lookup"><span data-stu-id="67df1-104">Consistency GUIDs are a detection strategy that allows an application to detect partial updates.</span></span> <span data-ttu-id="67df1-105">Un GUID de cohérence (identificateur global unique) est appliqué à chaque objet dans un ensemble associé.</span><span class="sxs-lookup"><span data-stu-id="67df1-105">A consistency GUID (Globally Unique IDentifier) is applied to each object in a related set.</span></span> <span data-ttu-id="67df1-106">Dans l’implémentation, une application source génère un nouveau GUID et l’applique à chaque objet qu’elle met à jour dans le jeu d’objets connexes.</span><span class="sxs-lookup"><span data-stu-id="67df1-106">In implementation, a source application generates a new GUID and applies it to each object it updates in the set of related objects.</span></span> <span data-ttu-id="67df1-107">Il applique ensuite le nouveau GUID au reste des objets de l’ensemble, et se termine en appliquant le nouveau GUID à l’objet « Master ».</span><span class="sxs-lookup"><span data-stu-id="67df1-107">It then applies the new GUID to the rest of the objects in the set, and finishes by applying the new GUID to the "master" object.</span></span> <span data-ttu-id="67df1-108">En général, l’objet « maître » est un conteneur qui est le parent des autres objets de l’ensemble.</span><span class="sxs-lookup"><span data-stu-id="67df1-108">Typically, the "master" object will be a container that is the parent of the other objects in the set.</span></span>

<span data-ttu-id="67df1-109">Quelques points importants à prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="67df1-109">Some important considerations:</span></span>

-   <span data-ttu-id="67df1-110">Les GUID de cohérence combinés avec les nombres d’objets ou les sommes de contrôle sont plus efficaces que les GUID de cohérence seuls, car l’application qui lit les objets peut ne pas savoir combien d’objets avec le GUID doivent être présents.</span><span class="sxs-lookup"><span data-stu-id="67df1-110">Consistency GUIDs combined with object counts or checksums are more effective than consistency GUIDs alone, because the application reading the objects may not know how many objects with the GUID should be present.</span></span>
-   <span data-ttu-id="67df1-111">Les applications doivent générer leurs propres GUID (une API Microsoft Win32, UuidCreate, fournit cette fonction) et ne pas utiliser les GUID générés par le système qui se trouvent dans l’attribut **objectGUID** d’un objet.</span><span class="sxs-lookup"><span data-stu-id="67df1-111">Applications must generate their own GUIDs (a Microsoft Win32 API, UuidCreate, provides this function), and not use the system-generated GUIDs found in an object's **objectGUID** attribute.</span></span> <span data-ttu-id="67df1-112">Cela est dû au fait qu’un GUID de cohérence doit changer chaque fois que l’ensemble d’objets est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="67df1-112">This is because a consistency GUID needs to change each time the set of objects is updated.</span></span> <span data-ttu-id="67df1-113">Les GUID d’identité d’objet trouvés dans **objectGUID** ne changent jamais après la création de l’objet.</span><span class="sxs-lookup"><span data-stu-id="67df1-113">Object identity GUIDs found in **objectGUID** never change after the object has been created.</span></span>
-   <span data-ttu-id="67df1-114">Les GUID de cohérence supposent qu’aucun objet n’est partagé entre les ensembles, donc chaque ensemble peut avoir un GUID de cohérence unique.</span><span class="sxs-lookup"><span data-stu-id="67df1-114">Consistency GUIDs assume that no object is shared among sets, so each set can have a unique consistency GUID.</span></span>

 

 




