---
title: Active Accessibility et UI Automation
description: Microsoft Active Accessibility est conçu pour être utilisé avec Windows XP et les systèmes d’exploitation antérieurs.
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2483f4f6679926ef2f87c380d4ac0febcc88652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510638"
---
# <a name="active-accessibility-and-ui-automation"></a>Active Accessibility et UI Automation

Microsoft Active Accessibility est conçu pour être utilisé avec Windows XP et les systèmes d’exploitation antérieurs. Les développeurs de contrôles personnalisés et d’applications clientes de technologie accessibles pour Windows XP et Windows Vista doivent envisager d’utiliser Microsoft [UI Automation](entry-uiauto-win32.md) à la place.

Microsoft UI Automation est un système complet qui fournit des informations plus précises sur l’interface utilisateur et donne à l’utilisateur davantage de capacité d’interagir avec les contrôles. En particulier, il fournit une prise en charge beaucoup plus étendue du texte.

Un ensemble d’objets proxy assure la prise en charge d’UI Automation pour les contrôles Microsoft Win32 et Windows Forms standard. Une prise en charge plus riche est disponible pour les contrôles spécifiquement écrits avec UI Automation à l’esprit, y compris les éléments natifs Windows Presentation Foundation (WPF), qui ne prennent pas directement en charge les Active Accessibility Microsoft. Les contrôles personnalisés qui prennent en charge l’Automation d’interface utilisateur peuvent être écrits en code managé ou non managé.

Les clients Microsoft Active Accessibility disposent d’un accès limité, via une couche de pontage, aux éléments d’interface utilisateur qui prennent en charge uniquement UI Automation. Pour plus d’informations, consultez [l’annexe G : Active Accessibility Bridge to UI Automation](appendix-g--active-accessibility-bridge-to-ui-automation.md).

Pour plus d’informations sur les similitudes et les différences entre Microsoft Active Accessibility et UI Automation, consultez [comparaison entre microsoft Active Accessibility et UI Automation](microsoft-active-accessibility-and-ui-automation-compared.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Prise en main](getting-started.md)
</dt> <dt>

[UI Automation](entry-uiauto-win32.md)
</dt> </dl>

 

 




