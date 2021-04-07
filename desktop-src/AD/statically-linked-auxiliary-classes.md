---
title: Classes auxiliaires liées statiquement
description: Une classe auxiliaire liée de manière statique est une classe qui est incluse dans l’attribut auxiliaryClass ou systemAuxiliaryClass de la définition de l’objet classSchema d’une classe d’objets dans le schéma.
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- Active Directory des classes auxiliaires liées statiquement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1ef6191834687fc2b7741f097f6bfe75b5ef31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671225"
---
# <a name="statically-linked-auxiliary-classes"></a><span data-ttu-id="90bf2-104">Classes auxiliaires liées statiquement</span><span class="sxs-lookup"><span data-stu-id="90bf2-104">Statically Linked Auxiliary Classes</span></span>

<span data-ttu-id="90bf2-105">Une classe auxiliaire liée de manière statique est une classe qui est incluse dans l’attribut **auxiliaryClass** ou **systemAuxiliaryClass** de la définition de l’objet **classSchema** d’une classe d’objets dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="90bf2-105">A statically linked auxiliary class is one that is included in the **auxiliaryClass** or **systemAuxiliaryClass** attribute of an object class's **classSchema** definition in the schema.</span></span> <span data-ttu-id="90bf2-106">Cela signifie que la classe auxiliaire fait partie de chaque instance de la classe à laquelle elle est associée.</span><span class="sxs-lookup"><span data-stu-id="90bf2-106">This means that the auxiliary class is part of every instance of the class with which it is associated.</span></span>

<span data-ttu-id="90bf2-107">Une classe auxiliaire peut être liée de manière statique à une classe d’objet lorsque la classe est définie, autrement dit, quand son objet **classSchema** est ajouté au conteneur de schéma.</span><span class="sxs-lookup"><span data-stu-id="90bf2-107">An auxiliary class can be statically linked to an object class when the class is defined, that is, when its **classSchema** object is added to the schema container.</span></span> <span data-ttu-id="90bf2-108">Il s’agit de la seule fois où le **systemAuxiliaryClass** peut être utilisé ; après la création d’un objet **classSchema** , son attribut **systemAuxiliaryClass** ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="90bf2-108">This is the only time that the **systemAuxiliaryClass** can be used; after a **classSchema** object is created, its **systemAuxiliaryClass** attribute cannot be modified.</span></span> <span data-ttu-id="90bf2-109">Une classe auxiliaire liée de manière statique à ce moment peut avoir des attributs obligatoires (**musthave**) et/ou facultatifs (**mayHave**).</span><span class="sxs-lookup"><span data-stu-id="90bf2-109">An auxiliary class that is statically linked at this time can have mandatory (**mustHave**) and/or optional (**mayHave**) attributes.</span></span>

<span data-ttu-id="90bf2-110">Un utilisateur privilégié disposant des autorisations nécessaires pour étendre le schéma peut ajouter ou supprimer des classes auxiliaires de l’attribut **systemAuxiliaryClass** d’un objet **classSchema** existant.</span><span class="sxs-lookup"><span data-stu-id="90bf2-110">A privileged user with the permissions required to extend the schema can add or remove auxiliary classes from the **systemAuxiliaryClass** attribute of an existing **classSchema** object.</span></span> <span data-ttu-id="90bf2-111">Cela permet d’ajouter ou de supprimer la classe auxiliaire de chaque instance existante de la classe d’objet.</span><span class="sxs-lookup"><span data-stu-id="90bf2-111">Doing so adds or removes the auxiliary class from every existing instance of the object class.</span></span> <span data-ttu-id="90bf2-112">Une classe auxiliaire liée de manière statique à ce moment peut avoir des attributs facultatifs, mais elle ne peut pas avoir d’attributs obligatoires.</span><span class="sxs-lookup"><span data-stu-id="90bf2-112">An auxiliary class that is statically linked at this time can have optional attributes, but cannot have mandatory attributes.</span></span> <span data-ttu-id="90bf2-113">Cela est dû au fait qu’il peut y avoir des instances existantes de la classe d’objet, auquel cas l’ajout d’un nouvel attribut obligatoire créerait des problèmes.</span><span class="sxs-lookup"><span data-stu-id="90bf2-113">This is because there may be existing instances of the object class, in which case, adding a new mandatory attribute would create problems.</span></span> <span data-ttu-id="90bf2-114">Un utilisateur privilégié peut supprimer par la suite une classe auxiliaire de l’attribut **auxiliaryClass** d’un objet **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="90bf2-114">A privileged user can subsequently remove an auxiliary class from the **auxiliaryClass** attribute of a **classSchema** object.</span></span>

 

 




