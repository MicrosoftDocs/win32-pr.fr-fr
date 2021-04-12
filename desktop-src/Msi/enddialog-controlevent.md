---
description: Cet événement notifie le programme d’installation de la suppression d’une boîte de dialogue modale. Dans tous les cas, le programme d’installation supprime la boîte de dialogue présente.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: ControlEvent, EndDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08449bffe29093e32066e92e1b8fc739efa02d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203212"
---
# <a name="enddialog-controlevent"></a>ControlEvent, EndDialog

Cet événement notifie le programme d’installation de la suppression d’une boîte de dialogue modale. Dans tous les cas, le programme d’installation supprime la boîte de dialogue présente.

Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

Le tableau suivant répertorie l’action de l’événement résultant de différents arguments entrés dans la [table ControlEvent,](controlevent-table.md).



| Argument | Action par le programme d’installation                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Quitter     | La séquence de l’Assistant est fermée et le contrôle retourne au programme d’installation avec la valeur UserExit. Cet argument ne peut pas être utilisé dans une boîte de dialogue qui est l’enfant d’une autre boîte de dialogue. |
| Recommencer    | La séquence de l’Assistant est fermée et le contrôle retourne au programme d’installation avec la valeur de suspension. Cet argument ne peut pas être utilisé dans une boîte de dialogue qui est l’enfant d’une autre boîte de dialogue.  |
| Ignorer   | La séquence de l’Assistant est fermée et le contrôle retourne au programme d’installation avec la valeur terminée. Cet argument ne peut pas être utilisé dans une boîte de dialogue qui est l’enfant d’une autre boîte de dialogue. |
| Renvoie   | Le contrôle retourne au parent de la boîte de dialogue présente, ou s’il n’existe aucun parent, le contrôle retourne au programme d’installation avec la valeur Success.                                 |



 

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Dans les boîtes de dialogue normales, la colonne argument de la [table ControlEvent,](controlevent-table.md) peut être « Return », « Exit », « Retry » ou « ignore ».

Dans les boîtes de dialogue d’erreur, la colonne argument de la [table ControlEvent,](controlevent-table.md) peut être « ErrorOk », « ErrorCancel », « ErrorAbort », « ErrorRetry », « ErrorIgnore », « ErrorYes » ou « ErrorNo ».

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue modale est lié à cet événement dans la table [ControlEvent,](controlevent-table.md) pour fermer une boîte de dialogue.

 

 



