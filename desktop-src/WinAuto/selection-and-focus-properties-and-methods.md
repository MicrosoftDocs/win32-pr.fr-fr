---
title: Propriétés et méthodes de sélection et de focus
description: À l’instar de nombreux éléments des applications exécutées sur les systèmes d’exploitation Microsoft Windows, les objets accessibles sélectionnent et reçoivent le focus clavier. Ces attributs permettent aux utilisateurs d’interagir avec des éléments d’application, de modifier des valeurs et de les manipuler.
ms.assetid: 8170fe19-f157-4d7d-8eec-d384e51f1560
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbb5eee361707ec4876245eef5b0eb352f8dfd6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728429"
---
# <a name="selection-and-focus-properties-and-methods"></a>Propriétés et méthodes de sélection et de focus

À l’instar de nombreux éléments des applications exécutées sur les systèmes d’exploitation Microsoft Windows, les objets accessibles *sélectionnent* et reçoivent *le focus* clavier. Ces attributs permettent aux utilisateurs d’interagir avec des éléments d’application, de modifier des valeurs et de les manipuler.

Il existe quelques différences clés entre la sélection des objets et le focus de l’objet :

-   Un objet ayant le focus est l’objet de l’ensemble du système d’exploitation qui reçoit l’entrée au clavier. L’objet avec le focus clavier est soit la fenêtre active, soit un objet enfant de la fenêtre active.
-   Un objet sélectionné est marqué pour participer à un type d’opération de groupe.

Par exemple, un utilisateur peut sélectionner plusieurs éléments dans un contrôle List-View, mais le focus est donné à un seul objet dans le système à la fois. Notez que les éléments ayant le focus proviennent d’une sélection d’éléments.

Les clients déterminent si un objet ou un élément enfant accessible particulier a le focus en appelant [**IAccessible :: obtenir \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus). Les clients déterminent si un objet est sélectionné, ou les enfants d’un objet accessible, en appelant [**IAccessible :: obtenir \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection). Pour les objets tels que les contrôles de vue de liste dans lesquels plusieurs enfants sont sélectionnés, l’objet parent doit prendre en charge l’interface [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) , qui permet aux clients d’énumérer les enfants sélectionnés.

## <a name="events-triggered-in-menus"></a>Événements déclenchés dans les menus

Microsoft Active Accessibility expose les menus standard créés avec les API de menu et les fichiers de ressources de Microsoft Win32. Pour être cohérente avec les menus standard, les serveurs avec des menus personnalisés déclenchent [**\_ \_ le focus**](event-constants.md)de l’objet d’événement, et non l’objet d’événement, lorsqu’un utilisateur met en surbrillance un élément de menu. [**\_ \_**](event-constants.md)

> [!Note]  
> Microsoft Active Accessibility ne prend pas en charge la sélection du texte contenu dans les contrôles Edit et Rich Edit, car le texte est exposé sous la forme d’une chaîne unique dans la propriété [**value**](value-property.md) de ces contrôles.

 

## <a name="in-this-section"></a>Dans cette section

-   [Sélection des objets enfants](selecting-child-objects.md)

 

 