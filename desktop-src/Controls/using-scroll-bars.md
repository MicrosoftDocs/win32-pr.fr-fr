---
title: Utilisation des barres de défilement
description: Cette section contient des rubriques qui montrent comment créer des barres de défilement.
ms.assetid: 45ffb56f-f567-40d7-8172-e64e26744ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d602426bd5f716a380d43104046f330d3240d516
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115249"
---
# <a name="using-scroll-bars"></a>Utilisation des barres de défilement

Cette section contient des rubriques qui montrent comment créer des barres de défilement.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comment créer des barres de défilement](create-scroll-bars.md)<br/>                                                                     | Lors de la création d’une fenêtre superposée, indépendante ou enfant, vous pouvez ajouter des barres de défilement standard à l’aide de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) et en spécifiant WS \_ HSCROLL, WS \_ VSCROLL ou les deux styles. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [Comment faire défiler le texte](scroll-text-in-scroll-bars.md)<br/>                                                                    | Cette section décrit les modifications que vous pouvez apporter à la procédure de fenêtre principale d’une application pour permettre à un utilisateur de faire défiler le texte. L’exemple de cette section crée et affiche un tableau de chaînes de texte, puis traite les messages de la barre de défilement [**WM \_ HSCROLL**](wm-hscroll.md) et [**WM \_ VSCROLL**](wm-vscroll.md) pour permettre à l’utilisateur de faire défiler le texte à la fois verticalement et horizontalement. <br/>                                                                                                                                                                                                                                                                 |
| [Comment faire défiler une bitmap](scroll-a-bitmap-in-scroll-bars.md)<br/>                                                            | Cette section décrit les modifications que vous pouvez apporter à la procédure de fenêtre principale d’une application pour permettre à l’utilisateur de faire défiler une bitmap. <br/> L’exemple comprend un élément de menu qui copie le contenu de l’écran dans une image bitmap et affiche l’image bitmap dans la zone cliente. L’exemple traite également les messages [**WM \_ HSCROLL**](wm-hscroll.md) et [**WM \_ VSCROLL**](wm-vscroll.md) qui sont générés par les barres de défilement de sorte que l’utilisateur puisse faire défiler le bitmap horizontalement et verticalement. Contrairement à l’exemple de texte défilé, l’exemple de bitmap utilise la fonction [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) pour dessiner la partie non valide de la zone cliente. <br/> |
| [Comment créer une interface clavier pour les barres de défilement standard](create-a-keyboard-interface-for-standard-scroll-bars.md)<br/> | Bien qu’un contrôle de barre de défilement fournisse une interface clavier intégrée, aucune barre de défilement standard ne le fait. Pour implémenter une interface clavier pour une barre de défilement standard, une procédure de fenêtre doit traiter le message KeyOut [**WM \_**](/windows/desktop/inputdev/wm-keydown) et examiner le code de la touche virtuelle spécifié par le paramètre *wParam* . Si le code de la touche virtuelle correspond à une touche de direction, la procédure de fenêtre s’envoie un message [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) avec le mot de poids faible du paramètre *wParam* défini sur le code de requête de la barre de défilement appropriée. <br/>                                              |



 

 

