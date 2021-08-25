---
title: Implémentation d’un fournisseur UI Automation Client-Side (proxy)
description: Cette rubrique explique comment écrire un fournisseur proxy pour un contrôle non pris en charge et l’ajouter à la liste des proxies utilisés par les applications clientes.
ms.assetid: c66f4a7b-0a12-4c65-a3e9-1c826d54ac6b
keywords:
- UI Automation, implémentation du fournisseur côté client
- UI Automation, implémentation du fournisseur
- UI Automation, implémentation de fournisseurs côté client
- UI Automation, implémenter des fournisseurs
- UI Automation, proxies
- proxies
- fournisseurs côté client
- fournisseurs, implémenter
- implémentation des fournisseurs côté client
- implémenter des fournisseurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8724f0761b5d7e5d361742734901990136a7a98c1b2f541b4fadb69c31a92d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861299"
---
# <a name="implementing-a-client-side-proxy-ui-automation-provider"></a>Implémentation d’un fournisseur UI Automation Client-Side (proxy)

Microsoft UI Automation fournit un ensemble de proxies pour la plupart des contrôles standard, tels que ceux utilisés dans les applications Microsoft Win32, Windows Forms et Windows Presentation Foundation (WPF). Toutefois, de nombreux contrôles personnalisés et contrôles tiers n’implémentent pas les fournisseurs UI Automation natifs. Pour être accessibles aux applications clientes UI Automation, ces contrôles doivent être fournis avec les fournisseurs côté client, également appelés *fournisseurs proxy* *ou* proxys.

Cette rubrique explique comment écrire un fournisseur proxy pour un contrôle non pris en charge et l’ajouter à la liste des proxies utilisés par les applications clientes. Il contient les rubriques suivantes :

