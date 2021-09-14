---
title: Génération de WinEvents appropriée
description: Les développeurs de serveurs doivent s’assurer que les WinEvents appropriés sont générés pour tous les éléments d’interface utilisateur, notamment les éléments d’interface utilisateur de fenêtre, les éléments d’interface utilisateur sans fenêtre et les éléments d’interface utilisateur avec des comportements hautement personnalisés.
ms.assetid: 253e0162-20e6-4e89-b563-aae9cf7e53a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6273411115e908303e863a34908e15ef91b19c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291899"
---
# <a name="generating-appropriate-winevents"></a>Génération de WinEvents appropriée

Les développeurs de serveurs doivent s’assurer que les WinEvents appropriés sont générés pour tous les éléments d’interface utilisateur, notamment les éléments d’interface utilisateur de fenêtre, les éléments d’interface utilisateur sans fenêtre et les éléments d’interface utilisateur avec des comportements hautement personnalisés.

L’utilisateur fournit la prise en charge WinEvent par défaut pour les éléments d’interface utilisateur standard basés sur **HWND**. Étant donné que l’utilisateur génère ces événements automatiquement, les serveurs doivent générer des événements uniquement pour les contrôles personnalisés, les éléments sans fenêtre ou les contrôles dont les événements ne sont pas déjà générés par l’utilisateur.

Pour envoyer un événement, les serveurs appellent [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) et transmettent la constante d’événement, un ID d’objet et le **HWND** pour une fenêtre qui peut répondre aux demandes des clients pour plus d’informations. Les événements qui doivent être déclenchés varient en fonction du type d’élément d’interface utilisateur. Il existe des événements généraux qui doivent être envoyés pour tous les contrôles, ainsi que des événements spécifiques qui doivent être envoyés uniquement pour l’élément d’interface utilisateur approprié.

## <a name="general-events"></a>Événements généraux

Les WinEvents générales peuvent être envoyés pour tous les éléments d’interface utilisateur. En voici quelques-uns :

-   [**Événement \_ \_Création d’objet**](event-constants.md) (lors de la création d’un objet)
-   [**Événement \_ \_Destruction d’objet**](event-constants.md) (lorsqu’un objet est détruit)
-   [**Événement \_ OBJET \_ Show**](event-constants.md) (quand un objet est affiché)
-   [**Événement \_ \_Masquer l’objet**](event-constants.md) (quand un objet est masqué)

## <a name="specific-events"></a>Événements spécifiques

Il existe également des WinEvents spécifiques qui peuvent être envoyés pour un type particulier d’élément d’interface utilisateur. Par exemple, utilisez [**la \_ \_ sélection d’objet d’événement**](event-constants.md) pour les contrôles qui permettent à l’utilisateur d’effectuer une sélection, telle qu’une zone de liste.

Pour plus d’informations sur les événements attendus pour un type particulier d’élément d’interface utilisateur, consultez les ressources suivantes :

-   [Annexe A : informations de référence sur les éléments d’interface utilisateur pris en charge](appendix-a--supported-user-interface-elements-reference.md). Cette annexe contient des informations sur les éléments d’interface utilisateur générés par Microsoft Active Accessibility. La documentation de chaque contrôle contient des informations sur les événements qui peuvent être générés par l’élément d’interface utilisateur.
-   [Constantes d’événement](event-constants.md). Cette rubrique contient des informations sur les événements générés par le système d’exploitation et les applications serveur.
-   Observateur d’événements accessible (AccEvent.exe). Cet outil affiche les événements que l’utilisateur envoie pour un élément d’interface utilisateur particulier. Vous pouvez utiliser cet outil pour savoir quels événements vous pouvez attendre pour un élément d’interface utilisateur. Pour plus d’informations, consultez [Observateur d’événements accessible](accessible-event-watcher.md).

 

 




