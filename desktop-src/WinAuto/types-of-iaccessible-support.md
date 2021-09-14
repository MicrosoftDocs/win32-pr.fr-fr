---
title: Types de prise en charge de IAccessible
description: Types de prise en charge de IAccessible
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb2cb3d25e4cf95cc1ad790c77ffe66e02efda2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010593"
---
# <a name="types-of-iaccessible-support"></a>Types de prise en charge de IAccessible

Les serveurs Microsoft Active Accessibility ont deux types de prise en charge de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : natif et proxy. Les éléments d’interface utilisateur utilisés dans une application déterminent le type de prise en charge approprié. De nombreux serveurs écrits aujourd’hui tirent pleinement parti des proxies et implémentent uniquement **IAccessible** pour les contrôles qui ne sont pas proxyés **par des Oleacc.dll** , tels que les contrôles ou les contrôles sans fenêtre avec un nom de classe de fenêtre personnalisé.

## <a name="in-this-section"></a>Dans cette section

-   [Implémentation de Active Accessibility Native](native-active-accessibility-implementation.md)
-   [Proxys IAccessible](iaccessible-proxies.md)

 

 




