---
title: Classes auxiliaires dynamiques
description: À l’instar des classes d’objets structurelles et abstraites, les classes auxiliaires sont définies par un objet classSchema dans le schéma Active Directory.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- Active Directory des classes auxiliaires dynamiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c13fc8231b5232b82a61b9409f1736e5bd9249
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462875"
---
# <a name="dynamic-auxiliary-classes"></a><span data-ttu-id="8913f-104">Classes auxiliaires dynamiques</span><span class="sxs-lookup"><span data-stu-id="8913f-104">Dynamic Auxiliary Classes</span></span>

<span data-ttu-id="8913f-105">À l’instar des classes d’objets structurelles et abstraites, les classes auxiliaires sont définies par un objet [**classSchema**](/windows/desktop/ADSchema/c-classschema) dans le schéma Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8913f-105">Similar to structural and abstract object classes, auxiliary classes are defined by a [**classSchema**](/windows/desktop/ADSchema/c-classschema) object in the Active Directory schema.</span></span> <span data-ttu-id="8913f-106">Pour plus d’informations, consultez [classes structurelles, abstraites et auxiliaires](structural-abstract-and-auxiliary-classes.md).</span><span class="sxs-lookup"><span data-stu-id="8913f-106">For more information, see [Structural, Abstract, and Auxiliary Classes](structural-abstract-and-auxiliary-classes.md).</span></span> <span data-ttu-id="8913f-107">Cette définition de schéma spécifie différentes caractéristiques de la classe, y compris les attributs associés à la classe.</span><span class="sxs-lookup"><span data-stu-id="8913f-107">This schema definition specifies various characteristics of the class, including the attributes associated with the class.</span></span>

<span data-ttu-id="8913f-108">Contrairement aux classes structurelles, vous ne pouvez pas créer une instance d’une classe auxiliaire comme vous pouvez le faire avec une classe structurelle.</span><span class="sxs-lookup"><span data-stu-id="8913f-108">Unlike with structural classes, You cannot create an instance of an auxiliary class as you can with a structural class.</span></span> <span data-ttu-id="8913f-109">Au lieu de cela, vous utilisez une classe auxiliaire pour étendre la liste des attributs qui est associée à une autre classe d’objets structurelle, abstraite ou auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="8913f-109">Instead, you use an auxiliary class to extend the list of attributes that is associated with another structural, abstract, or auxiliary object class.</span></span>

<span data-ttu-id="8913f-110">Dans la version initiale de Windows 2000, Active Directory Domain Services fourni la prise en charge de la liaison statique des classes auxiliaires à la définition [**classSchema**](/windows/desktop/ADSchema/c-classschema) d’une autre classe d’objets.</span><span class="sxs-lookup"><span data-stu-id="8913f-110">In the initial release of Windows 2000, Active Directory Domain Services provided support for statically linking auxiliary classes to the [**classSchema**](/windows/desktop/ADSchema/c-classschema) definition of another object class.</span></span> <span data-ttu-id="8913f-111">Quand une classe auxiliaire est utilisée de cette façon, chaque instance de la classe d’objet prend en charge les attributs de la classe auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="8913f-111">When an auxiliary class is used in this way, every instance of the object class supports the attributes of the auxiliary class.</span></span>

<span data-ttu-id="8913f-112">**Windows 2000 Server et versions antérieures :** Active Directory Domain Services ne prend pas en charge la liaison dynamique des classes auxiliaires à des objets individuels, et pas seulement à des classes entières d’objets.</span><span class="sxs-lookup"><span data-stu-id="8913f-112">**Windows 2000 Server and earlier:** Active Directory Domain Services does not provide support for dynamically linking auxiliary classes to individual objects, and not just to entire classes of objects.</span></span> <span data-ttu-id="8913f-113">En outre, les classes auxiliaires qui ont été attachées à une instance d’objet ne peuvent pas être supprimées par la suite de l’instance.</span><span class="sxs-lookup"><span data-stu-id="8913f-113">In addition, auxiliary classes that have been attached to an object instance cannot subsequently be removed from the instance.</span></span>

<span data-ttu-id="8913f-114">**Windows Server 2003 :** Les classes auxiliaires dynamiques sont prises en charge lorsque tous les contrôleurs de domaine de la forêt exécutent Windows Server 2003 et le mode fonctionnel de la forêt est Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8913f-114">**Windows Server 2003:** Dynamic Auxiliary Classes are supported when all domain controllers in the forest are running Windows Server 2003 and the forest functional mode is Windows Server 2003.</span></span>

<span data-ttu-id="8913f-115">Pour plus d’informations sur les classes auxiliaires, consultez :</span><span class="sxs-lookup"><span data-stu-id="8913f-115">For more information about auxiliary classes, see:</span></span>

-   [<span data-ttu-id="8913f-116">Classes auxiliaires liées de manière dynamique</span><span class="sxs-lookup"><span data-stu-id="8913f-116">Dynamically Linked Auxiliary Classes</span></span>](dynamically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="8913f-117">Classes auxiliaires liées statiquement</span><span class="sxs-lookup"><span data-stu-id="8913f-117">Statically Linked Auxiliary Classes</span></span>](statically-linked-auxiliary-classes.md)
-   [<span data-ttu-id="8913f-118">Détermination des classes associées à une instance d’objet</span><span class="sxs-lookup"><span data-stu-id="8913f-118">Determining the Classes Associated With an Object Instance</span></span>](determining-the-classes-associated-with-an-object-instance.md)
-   [<span data-ttu-id="8913f-119">Ajout d’une classe auxiliaire à une instance d’objet</span><span class="sxs-lookup"><span data-stu-id="8913f-119">Adding an Auxiliary Class to an Object Instance</span></span>](adding-an-auxiliary-class-to-an-object-instance.md)

<span data-ttu-id="8913f-120">Pour plus d’informations sur les niveaux fonctionnels de forêt, consultez la rubrique « Comment élever Active Directory niveaux fonctionnels de domaine et de forêt » dans la base de connaissances de l’aide et du support à l’adresse [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .</span><span class="sxs-lookup"><span data-stu-id="8913f-120">For more information about forest functional levels, see "How to raise Active Directory domain and forest functional levels" in the Help and Support Knowledge Base at [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692).</span></span>

 

 