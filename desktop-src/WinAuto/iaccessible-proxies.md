---
title: Proxys IAccessible
description: Les proxys IAccessible fournissent des informations d’accessibilité par défaut pour les éléments d’interface utilisateur standard, les menus utilisateur et les contrôles communs de COMCTL et COMCTL32.
ms.assetid: 236c2064-de44-4021-8825-f1519312dbfc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53dcb4cae8980e4003d9915c6783e4ddb043a8c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191707"
---
# <a name="iaccessible-proxies"></a>Proxys IAccessible

Les proxys [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fournissent des informations d’accessibilité par défaut pour les éléments d’interface utilisateur standard : les contrôles utilisateur, les menus utilisateur et les contrôles communs de COMCTL et Comctl32. Cette prise en charge par défaut est exposée par le biais d’objets **IAccessible** créés par Oleacc.dll et fournit la prise en charge de Microsoft Active Accessibility sans travail supplémentaire de développement serveur. Le serveur peut ensuite utiliser l' [API d’annotation dynamique](dynamic-annotation-api.md) pour modifier la plupart des informations exposées par Oleacc.dll, mais il n’a pas de contrôle total.

## <a name="creating-a-proxy"></a>Création d’un proxy

Pour déterminer si un élément d’interface utilisateur prend en charge l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en mode natif, Oleacc.dll lui envoie un message [**WM \_**](wm-getobject.md) . Une valeur de retour différente de zéro signifie que l’élément prend en charge en mode natif Microsoft Active Accessibility et fournit sa propre prise en charge de **IAccessible** . Toutefois, si la valeur de retour est égale à zéro, Oleacc.dll fournit un objet proxy pour l’élément d’interface utilisateur et tente de retourner des informations significatives en son nom. Pour plus d’informations sur **WM \_ GetObject**, consultez fonctionnement de l’utilisation de [la fonction \_ GetObject](how-wm-getobject-works.md).

## <a name="what-information-is-exposed"></a>Informations exposées

Oleacc.dll utilise le nom de classe de l’élément d’interface utilisateur Windows pour déterminer les informations qui doivent être exposées pour chacune de ses propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et comment collecter ces informations. Par exemple, Oleacc.dll appelle la fonction [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) pour récupérer la propriété [**Name**](name-property.md) d’un bouton de commande standard, mais appelle cette même fonction pour récupérer la propriété [**value**](value-property.md) d’un contrôle d’édition standard. En effet, Oleacc.dll mappe chaque méthode **IAccessible** à un appel de fonction ou de message spécifique à Microsoft Win32 ou spécifique au contrôle. En utilisant cette casse spéciale basée sur le nom de la classe, il peut retourner des informations significatives via les proxys **IAccessible** sans la prise en charge de Microsoft Active Accessibility sur le serveur.

Les applications générées avec des éléments d’interface utilisateur standard bénéficient en général de la prise en charge complète de Microsoft Active Accessibility sans travail supplémentaire de développement. Les exceptions à cette règle sont des contrôles qui ont été sous-classés, qui ne stockent pas leurs propres chaînes (absence du style **HASSTRINGS** ) ou qui sont owner-drawn. Dans ces cas, Oleacc.dll ne peut pas collecter les informations dont il a besoin car les informations sont stockées en dehors du contrôle. Toutefois, dans la plupart de ces scénarios, les solutions de contournement établies ou l’utilisation de l’annotation dynamique permettent au serveur de coopérer avec les proxies fournis par Oleacc.dll.

## <a name="generic-proxy-objects"></a>Objets proxy génériques

Si Oleacc.dll ne reconnaît pas le nom de classe de l’élément d’interface utilisateur, il crée un proxy générique qui expose le plus d’informations possible. Au plus, cela comprend le rectangle englobant de l’objet, l’objet parent, le nom (de [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)) et tous les enfants de la hiérarchie de la fenêtre.

 

 