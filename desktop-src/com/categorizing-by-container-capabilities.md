---
title: Catégorisation par fonctionnalités de conteneur
description: Les composants requièrent souvent certaines fonctionnalités du conteneur et ne fonctionnent pas avec un conteneur qui ne fournit pas la prise en charge.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987546c20ff77a40666bb74689466a15fab989a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029778"
---
# <a name="categorizing-by-container-capabilities"></a><span data-ttu-id="6c93f-103">Catégorisation par fonctionnalités de conteneur</span><span class="sxs-lookup"><span data-stu-id="6c93f-103">Categorizing by Container Capabilities</span></span>

<span data-ttu-id="6c93f-104">Les composants requièrent souvent certaines fonctionnalités du conteneur et ne fonctionnent pas avec un conteneur qui ne fournit pas la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="6c93f-104">Components often require certain functionality from the container and will not work with a container that does not provide the support.</span></span> <span data-ttu-id="6c93f-105">L’interface utilisateur doit filtrer les composants qui requièrent des fonctionnalités que le conteneur ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="6c93f-105">The user interface should filter out components that require functionality the container does not support.</span></span> <span data-ttu-id="6c93f-106">Pour ce faire, les composants peuvent être catégorisés par la fonctionnalité de conteneur requise.</span><span class="sxs-lookup"><span data-stu-id="6c93f-106">To accomplish this, components can be categorized by the required container functionality.</span></span>

<span data-ttu-id="6c93f-107">Voici un exemple de composants qui requièrent des fonctionnalités du conteneur et qui ne fonctionnent pas dans les conteneurs qui ne prennent pas en charge cette fonctionnalité. il s’agit de contrôles OLE Frame simples.</span><span class="sxs-lookup"><span data-stu-id="6c93f-107">An example of components that require functionality from the container and do not work in containers that do not support that functionality are simple frame OLE controls.</span></span> <span data-ttu-id="6c93f-108">La catégorisation par fonctionnalités de conteneur est effectuée par une clé de Registre supplémentaire au sein de la clé CLSID du composant :</span><span class="sxs-lookup"><span data-stu-id="6c93f-108">Categorizing by container capabilities is accomplished by an additional registry key within the component's CLSID key:</span></span>

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

<span data-ttu-id="6c93f-109">Comme indiqué dans cet exemple, un composant peut appartenir à des catégories de composants qui indiquent les fonctionnalités prises en charge ainsi que les catégories de composants qui indiquent les fonctionnalités requises.</span><span class="sxs-lookup"><span data-stu-id="6c93f-109">As shown in this example, a component can belong to component categories that indicate supported functionality as well as to component categories that indicate required functionality.</span></span>

<span data-ttu-id="6c93f-110">Dans l’exemple suivant, le contrôle Button est un contrôle OLE générique qui ne prend pas en charge les fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="6c93f-110">In the following example, the button control is a generic OLE control that supports no additional functionality.</span></span> <span data-ttu-id="6c93f-111">Elle fonctionnera dans n’importe quel conteneur de contrôle OLE.</span><span class="sxs-lookup"><span data-stu-id="6c93f-111">It will work in any OLE control container.</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

<span data-ttu-id="6c93f-112">Comparez l’exemple précédent à l’exemple suivant dans lequel le MyDBControl peut utiliser Visual Basic la liaison de données si le conteneur le prend en charge.</span><span class="sxs-lookup"><span data-stu-id="6c93f-112">Compare the preceding example with the next example in which the MyDBControl can use Visual Basic data binding if the container supports it.</span></span> <span data-ttu-id="6c93f-113">Toutefois, il a été défini de manière à fonctionner dans des conteneurs qui ne prennent pas en charge la liaison de données Visual Basic (par exemple, une API de base de données différente) :</span><span class="sxs-lookup"><span data-stu-id="6c93f-113">However, it has been defined so that it will work in containers that do not support Visual Basic data binding (perhaps by a different database API):</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

<span data-ttu-id="6c93f-114">Le contrôle GroupBox est un contrôle Frame simple.</span><span class="sxs-lookup"><span data-stu-id="6c93f-114">The GroupBox control is a simple frame control.</span></span> <span data-ttu-id="6c93f-115">Il s’appuie sur le conteneur qui implémente l’interface [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) et fonctionnera correctement uniquement dans ces conteneurs :</span><span class="sxs-lookup"><span data-stu-id="6c93f-115">It relies on the container implementing the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface and will work correctly only in such containers:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

<span data-ttu-id="6c93f-116">Un conteneur qui prend en charge Visual Basic contrôles liés aux données mais ne prend pas en charge les contrôles Frame simples qui spécifient \_ le contrôle CATID et \_ le CATID VBDatabound à l’interface utilisateur du contrôle Insert.</span><span class="sxs-lookup"><span data-stu-id="6c93f-116">A container that supports Visual Basic data bound controls but does not support simple frame controls would specify CATID\_Control and CATID\_VBDatabound to the insert control user interface.</span></span> <span data-ttu-id="6c93f-117">La liste de contrôles affichée à l’utilisateur doit contenir le \_ bouton CLSID et le CLSID \_ MyDBControl.</span><span class="sxs-lookup"><span data-stu-id="6c93f-117">The list of controls displayed to the user would contain the CLSID\_Button and CLSID\_MyDBControl.</span></span> <span data-ttu-id="6c93f-118">Le \_ GroupBox CLSID ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="6c93f-118">CLSID\_GroupBox would not be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c93f-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6c93f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c93f-120">Association d’icônes à une catégorie</span><span class="sxs-lookup"><span data-stu-id="6c93f-120">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="6c93f-121">Catégorisation par fonctionnalités de composant</span><span class="sxs-lookup"><span data-stu-id="6c93f-121">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="6c93f-122">Classes et associations par défaut</span><span class="sxs-lookup"><span data-stu-id="6c93f-122">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="6c93f-123">Définition des catégories de composants</span><span class="sxs-lookup"><span data-stu-id="6c93f-123">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="6c93f-124">Gestionnaire de catégories de composants</span><span class="sxs-lookup"><span data-stu-id="6c93f-124">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




