---
title: interopérabilité 32 bits et 64 bits
description: Les applications de technologie d’assistance doivent communiquer à travers les limites de processus pour obtenir des informations sur l’interface utilisateur auprès des serveurs Microsoft Active Accessibility et des fournisseurs UI Automation de Microsoft.
ms.assetid: 8b46daed-4fd9-430c-bb4d-24be9c8015b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1c056c9fe2792734e9369fa311e69528ce226f7edf15b82440b63c12c52de66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327988"
---
# <a name="32-bit-and-64-bit-interoperability"></a>interopérabilité 32 bits et 64 bits

Les applications de technologie d’assistance doivent communiquer à travers les limites de processus pour obtenir des informations sur l’interface utilisateur auprès des serveurs Microsoft Active Accessibility et des fournisseurs UI Automation de Microsoft. cette rubrique décrit les principaux problèmes de communication entre processus que vous devez garder à l’esprit lors du développement d’applications d’accessibilité Windows.

lorsque les applications utilisent l’API d’automatisation Windows, les composants d’exécution de Microsoft Active Accessibility et UI automation gèrent automatiquement tous les problèmes et les complexités liés à l’exécution des communications interprocessus (IPC), y compris les problèmes d’interopérabilité impliqués lorsqu’un processus est 32 bits et l’autre à 64 bits. Microsoft reconnaît qu’il est possible qu’une application de technologie d’assistance doive utiliser une certaine forme d’IPC au lieu de l’API d’automatisation d’Windows pour communiquer avec un fournisseur Microsoft Active Accessibility server ou UI automation. dans ces cas, Microsoft vous recommande d’utiliser des messages DCOM ou Windows (ceux dont la valeur est inférieure à celle de l' **\_ utilisateur WM**) pour communiquer avec d’autres processus. à l’instar de l’API Windows Automation, les messages DCOM et Windows gèrent automatiquement tous les problèmes IPC, y compris l’interopérabilité 32 bits sur 64 bits.

lorsque l’API Windows Automation, DCOM et Windows messages ne sont pas une option, gardez les points suivants à l’esprit lors de l’implémentation de la méthode IPC choisie :

-   Mémoire partagée : lors de l’utilisation de la mémoire partagée, sachez qu’une structure dans un processus 32 bits peut avoir une taille et une disposition différentes de la même structure dans un processus 64 bits. Cela est particulièrement vrai pour les structures qui contiennent des pointeurs ou des handles.
-   troncation de pointeur : bien qu’une application 32 bits puisse utiliser le type de données **LONGLONG** pour stocker une valeur 64 bits, il existe des cas où il n’existe aucun élément API Windows qui permet à l’application 32 bits de recevoir une valeur 64 bits d’un processus 64 bits ou d’envoyer une valeur 64 bits à un processus 64 bits. Par exemple, les fonctions [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) et [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) tronquent toutes les valeurs de pointeur, laissant l’application 32 bits avec une valeur inutile.
-   Handles : comme les handles Kernel32 et User32 ne sont significatifs que de 32 bits dans les processus 32 bits et 64 bits, ils peuvent être transférés entre les processus sans problème. toutefois, certains éléments que Windows définit en tant que handles sont simplement des pointeurs encapsulés (par exemple, **HTREEITEM**). Ces « handles » seront tronqués s’ils sont passés d’un processus 64 bits à un processus 32 bits.
-   [WinEvent](winevents-infrastructure.md) Fonctions de raccordement : pour inscrire une fonction de raccordement dans le contexte avec un processus serveur 32 bits, la fonction de raccordement doit résider dans une DLL 32 bits. De même, pour inscrire une fonction de raccordement dans le contexte avec un processus serveur 64 bits, la fonction de raccordement doit résider dans une DLL 64 bits. Si une application de technologie d’assistance tente d’enregistrer une fonction de raccordement dans le contexte avec un serveur qui a une profondeur de bits différente, les événements sont toujours remis à la fonction de raccordement, mais ils sont remis hors contexte. Pour plus d’informations, consultez WinEvents et [fonctions de raccordement en contexte et hors](in-context-and-out-of-context-hook-functions.md)contexte.

Pour plus d’informations sur l’interopérabilité 32 bits et 64 bits, consultez [interopérabilité des processus](/windows/desktop/WinProg64/process-interoperability).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Vue d’ensemble de l’API Automation](windows-automation-api-overview.md)
</dt> </dl>

 

 