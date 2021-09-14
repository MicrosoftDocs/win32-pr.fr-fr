---
description: Description de l’utilisation d’Active Accessibility pour exposer des contrôles personnalisés pour le Tablet PC.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Utilisation de Active Accessibility pour exposer des contrôles personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d33d4c2b57a881cfbdc15f14e71e339ed7f9e84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296007"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a>Utilisation de Active Accessibility pour exposer des contrôles personnalisés

Vous pouvez utiliser Microsoft Active Accessibility comme méthode efficace pour rendre les contrôles personnalisés compatibles avec les aides à l’accessibilité. Active Accessibility nécessite que l’application :

-   Créez des objets COM (Component Object Model) qui représentent des contrôles personnalisés individuels ou des groupes de contrôles qui prennent correctement en charge l’interface **IAccessible** . (L’objet peut être créé à la demande lorsqu’il est demandé par un client Active Accessibility.)
-   Appelez [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) lorsque les contrôles sont créés ou détruits, gagnez ou perdez le focus ou modifiez l’État.
-   Gérez le \_ message WM GETOBJECT lorsqu’il est utilisé pour interroger les propriétés de l’objet ou des objets.

Dans le cadre de cette discussion, une fenêtre contenant d’autres objets personnalisés doit également être exposée à Active Accessibility, ce qui permet au client de découvrir et d’accéder aux objets enfants. Pour plus d’informations sur la façon de rendre les contrôles personnalisés compatibles avec les aides à l’accessibilité, consultez [accessibilité](../accessibility/accessibility.md).

 

 
