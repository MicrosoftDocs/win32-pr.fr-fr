---
title: Interface IDispatch et accessibilité
description: L’interface IDispatch a été initialement conçue pour prendre en charge l’automatisation.
ms.assetid: 5a95f002-4fd5-43d3-9b50-7b3f7790300a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641ca3e4cc18b96441aefbbc46231e3f7753a94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228342"
---
# <a name="idispatch-interface-and-accessibility"></a>Interface IDispatch et accessibilité

L’interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) a été initialement conçue pour prendre en charge l’automatisation. Il fournit un mécanisme de liaison tardive pour accéder et récupérer des informations sur les méthodes et les propriétés d’un objet. Auparavant, les développeurs de serveurs devaient implémenter à la fois les interfaces **IDispatch** et [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour leurs objets accessibles. autrement dit, ils devaient fournir une [interface double](dual-interfaces--iaccessible-and-idispatch.md). Avec Microsoft Active Accessibility 2,0, les serveurs peuvent retourner **E \_ NOTIMPL** à partir des méthodes **IDispatch** et Microsoft Active Accessibility implémente l’interface **IAccessible** pour eux.

En plus des méthodes héritées de [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), les développeurs de serveur doivent implémenter les méthodes suivantes dans la définition de classe de chaque objet exposé :

-   [**GetTypeInfoCount**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) retourne le nombre de descriptions de type pour l’objet. Pour les objets qui prennent en charge [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch), le nombre d’informations de type est toujours un.
-   [**GetTypeInfo**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfo) récupère une description de l’interface programmable de l’objet.
-   [**GetIDsOfNames**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) mappe le nom d’une méthode ou d’une propriété à un **DISPID**, qui est ensuite utilisé pour appeler la méthode ou la propriété.
-   [**Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) appelle l’une des méthodes de l’objet, ou obtient ou définit l’une de ses propriétés.

 

 