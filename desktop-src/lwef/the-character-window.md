---
title: Fenêtre de caractères
description: Fenêtre de caractères
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a386dc769e2b5fe7313b768d1b2debfe4a1131
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383356"
---
# <a name="the-character-window"></a>Fenêtre de caractères

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Microsoft Agent affiche les caractères animés dans leurs propres fenêtres qui apparaissent toujours en haut de l’ordre de plan de la fenêtre (c’est-à-dire toujours visible). Un utilisateur peut déplacer la fenêtre d’un caractère en faisant glisser le caractère avec le bouton gauche de la souris. L’image de caractère se déplace avec le pointeur. En outre, une application peut déplacer un caractère à l’aide de la méthode [**MoveTo**](moveto-method.md) .

Quand l’utilisateur clique avec le bouton droit sur un caractère, un menu contextuel s’affiche avec les commandes suivantes :

Ouvrir la \| fenêtre fermer les commandes <span class="underline">V</span>OCAL

IDE <span class="underline">H</span>

----------------------------…

Commande\*


*OtherHostingApplicationCaption\*\**

\*Les commandes répertoriées sont basées sur le client d’entrée-actif. Pour plus d’informations sur la définition des commandes qui s’affichent dans le menu contextuel, consultez la vue d’ensemble de l’interface de programmation Microsoft Agent.

\*\*Les entrées répertoriées sont toutes les autres applications qui hébergent actuellement le caractère. Pour plus d’informations sur la définition de cette entrée, consultez la vue d’ensemble de l’interface de programmation Microsoft Agent.

La \| commande ouvrir fermer les commandes vocales de la fenêtre contrôle l’affichage de la fenêtre commandes du caractère actif actuel. Si les services de reconnaissance vocale sont désactivés, cette commande est désactivée. Si les services de reconnaissance vocale ne sont pas installés, cette commande n’apparaît pas.

La commande masquer masque le caractère. L’animation assignée à l’état de **masquage** du caractère lit et masque le caractère. La lettre « H » dans Hide est la clé d’accès de la commande (mnémonique).

Les commandes de la ou des applications qui hébergent actuellement le caractère suivent la commande masquer, précédée d’un séparateur. Les noms des autres applications qui utilisent le caractère apparaissent, également précédés d’un séparateur.

 

 




