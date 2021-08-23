---
description: Le ControlEvent, de la transaction notifie le programme d’installation d’exécuter une action personnalisée. Cet événement peut être publié par un contrôle de bouton de commande, un contrôle de case à cocher ou un contrôle SelectionTree. Cet événement doit être créé dans la table ControlEvent,.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: Action ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc4133c9b9fb0b312423952ee72d1e9e38defc2713345e1a7ed106fb141f0a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692619"
---
# <a name="doaction-controlevent"></a>Action ControlEvent,

Le ControlEvent, de la transaction notifie le programme d’installation d’exécuter une action personnalisée. Cet événement peut être publié par un contrôle de [bouton](pushbutton-control.md) de commande, un contrôle de [case à cocher](checkbox-control.md) ou un contrôle [SelectionTree](selectiontree-control.md) . Cet événement doit être créé dans la table [ControlEvent,](controlevent-table.md) .

Notez que les actions personnalisées lancées par une action ControlEvent, peuvent envoyer un message avec la [**méthode de message**](session-message.md), mais ne peuvent pas envoyer de message avec [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage). sur les systèmes antérieurs à Windows Server 2003, les actions personnalisées lancées par une action controlevent, ne peuvent pas envoyer de messages avec **MsiProcessMessage** ou la **méthode de Message**. pour plus d’informations, consultez [envoi de Messages à Windows Installer à l’aide de MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez niveaux de l' [interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Chaîne, nom de l’action personnalisée à exécuter.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue est lié à cet événement dans la table [ControlEvent,](controlevent-table.md) pour appeler une action personnalisée.

 

 



