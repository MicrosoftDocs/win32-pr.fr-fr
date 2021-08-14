---
title: UI_PKEY_ItemsSource
description: Identifie la propriété ItemsSource de l’interface utilisateur \_ \_ .
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017a3fc8f05c24c8d1996202b1db08a459f1a3747e3f787b521a70e6e3a25df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201568"
---
# <a name="ui_pkey_itemssource"></a>IU de l’IU \_ \_

Identifie la propriété ItemsSource de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ de la bibliothèque d’applications de groupe est utilisée par une application pour interroger la collection d’éléments dans un contrôle Gallery, tel que la barre d’outils accès rapide (qat).

La valeur de la propriété est un objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

Chaque élément de ce [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) doit implémenter [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pour exposer les propriétés en lecture seule associées à l’élément, telles que l’étiquette ou l’image.

Pour ajouter ou supprimer des éléments dans un contrôle Gallery au moment de l’exécution, utilisez les méthodes [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

La capture d’écran suivante illustre une collection d’éléments dans un menu [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

![capture d’écran montrant des catégories dans une galerie de ruban.](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés de la collection](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 