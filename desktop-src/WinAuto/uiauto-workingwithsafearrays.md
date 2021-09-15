---
title: meilleures pratiques pour l’utilisation de Coffre des tableaux
description: De nombreuses méthodes d’interface de Microsoft UI Automation \ 32 ; L’API prend des arguments appelés tableaux sécurisés, du type de données SAFEARRAY. Cette rubrique décrit les meilleures pratiques pour l’utilisation de tableaux sécurisés dans une application UI Automation.
ms.assetid: 07e87cfd-d565-41b5-a68d-b99dd191fa95
keywords:
- UI Automation, tableaux sécurisés
- UI Automation, fournisseurs
- UI Automation, clients
- UI Automation, conversion entre types de données
- clients, tableaux sécurisés
- fournisseurs, UI Automation
- tableaux sécurisés
- types de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ade30398f8fbeb43336707f66a0709dfab83d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403966"
---
# <a name="best-practices-for-using-safe-arrays"></a>meilleures pratiques pour l’utilisation de Coffre des tableaux

De nombreuses méthodes d’interface de l’API d’automatisation d’interface utilisateur de Microsoft acceptent des arguments appelés tableaux sécurisés, du type de données [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) . Cette rubrique décrit les meilleures pratiques pour l’utilisation de tableaux sécurisés dans une application UI Automation.

## <a name="clients"></a>Clients

Tous les tableaux sécurisés qui sont utilisés avec les méthodes de l’API du client UI Automation sont des tableaux unidimensionnels de base zéro. Pour créer un tableau sécurisé pour une méthode de client UI Automation, utilisez la fonction [**SafeArrayCreateVector**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreatevector) , et pour lire et écrire dans un tableau sécurisé, utilisez les fonctions [**SafeArrayGetElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraygetelement) et [**SafeArrayPutElement**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayputelement) . Lorsque vous avez fini d’utiliser un tableau sécurisé, détruisez-le toujours à l’aide de la fonction [**SafeArrayDestroy**](/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy) , que vous ayez créé ou reçu le tableau sécurisé à partir d’une méthode de client UI Automation.

Plusieurs méthodes UI Automation, y compris les méthodes de récupération de propriété telles que [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue), récupèrent des [**variantes**](/windows/win32/api/oaidl/ns-oaidl-variant)qui peuvent contenir des structures [**point**](/previous-versions//dd162805(v=vs.85)) ou [**UiaRect**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect) . Un **point** est empaqueté dans un **Variant** comme un tableau sécurisé de doubles (VT \_ R8) avec le membre **x** à l’index 0, et le membre **y** à l’index 1. De même, un **UiaRect** est empaqueté dans un **Variant** comme un tableau sécurisé de doubles avec les membres de **gauche**, de **haut**, de **largeur** et de **hauteur** aux index 0 à 3, respectivement. Pour un tableau de structures **UiaRect** , le tableau Safe contient un tableau séquentiel de quatre doubles pour chaque **UiaRect**. Les membres **gauche**, **supérieur**, **largeur** et **hauteur** du premier **UiaRect** occupent l’index 0 à 3, les membres du deuxième rectangle occupent l’index 4 jusqu’à 7, et ainsi de suite.

L’interface [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) comprend les méthodes suivantes pour la conversion entre [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) et différents autres types de données.



| Méthode                                                                                               | Description                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IUIAutomation::IntNativeArrayToSafeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intnativearraytosafearray)   | Convertit un tableau d’entiers en [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).                                          |
| [**IUIAutomation::IntSafeArrayToNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-intsafearraytonativearray)   | Convertit un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) d’entiers en tableau.                                          |
| [**IUIAutomation::SafeArrayToRectNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray) | Convertit un [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) qui contient des coordonnées de rectangle en tableau de type **Rect**. |



 

## <a name="providers"></a>Fournisseurs

Un fournisseur doit implémenter un certain nombre de méthodes d’interface appelées par UI Automation pour récupérer des informations à partir du fournisseur. De nombreuses fois, ces informations se composent d’un tableau de valeurs. Pour retourner un tableau à UI Automation, le fournisseur doit empaqueter le tableau dans une structure [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) . Les éléments de tableau doivent être du type de données attendu et doivent apparaître dans l’ordre attendu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des propriétés UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Notions de base d’UI Automation](entry-uiautocore-overview.md)
</dt> </dl>

 

 