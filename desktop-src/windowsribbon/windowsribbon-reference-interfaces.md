---
title: Interfaces (infrastructure du ruban)
description: documentation de référence pour les interfaces de l’infrastructure de ruban Windows.
ms.assetid: d5fd6e4f-ca10-4010-aab4-d2728b0ac53c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c168a342b7f362d2d679d578a88011c9d14977
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404731"
---
# <a name="interfaces-ribbon-framework"></a>Interfaces (infrastructure du ruban)

documentation de référence pour les interfaces de l’infrastructure de ruban Windows.

### <a name="interfaces"></a>Interfaces



| Rubrique                                                                                  | Contenu                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | L’interface [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) est implémentée par l’application et définit les méthodes de point d’entrée de rappel pour l’infrastructure du ruban.<br/>                                                                                                                                                                                                              |
| [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)                         | L’interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) est implémentée par l’infrastructure du ruban. L’interface **IUICollection** définit les méthodes de manipulation dynamique des contrôles basés sur une collection, tels que les diverses [galeries](ribbon-controls-galleries.md) de ruban et la barre d’outils accès rapide (qat) au moment de l’exécution.<br/>                                              |
| [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | L’interface [**IUICollectionChangedEvent**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) est implémentée par l’application et définit la méthode requise pour gérer les modifications apportées à une collection au moment de l’exécution.<br/>                                                                                                                                                                                |
| [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | L’interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) est implémentée par l’application et définit les méthodes de collecte des informations de commande et de gestion des événements de commande à partir de l’infrastructure du ruban.<br/>                                                                                                                                                              |
| [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)                     | L’interface [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)est implémentée par l’infrastructure du ruban et fournit les fonctionnalités de base de la vue [contextuelle](windowsribbon-controls-contextpopup.md)contextuelle.<br/>                                                                                                                                                                       |
| [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                           | L’interface [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) est implémentée par l’infrastructure du ruban et définit les méthodes qui fournissent les fonctionnalités de base pour le Framework.<br/>                                                                                                                                                                                                     |
| [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                   | L’interface [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) est implémentée par l’application et définit la méthode pour récupérer une image à afficher dans l’interface utilisateur contextuelle du ruban et du contexte de l’infrastructure du ruban.<br/>                                                                                                                                                                          |
| [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)               | [**IUIImageFromBitmap**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap) est une interface de fabrique implémentée par l’infrastructure de ruban qui définit la méthode de création d’un objet [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) .<br/>                                                                                                                                                             |
| [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                                 | L’interface [**IUIRibbon**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) est implémentée par l’infrastructure du ruban et offre la possibilité de spécifier des paramètres et des propriétés pour un ruban. <br/>                                                                                                                                                                                                               |
| [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)           | [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)est une interface en lecture seule qui définit une méthode de récupération de la valeur identifiée par une clé de propriété. Cette interface est implémentée par l’infrastructure du ruban et est également implémentée par l’application hôte pour chaque élément de l’objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)d’une galerie d’éléments.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Informations de référence sur l’infrastructure du ruban](windowsribbon-reference-entry.md)
</dt> </dl>

 

