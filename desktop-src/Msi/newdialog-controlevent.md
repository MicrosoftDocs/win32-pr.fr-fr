---
description: Cet événement notifie le programme d’installation de faire passer une boîte de dialogue modale à une autre boîte de dialogue. Le programme d’installation supprime la boîte de dialogue présente et en crée une avec le nom indiqué dans l’argument.
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: NewDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439c459bc5bfe061cc7f888d9c0a3374afa9098b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114558"
---
# <a name="newdialog-controlevent"></a>NewDialog ControlEvent,

Cet événement notifie le programme d’installation de faire passer une boîte de dialogue modale à une autre boîte de dialogue. Le programme d’installation supprime la boîte de dialogue présente et en crée une avec le nom indiqué dans l’argument.

Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Chaîne qui est le nom de la nouvelle boîte de dialogue.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) dans une boîte de dialogue modale est lié à cet événement dans la table [ControlEvent,](controlevent-table.md) pour signaler une transition vers la boîte de dialogue suivante ou précédente de la même séquence d’Assistant.

 

 



