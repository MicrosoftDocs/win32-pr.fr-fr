---
title: UI_PKEY_Categories
description: Identifie la propriété des catégories d’IU de l’interface utilisateur \_ \_ .
ms.assetid: 15f97307-ea3d-407a-a276-46b82f81bdbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7666ee9eba6639f1f39b96f012b464854191ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509454"
---
# <a name="ui_pkey_categories"></a><span data-ttu-id="d2789-103">Catégories d’IU de l’interface utilisateur \_ \_</span><span class="sxs-lookup"><span data-stu-id="d2789-103">UI\_PKEY\_Categories</span></span>

<span data-ttu-id="d2789-104">Identifie la propriété des catégories d’IU de l’interface utilisateur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d2789-104">Identifies the UI\_PKEY\_Categories property.</span></span>

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="d2789-105">Notes</span><span class="sxs-lookup"><span data-stu-id="d2789-105">Remarks</span></span>

<span data-ttu-id="d2789-106">\_ \_ Les catégories de groupe de lignes de l’interface utilisateur sont utilisées par une application pour interroger les catégories utilisées pour regrouper des éléments connexes dans un contrôle de Galerie.</span><span class="sxs-lookup"><span data-stu-id="d2789-106">UI\_PKEY\_Categories is used by an application to query the categories that are used to group related items in a gallery control.</span></span>

<span data-ttu-id="d2789-107">La valeur de propriété est un objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) dans lequel chaque élément de la collection représente une catégorie.</span><span class="sxs-lookup"><span data-stu-id="d2789-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object where each item in the collection represents a category.</span></span>

<span data-ttu-id="d2789-108">Chaque élément de ce [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) doit implémenter [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pour exposer les propriétés en lecture seule associées à l’élément, telles que l’étiquette ou l’image.</span><span class="sxs-lookup"><span data-stu-id="d2789-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="d2789-109">Pour ajouter ou supprimer des éléments dans un contrôle Gallery au moment de l’exécution, utilisez les différentes méthodes de [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span><span class="sxs-lookup"><span data-stu-id="d2789-109">To add or delete items in a gallery control at run time, use the various methods of [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span></span>

<span data-ttu-id="d2789-110">La capture d’écran suivante illustre l’utilisation de deux catégories, les **formes de sélection** et les options de **sélection**, dans un menu [**SplitButton**](windowsribbon-element-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="d2789-110">The following screen shot illustrates the use of two categories, **Selection shapes** and **Selection options**, in a [**SplitButton**](windowsribbon-element-splitbutton.md) menu.</span></span>

![capture d’écran montrant deux catégories, les formes de sélection et les options de sélection dans un contrôle splitbuttongallery.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a><span data-ttu-id="d2789-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d2789-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2789-113">Propriétés de la collection</span><span class="sxs-lookup"><span data-stu-id="d2789-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="d2789-114">Code de catégorie d’interface utilisateur \_ \_</span><span class="sxs-lookup"><span data-stu-id="d2789-114">UI\_PKEY\_CategoryId</span></span>](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 