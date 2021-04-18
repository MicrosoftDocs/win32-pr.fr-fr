---
title: Catégorisation par fonctionnalités de composant
description: Les catégories de composants peuvent être utilisées pour afficher un sous-ensemble de tous les composants installés.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff44e03e9eae0226ac57279c37d4a5dfd32fc6bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512649"
---
# <a name="categorizing-by-component-capabilities"></a><span data-ttu-id="c2c53-103">Catégorisation par fonctionnalités de composant</span><span class="sxs-lookup"><span data-stu-id="c2c53-103">Categorizing by Component Capabilities</span></span>

<span data-ttu-id="c2c53-104">Les catégories de composants peuvent être utilisées pour afficher un sous-ensemble de tous les composants installés.</span><span class="sxs-lookup"><span data-stu-id="c2c53-104">Component categories can be used to display a subset of all of the installed components.</span></span> <span data-ttu-id="c2c53-105">Chaque catégorie de composant est identifiée par un GUID, connu sous le nom d’ID de catégorie (CATID).</span><span class="sxs-lookup"><span data-stu-id="c2c53-105">Each component category is identified by a GUID, referred to as a Category ID (CATID).</span></span> <span data-ttu-id="c2c53-106">Chaque CATID contient une liste de noms explicites et explicites qui lui sont associés.</span><span class="sxs-lookup"><span data-stu-id="c2c53-106">Each CATID has a list of locale-tagged, human-readable names associated with it.</span></span> <span data-ttu-id="c2c53-107">Une liste des CATID et des noms explicites est stockée dans un emplacement bien connu du Registre.</span><span class="sxs-lookup"><span data-stu-id="c2c53-107">A listing of the CATIDs and the human-readable names is stored in a well-known location in the registry.</span></span>

<span data-ttu-id="c2c53-108">Par exemple, tous les composants qui implémentent la fonctionnalité d’incorporation de documents OLE peuvent être classés dans une catégorie de composant.</span><span class="sxs-lookup"><span data-stu-id="c2c53-108">For example, all components that implement the functionality for OLE document embedding can be classified within a component category.</span></span> <span data-ttu-id="c2c53-109">Dans le passé, ces objets auraient été identifiés par la clé « Insertable » dans le registre.</span><span class="sxs-lookup"><span data-stu-id="c2c53-109">In the past, these objects would have been identified by the "Insertable" key in the registry.</span></span> <span data-ttu-id="c2c53-110">Pour utiliser des catégories de composant à la place, les informations suivantes sont ajoutées au registre :</span><span class="sxs-lookup"><span data-stu-id="c2c53-110">To use component categories instead, the following information would be added to the registry:</span></span>

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

<span data-ttu-id="c2c53-111">Chaque classe qui implémente les fonctionnalités correspondant à une catégorie de composant répertorie l’ID de catégorie de cette catégorie dans la clé CLSID du Registre.</span><span class="sxs-lookup"><span data-stu-id="c2c53-111">Each class that implements the functionality corresponding to a component category lists the category ID for that category within the CLSID key in the registry.</span></span> <span data-ttu-id="c2c53-112">Étant donné qu’un seul composant peut prendre en charge un large éventail de fonctionnalités, les composants peuvent appartenir à plusieurs catégories de composants.</span><span class="sxs-lookup"><span data-stu-id="c2c53-112">Because a single component can support a wide range of functionality, components can belong to multiple component categories.</span></span> <span data-ttu-id="c2c53-113">Par exemple, un contrôle OLE particulier peut prendre en charge toutes les fonctionnalités requises pour participer en tant qu’incorporation de documents OLE, Microsoft Visual Basic la liaison de données et les fonctionnalités Internet.</span><span class="sxs-lookup"><span data-stu-id="c2c53-113">For example, a particular OLE control might support all of the functionality required to participate as OLE document embedding, Microsoft Visual Basic data binding, and Internet functionality.</span></span> <span data-ttu-id="c2c53-114">Ce type de contrôle aurait les informations suivantes stockées dans sa clé CLSID dans le registre :</span><span class="sxs-lookup"><span data-stu-id="c2c53-114">Such a control would have the following information stored in its CLSID key in the registry:</span></span>

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

<span data-ttu-id="c2c53-115">Grâce à ces informations, un conteneur peut énumérer les contrôles installés sur un système et afficher uniquement les contrôles qui prennent en charge les fonctionnalités requises par le conteneur.</span><span class="sxs-lookup"><span data-stu-id="c2c53-115">With this information, a container can enumerate the controls installed on a system and display only those controls that support the functionality required by the container.</span></span> <span data-ttu-id="c2c53-116">L’utilisation de catégories de composants permet de classer les composants par la fonctionnalité implémentée du composant.</span><span class="sxs-lookup"><span data-stu-id="c2c53-116">The use of component categories provides a way to categorize components by the implemented functionality of the component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2c53-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2c53-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2c53-118">Association d’icônes à une catégorie</span><span class="sxs-lookup"><span data-stu-id="c2c53-118">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="c2c53-119">Catégorisation par fonctionnalités de conteneur</span><span class="sxs-lookup"><span data-stu-id="c2c53-119">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="c2c53-120">Classes et associations par défaut</span><span class="sxs-lookup"><span data-stu-id="c2c53-120">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="c2c53-121">Définition des catégories de composants</span><span class="sxs-lookup"><span data-stu-id="c2c53-121">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="c2c53-122">Gestionnaire de catégories de composants</span><span class="sxs-lookup"><span data-stu-id="c2c53-122">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




