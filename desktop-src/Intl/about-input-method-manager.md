---
description: L’utilisation de la fonctionnalité IMM dans votre application prenant en charge l’IME évite aux utilisateurs d’avoir à mémoriser toutes les valeurs de caractères possibles.
ms.assetid: 43b3e561-b844-4688-ab3d-d99f92ed140e
title: À propos du gestionnaire de méthode d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b96c64eba5ddfb6966c96d88792fd657f94aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522080"
---
# <a name="about-input-method-manager"></a>À propos du gestionnaire de méthode d’entrée

L’utilisation de la fonctionnalité IMM dans votre application prenant en charge l’IME évite aux utilisateurs d’avoir à mémoriser toutes les valeurs de caractères possibles. Au lieu de cela, il permet à l’IME de surveiller les séquences de touches d’un utilisateur, anticipe les caractères que l’utilisateur peut souhaiter, et présente une liste de caractères candidats à choisir.

> [!Note]  
> Le IMM effectue des opérations similaires à celles de l' [infrastructure de services de texte](../tsf/text-services-framework.md), utilisée par les applications qui communiquent avec les services de texte.

 

Par défaut, le IMM fournit une fenêtre IME par le biais de laquelle l’utilisateur entre des séquences de touches et des vues et sélectionne des candidats. Les applications peuvent utiliser les fonctions et les messages IMM pour créer et gérer leurs propres fenêtres IME, en fournissant une interface personnalisée tout en utilisant les fonctionnalités de conversion de l’IME.

Le IMM est activé uniquement sur les systèmes d’exploitation Windows localisés pour l’Asie de l’est (chinois, japonais, coréen). Sur ces systèmes, l’application appelle [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) avec le \_ DBCSENABLED SM pour déterminer si le IMM est activé.

**Windows 2000 :** La prise en charge complète des IMM est fournie dans toutes les versions localisées de la langue. Toutefois, le IMM est activé uniquement lorsqu’un module linguistique asiatique est installé. Une application compatible avec l’IME peut appeler [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) avec SM \_ IMMENABLED pour déterminer si le IMM est activé.

Cette rubrique contient les sections suivantes.

-   [Listes de candidats](candidate-lists.md)
-   [Chaîne de composition](composition-string.md)
-   [IME HexToUnicode](hextounicode-ime.md)
-   [Touches d’accès rapide](hot-keys.md)
-   [Messages IME](ime-messages.md)
-   [Classe de fenêtre IME](ime-window-class.md)
-   [Contexte d’entrée](input-context.md)
-   [Fenêtres État, composition et candidats](status--composition--and-candidates-windows.md)

 

 
