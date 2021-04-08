---
title: UI_PKEY_ItemsSource
description: Identifie la propriété ItemsSource de l’interface utilisateur \_ \_ .
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bdc52a7688648f59be74c22516ee790d109dd2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729469"
---
# <a name="ui_pkey_itemssource"></a><span data-ttu-id="04c6b-103">IU de l’IU \_ \_</span><span class="sxs-lookup"><span data-stu-id="04c6b-103">UI\_PKEY\_ItemsSource</span></span>

<span data-ttu-id="04c6b-104">Identifie la propriété ItemsSource de l’interface utilisateur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="04c6b-104">Identifies the UI\_PKEY\_ItemsSource property.</span></span>

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="04c6b-105">Notes</span><span class="sxs-lookup"><span data-stu-id="04c6b-105">Remarks</span></span>

<span data-ttu-id="04c6b-106">L’interface utilisateur \_ \_ de la bibliothèque d’applications de groupe est utilisée par une application pour interroger la collection d’éléments dans un contrôle Gallery, tel que la barre d’outils accès rapide (qat).</span><span class="sxs-lookup"><span data-stu-id="04c6b-106">UI\_PKEY\_ItemsSource is used by an application to query the collection of items in a gallery control, such as the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="04c6b-107">La valeur de la propriété est un objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="04c6b-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="04c6b-108">Chaque élément de ce [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) doit implémenter [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pour exposer les propriétés en lecture seule associées à l’élément, telles que l’étiquette ou l’image.</span><span class="sxs-lookup"><span data-stu-id="04c6b-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="04c6b-109">Pour ajouter ou supprimer des éléments dans un contrôle Gallery au moment de l’exécution, utilisez les méthodes [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .</span><span class="sxs-lookup"><span data-stu-id="04c6b-109">To add or delete items in a gallery control at run time, use the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) methods.</span></span>

<span data-ttu-id="04c6b-110">La capture d’écran suivante illustre une collection d’éléments dans un menu [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="04c6b-110">The following screen shot illustrates a collection of items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) menu.</span></span>

![capture d’écran montrant des catégories dans une galerie de ruban.](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a><span data-ttu-id="04c6b-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04c6b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04c6b-113">Propriétés de la collection</span><span class="sxs-lookup"><span data-stu-id="04c6b-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 