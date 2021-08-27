---
description: Les fenêtres État, composition et candidats constituent l’interface utilisateur de l’IME.
ms.assetid: a0e52743-f9be-4934-9469-71d3cb5a768a
title: Windows de l’État, de la composition et des candidats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f5c385c14cd265630de77352e12e4c63bce806837462f3c9ab3c204940e66c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130109"
---
# <a name="status-composition-and-candidates-windows"></a>Windows de l’État, de la composition et des candidats

Les fenêtres État, composition et candidats constituent l’interface utilisateur de l’IME. La fenêtre d’État indique que l’IME est ouvert et fournit à l’utilisateur la possibilité de définir les modes de conversion. La fenêtre composition s’affiche lorsque l’utilisateur entre du texte et, selon le mode de conversion, affiche le texte tel qu’il est entré ou affiche le texte converti. La fenêtre candidats s’affiche conjointement avec la fenêtre de composition. Elle contient une liste de « candidats » (caractères de remplacement) pour le ou les caractères sélectionnés dans la fenêtre de composition. L’utilisateur peut faire défiler la liste des candidats et sélectionner les caractères souhaités, puis revenir à la fenêtre de composition. L’utilisateur peut composer le texte souhaité de cette façon jusqu’à ce que la chaîne de composition soit finalisée et que la fenêtre soit fermée.

L’IME envoie les caractères composés à l’application prenant en charge l’IME sous la forme de messages de résultat/GCS de l’IME [**WM \_ \_**](wm-ime-char.md) ou de la [**\_ \_ composition IME WM**](wm-ime-composition.md) \_ . Si l’application ne traite pas ces messages, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) les traduit en un ou plusieurs messages [**WM \_ char**](../inputdev/wm-char.md) .

Par défaut, le système d’exploitation crée et gère automatiquement les fenêtres d’État, de composition et de candidat pour les exigences d’entrée de texte. Pour de nombreuses applications, ce traitement par défaut est suffisant. Ces applications reposent entièrement sur le système d’exploitation pour la prise en charge de l’IME et sont dites « non compatibles avec l’IME », car elles n’ont pas conscience des nombreuses tâches que le système d’exploitation effectue pour gérer les fenêtres IME.

Une application compatible avec l’IME, en revanche, participe à la création et à la gestion des fenêtres IME. De telles applications contrôlent l’opération, la position et l’apparence des fenêtres par défaut en envoyant des messages à ces fenêtres et en interceptant et en traitant les messages à partir des fenêtres. Dans certains cas, les applications créent leurs propres fenêtres IME et fournissent un traitement complet pour leur état personnalisé, la composition et les fenêtres de candidats.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du gestionnaire de méthode d’entrée](about-input-method-manager.md)
</dt> </dl>

 

 
