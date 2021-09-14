---
title: Prise en charge de IAccessible Native
description: Oleacc.dll implémente IAccIdentity pour le compte du \_ client objid \ 160 ; les pointeurs d’interface IAccessible et leurs enfants d’éléments simples immédiats.
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606261a642f57c85f3f23a80257b7cdc498b927b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010676"
---
# <a name="native-iaccessible-support"></a>Prise en charge de IAccessible Native

Oleacc.dll implémente [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) pour le compte des pointeurs d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [**\_ client objid**](object-identifiers.md) et leurs enfants d’éléments simples immédiats. Un pointeur d’interface **IAccessible** **\_ client objid** est retourné lorsque le client [**WM \_ GETOBJECT**](wm-getobject.md) with *lParam*  =  **\_ objID** est envoyé à un **HWND**, qui représente la zone cliente de la fenêtre ou le contrôle dans son ensemble. Le parent d’un tel pointeur d’interface **IAccessible** aura généralement un rôle de [**\_ \_ fenêtre système de rôle**](object-roles.md) et est l’objet **IAccessible** retourné lorsque la fenêtre **WM \_ GETOBJECT** with *lParam*  =  [**objID \_**](object-identifiers.md) est envoyée à un HWND.

Ces pointeurs d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) se produisent généralement quand un proxy Oleacc.dll est sous-classé, ou lorsqu’un simple contrôle personnalisé (tel qu’un conteneur **IAccessible** plus un niveau d’éléments enfants simples) fournit une implémentation **IAccessible** native.

Les implémentations de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) natives plus complexes, telles que l’emplacement où une hiérarchie d’objets **IAccessible** existe ou l’emplacement où les ID d’objet personnalisés sont utilisés, doivent implémenter [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) eux-mêmes.

 

 




