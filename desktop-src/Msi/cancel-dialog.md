---
description: Une boîte de dialogue annuler confirme que l’utilisateur souhaite mettre fin à l’installation. Il s’agit d’une boîte de dialogue modale.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Boîte de dialogue annuler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2f0ba12c442b8b0f4445077497c26649b79714d1a1d77af7b2a82e6c1a3f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105389"
---
# <a name="cancel-dialog"></a>Boîte de dialogue annuler

Une boîte de dialogue **Annuler** confirme que l’utilisateur souhaite mettre fin à l’installation. Il s’agit d’une boîte de dialogue modale.

Ce type de boîte de dialogue contient généralement un [contrôle de texte](text-control.md) et deux [boutons](pushbutton-control.md)de commande. Les deux boutons permettent à l’utilisateur de choisir de retourner à la dernière boîte de dialogue ou de confirmer l’arrêt de l’installation.

Le ControlEvent, [EndDialog](enddialog-controlevent.md) est lié à ces deux boutons dans la [table ControlEvent,](controlevent-table.md). Le paramètre de *retour* de l’ControlEvent, EndDialog est lié à l’un des boutons et entraîne l’arrêt de la boîte de dialogue **Annuler** et le focus pour revenir à la boîte de dialogue précédente. Le paramètre de *sortie* est lié à l’autre bouton et fait en sorte que l’interface utilisateur retourne le contrôle au programme d’installation avec le code approprié indiquant que l’utilisateur souhaite quitter. Le programme d’installation s’arrête ensuite et affiche la [boîte de dialogue UserExit](userexit-dialog.md).

 

 



