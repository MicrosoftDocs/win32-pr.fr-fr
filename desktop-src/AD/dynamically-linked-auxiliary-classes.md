---
title: Classes auxiliaires liées de manière dynamique
description: Une classe auxiliaire liée de manière dynamique est une classe qui est attachée à un objet individuel, plutôt qu’à une classe d’objet.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- Active Directory des classes auxiliaires liées de manière dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0cacb09d3aef05bcaf0ef729411c2e023469be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190771"
---
# <a name="dynamically-linked-auxiliary-classes"></a><span data-ttu-id="4f226-104">Classes auxiliaires liées de manière dynamique</span><span class="sxs-lookup"><span data-stu-id="4f226-104">Dynamically Linked Auxiliary Classes</span></span>

<span data-ttu-id="4f226-105">Une classe auxiliaire liée de manière dynamique est une classe qui est attachée à un objet individuel, plutôt qu’à une classe d’objet.</span><span class="sxs-lookup"><span data-stu-id="4f226-105">A dynamically linked auxiliary class is a class that is attached to an individual object, rather than to an object class.</span></span> <span data-ttu-id="4f226-106">La liaison dynamique vous permet de stocker des attributs supplémentaires avec un objet individuel sans l’impact à l’échelle de la forêt de l’extension de la définition de schéma pour une classe entière.</span><span class="sxs-lookup"><span data-stu-id="4f226-106">Dynamic linking enables you to store additional attributes with an individual object without the forest-wide impact of extending the schema definition for an entire class.</span></span> <span data-ttu-id="4f226-107">Par exemple, une entreprise peut utiliser la liaison dynamique pour attacher une classe auxiliaire spécifique aux ventes aux objets utilisateur de ses commerciaux, ainsi qu’à d’autres classes auxiliaires spécifiques au département, aux objets utilisateur des employés d’autres services.</span><span class="sxs-lookup"><span data-stu-id="4f226-107">For example, an enterprise could use dynamic linking to attach a sales-specific auxiliary class to the user objects of its sales people, and other department-specific auxiliary classes to the user objects of employees in other departments.</span></span>

<span data-ttu-id="4f226-108">La liaison dynamique n’est pas complexe : ajoutez le nom de la classe auxiliaire aux valeurs de l’attribut **objectClass** d’un objet.</span><span class="sxs-lookup"><span data-stu-id="4f226-108">Dynamic linking is not complex: add the name of the auxiliary class to the values of an object's **objectClass** attribute.</span></span> <span data-ttu-id="4f226-109">Si la classe auxiliaire possède des attributs obligatoires (**musthave** ou **systemMustHave**), vous devez les définir en même temps.</span><span class="sxs-lookup"><span data-stu-id="4f226-109">If the auxiliary class has any mandatory attributes (**mustHave** or **systemMustHave**), you must set them at the same time.</span></span> <span data-ttu-id="4f226-110">Pour plus d’informations et pour obtenir un exemple de code, consultez [Ajout d’une classe auxiliaire à une instance d’objet](adding-an-auxiliary-class-to-an-object-instance.md).</span><span class="sxs-lookup"><span data-stu-id="4f226-110">For more information and a code example, see [Adding an Auxiliary Class to an Object Instance](adding-an-auxiliary-class-to-an-object-instance.md).</span></span>

<span data-ttu-id="4f226-111">Pour supprimer une classe auxiliaire liée de manière dynamique, effacez les valeurs de tous les attributs de la classe auxiliaire, puis supprimez le nom de la classe auxiliaire de l’attribut **objectClass** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4f226-111">To remove a dynamically linked auxiliary class, clear the values of all attributes from the auxiliary class, and then remove the name of the auxiliary class from the **objectClass** attribute of the object.</span></span>

<span data-ttu-id="4f226-112">Si vous ajoutez dynamiquement une classe auxiliaire qui est une sous-classe d’une autre classe auxiliaire, les deux classes auxiliaires sont ajoutées à l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="4f226-112">If you dynamically add an auxiliary class that is a subclass of another auxiliary class, both auxiliary classes are added to the target object.</span></span> <span data-ttu-id="4f226-113">Toutefois, la suppression de la classe auxiliaire enfant ne supprime pas son parent ; chaque classe doit être supprimée explicitement.</span><span class="sxs-lookup"><span data-stu-id="4f226-113">However, removing the child auxiliary class does not remove its parent; each class must be explicitly removed.</span></span>

 

 




