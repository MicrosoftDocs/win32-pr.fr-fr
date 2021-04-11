---
title: Association d’icônes à une catégorie
description: Association d’icônes à une catégorie
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c7a662ab3aaf578f037ff246207d03e4fcd688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028737"
---
# <a name="associating-icons-with-a-category"></a><span data-ttu-id="05879-103">Association d’icônes à une catégorie</span><span class="sxs-lookup"><span data-stu-id="05879-103">Associating Icons with a Category</span></span>

<span data-ttu-id="05879-104">La création d’une interface utilisateur qui permet à l’utilisateur de sélectionner des catégories de composants dans une catégorie nécessite la possibilité d’afficher une image significative pour une catégorie particulière.</span><span class="sxs-lookup"><span data-stu-id="05879-104">Building a user interface that allows the user to select component categories within a category requires the ability to display a meaningful image for a particular category.</span></span> <span data-ttu-id="05879-105">Pour associer une icône à une catégorie de composant, créez une clé pour le CATID de la catégorie et remplissez cette clé avec une sous-clé [DefaultIcon](defaulticon.md) .</span><span class="sxs-lookup"><span data-stu-id="05879-105">To associate an icon with a component category, create a key for the category's CATID and populate that key with a [DefaultIcon](defaulticon.md) subkey.</span></span> <span data-ttu-id="05879-106">L’entrée de Registre est la suivante :</span><span class="sxs-lookup"><span data-stu-id="05879-106">The registry entry is as follows:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

<span data-ttu-id="05879-107">Le nom de fichier référencé par la clé DefaultIcon peut être un fichier EXE ou une DLL (DLL de ressources uniquement).</span><span class="sxs-lookup"><span data-stu-id="05879-107">The filename referenced by the DefaultIcon key can be either an EXE or a DLL file (resource-only DLL).</span></span>

<span data-ttu-id="05879-108">Pour associer une petite image de la boîte à outils à une petite image de la boîte à outils, créez une clé dans le **\_ \_ \\ CLSID racine des classes HKEY** pour le CATID de la catégorie et remplissez cette clé avec une sous-clé [ToolboxBitmap32](toolboxbitmap32.md) , comme illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="05879-108">To associate a small 16x16 "toolbox bitmap" with a component category, create a key in **HKEY\_CLASSES\_ROOT\\CLSID** for the category's CATID and populate that key with a [ToolBoxBitmap32](toolboxbitmap32.md) subkey, as shown in the following example:</span></span>

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

<span data-ttu-id="05879-109">Le nom de fichier référencé par la clé [ToolboxBitmap32](toolboxbitmap32.md) peut également être un fichier exe ou DLL (dll de ressources uniquement).</span><span class="sxs-lookup"><span data-stu-id="05879-109">The filename referenced by the [ToolBoxBitmap32](toolboxbitmap32.md) key can also be an EXE or DLL file (resource-only DLL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="05879-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05879-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05879-111">Catégorisation par fonctionnalités de composant</span><span class="sxs-lookup"><span data-stu-id="05879-111">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="05879-112">Catégorisation par fonctionnalités de conteneur</span><span class="sxs-lookup"><span data-stu-id="05879-112">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="05879-113">Classes et associations par défaut</span><span class="sxs-lookup"><span data-stu-id="05879-113">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="05879-114">Définition des catégories de composants</span><span class="sxs-lookup"><span data-stu-id="05879-114">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="05879-115">**ICatInformation**</span><span class="sxs-lookup"><span data-stu-id="05879-115">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[<span data-ttu-id="05879-116">**ICatRegister**</span><span class="sxs-lookup"><span data-stu-id="05879-116">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[<span data-ttu-id="05879-117">Gestionnaire de catégories de composants</span><span class="sxs-lookup"><span data-stu-id="05879-117">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