-   [Qu’est-ce qu’un proxy ?](#what-is-a-proxy)
-   [Qu’est-ce qu’une fabrique de proxy ?](#what-is-a-proxy-factory)
-   [Mappage de la fabrique proxy](#proxy-factory-mapping)
-   [Gestion des proxies par défaut](#managing-default-proxies)
-   [Rubriques connexes](#related-topics)

Pour obtenir des exemples de code qui montrent comment implémenter des fournisseurs de proxy, consultez [les rubriques de procédures pour les fournisseurs UI Automation](uiauto-howto-topics-for-uiautomation-providers.md).

## <a name="what-is-a-proxy"></a>Qu’est-ce qu’un proxy ?

Un fournisseur côté client, ou proxy, est un objet qui implémente l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) pour le compte d’un contrôle qui n’a pas d’implémentation **IRawElementProviderSimple** propre. Sans proxy, ce type de contrôle est largement opaque pour l’Automation d’interface utilisateur, qui peut fournir uniquement les informations de base disponibles à partir du handle de fenêtre (**HWND**), telles que l’emplacement du contrôle.

## <a name="what-is-a-proxy-factory"></a>Qu’est-ce qu’une fabrique de proxy ?

Chaque proxy requiert une *fabrique de proxy* correspondante, qui est un objet qui expose l’interface [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) . UI Automation gère une table interne d' *entrées de fabrique proxy*, chacune contenant une référence à la fabrique de proxy pour chaque proxy et un ensemble de conditions. Quand UI Automation rencontre un contrôle qui n’a pas d’implémentation [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) native, il recherche une entrée de fabrique proxy dont les conditions indiquent qu’il prend en charge le contrôle. UI Automation effectue des recherches dans la table à partir du début et, lorsqu’il trouve une entrée correspondante, UI Automation appelle la méthode [**IUIAutomationProxyFactory :: CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) de la fabrique. Si le proxy correspondant est correctement créé, UI Automation arrête la recherche et utilise l’objet proxy nouvellement créé. dans le cas contraire, UI Automation continue la recherche.

Une application cliente crée une instance d’une entrée de fabrique proxy à l’aide de la méthode [**IUIAutomation :: CreateProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) , qui retourne un pointeur d’interface [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) . Les clients utilisent des méthodes exposées par **IUIAutomationProxyFactoryEntry** pour spécifier l’ensemble de conditions que la fabrique de proxy utilise pour créer le proxy.

Quand il appelle [**IUIAutomationProxyFactory :: CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider), UI Automation transmet les paramètres que l’objet de fabrique proxy peut utiliser pour déterminer si le proxy prend correctement en charge le contrôle personnalisé. Si c’est le cas, la fabrique de proxy crée une instance du proxy et retourne le pointeur d’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) ; Sinon, elle retourne un pointeur **null** .

## <a name="proxy-factory-mapping"></a>Mappage de la fabrique proxy

Par défaut, UI Automation effectue une recherche dans la table de fabrique de proxy dans l’ordre suivant.



| Commande | Proxy                        | Description                                                                      |
|-------|------------------------------|----------------------------------------------------------------------------------|
| 1     | Microsoft : proxy sans contrôle | Pour Windows avec le nom de classe exact ou le nom de la classe de base « ComboBoxEx32 ».         |
| 2     | Microsoft : proxy sans contrôle | Pour Windows avec le nom de classe exact ou le nom de la classe de base « WorkerW ».              |
| 3     | Microsoft : proxy sans contrôle | Pour Windows avec le nom de classe exact ou le nom de la classe de base « SHELLDLL \_ DefView ».    |
| 4     | Microsoft : conteneur proxy   | Pour Windows avec le nom de classe ou le nom de classe de base exact « \# 32770 ».              |
| 5     | Microsoft : conteneur proxy   | Pour Windows avec un nom de classe ou un nom de classe de base contenant « AfxControlBar ».     |
| 6     | Microsoft : proxy TreeView    | Pour Windows avec un nom de classe ou un nom de classe de base contenant « SysTreeView32 ».     |
| 7     | Microsoft : proxy ListView    | Pour Windows avec un nom de classe ou un nom de classe de base contenant « SysListView32 » (1). |
| 8     | Microsoft : proxy ListView    | Pour Windows avec un nom de classe ou un nom de classe de base contenant « SysListView32 » (2). |
| 9     | Microsoft : proxy MSAA        | Pour n’importe quelle fenêtre.                                                                  |



 

Les proxies 7 et 8 sont des entrées en double pour le contrôle SysListView32. Sans modification, le proxy 7 est toujours utilisé pour le contrôle SysListView32 et proxy 8 n’est jamais utilisé. Proxy 8 est utilisé uniquement pour les éléments de liste visibles, et est généralement utilisé par les applications clientes qui fonctionnent uniquement avec les éléments visibles, ou qui ont des exigences de performances strictes. Ces clients peuvent supprimer le proxy 7.

Proxy 9, le Active Accessibility Microsoft pour le proxy UI Automation, doit toujours être la dernière entrée de la table. Cela permet à Microsoft Active Accessibility la fonctionnalité de secours pour les contrôles qui implémentent Microsoft Active Accessibility, mais pas UI Automation.

Lorsque vous modifiez des entrées dans la table de fabrique de proxy, vous devez évaluer avec soin la nouvelle position des entrées. Nous vous recommandons de placer les entrées de proxys personnalisés après les proxys de conteneur et de non-contrôle, mais avant le Active Accessibility Microsoft pour le proxy UI Automation. En outre, bien qu’il soit possible d’avoir du code dans l’appel à [**CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) pour déterminer s’il doit prendre en charge un handle de fenêtre (**HWND**) donné, il est plus efficace de laisser UI Automation sélectionner le proxy en fonction du nom de la classe, et conserver le code conditionnel dans la méthode **CreateProvider** au minimum.

UI Automation gère une table de fabrique de proxy distincte pour chaque client. Lorsqu’un client modifie sa table proxy, les modifications affectent uniquement le client lui-même. les autres clients ne sont pas affectés.

## <a name="managing-default-proxies"></a>Gestion des proxies par défaut

Lorsqu’une application cliente crée l’objet [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) , la table de fabrique proxy contient initialement des entrées uniquement pour les fournisseurs de proxy par défaut pour les contrôles standard. À l’aide de l’interface [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) , les clients peuvent ajouter de nouvelles entrées, supprimer des entrées indésirables, modifier l’ordre des entrées, et ainsi de suite. Un client peut récupérer un pointeur d’interface **IUIAutomationProxyFactoryMapping** en appelant la méthode [**IUIAutomation ::P roxyfactorymapping**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) .

La table des proxies disponibles contient une interface [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) pour chaque proxy. Chaque **IUIAutomationProxyFactoryEntry** spécifie le [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) et la classe de contrôle que le proxy sert, et définit la manière dont les événements doivent être gérés.

La table des proxies est représentée par une interface [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) , qui peut être obtenue à partir de la propriété [**IUIAutomation ::P roxyfactorymapping**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) . Une application peut utiliser des méthodes **IUIAutomationProxyFactoryMapping** pour ajouter et supprimer des proxies. Pour créer une nouvelle entrée à ajouter à cette table, utilisez [**IUIAutomation :: CreateProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) pour obtenir l’interface, puis utilisez les méthodes [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) pour définir la classe de contrôle applicable et le comportement du proxy.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment créer un fournisseur UI Automation Client-Side (proxy)](uiauto-howto-create-clientside-provider.md)
</dt> <dt>

[Guide du programmeur du fournisseur UI Automation](uiauto-providerportal.md)
</dt> </dl>

 

 