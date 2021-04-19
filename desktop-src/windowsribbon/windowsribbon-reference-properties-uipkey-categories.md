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
# <a name="ui_pkey_categories"></a>Catégories d’IU de l’interface utilisateur \_ \_

Identifie la propriété des catégories d’IU de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Notes

\_ \_ Les catégories de groupe de lignes de l’interface utilisateur sont utilisées par une application pour interroger les catégories utilisées pour regrouper des éléments connexes dans un contrôle de Galerie.

La valeur de propriété est un objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) dans lequel chaque élément de la collection représente une catégorie.

Chaque élément de ce [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) doit implémenter [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pour exposer les propriétés en lecture seule associées à l’élément, telles que l’étiquette ou l’image.

Pour ajouter ou supprimer des éléments dans un contrôle Gallery au moment de l’exécution, utilisez les différentes méthodes de [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).

La capture d’écran suivante illustre l’utilisation de deux catégories, les **formes de sélection** et les options de **sélection**, dans un menu [**SplitButton**](windowsribbon-element-splitbutton.md) .

![capture d’écran montrant deux catégories, les formes de sélection et les options de sélection dans un contrôle splitbuttongallery.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés de la collection](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[Code de catégorie d’interface utilisateur \_ \_](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 