---
description: Une boîte de dialogue d’erreur est une boîte de dialogue modale qui affiche un message d’erreur. Il peut y avoir plusieurs boîtes de dialogue d’erreur dans chaque installation.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Boîte de dialogue d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a153f5e6ee38235f830937d794a9ca9b81314583
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091353"
---
# <a name="error-dialog"></a>Boîte de dialogue d’erreur

Une boîte de dialogue d’erreur est une boîte de dialogue modale qui affiche un message d’erreur. Il peut y avoir plusieurs boîtes de dialogue d’erreur dans chaque installation.

Une propriété ErrorDialog doit être définie pour spécifier la boîte de dialogue à utiliser. Si cette propriété n’est pas définie ou ne pointe pas vers une boîte de dialogue d’erreur valide, les messages d’erreur ne s’affichent pas. Dans ce cas, l’erreur est enregistrée uniquement avec un avertissement concernant la boîte de dialogue manquante.

Le bit de style de boîte de [dialogue d’erreur](error-dialog-style-bit.md) doit être défini pour une boîte de dialogue d’erreur. La boîte de dialogue doit avoir un [contrôle de texte](text-control.md) nommé ErrorText. L’enregistrement de la boîte de dialogue d’erreur dans la [table de boîte de dialogue](dialog-table.md) doit avoir le contrôle ErrorText entré dans le \_ premier champ Control.

La boîte de dialogue doit contenir sept [PUSHBUTTON](pushbutton-control.md). Tous ces boutons spécifient le ControlEvent, [EndDialog](enddialog-controlevent.md) dans la [table ControlEvent,](controlevent-table.md). Chaque bouton spécifie l’un des attributs suivants : **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.

> [!Note]  
> Le focus de ces contrôles ne doit pas être lié par le biais de l’utilisation de la \_ colonne Control Next dans la [table Control](control-table.md).

 

Ces boutons doivent être placés à peu près à la même position dans la boîte de dialogue, car lorsqu’ils sont créés, seul un sous-ensemble de ces sept boutons est créé, en fonction du message. La coordonnée X des boutons est modifiée afin que les boutons affichés soient espacés uniformément. La coordonnée Y, la hauteur et la largeur des boutons sont inchangées. Étant donné que les boutons sont disposés horizontalement, aucun autre contrôle ne peut être placé dans la même zone horizontale de la boîte de dialogue.

Pour une boîte de dialogue d’erreur, les \_ champs Control default et Control \_ Cancel de la [table Dialog](dialog-table.md) sont ignorés. Le \_ premier champ contrôle d’une boîte de dialogue d’erreur doit spécifier le contrôle ErrorText.

si un [contrôle Icon](icon-control.md) nommé ErrorIcon est inclus dans cette boîte de dialogue, les icônes de Windows standard suivantes s’affichent :

-   \_Erreur IDI en réponse aux messages imtFatalExit.
-   IDI \_ avertissement en réponse aux messages imtWarning et.
-   IDI \_ les informations en réponse aux messages imtOutOfDiskSpace.

le contrôle ErrorIcon doit être créé avec l' [attribut de contrôle FixedSize](fixedsize-control-attribute.md) défini pour éviter le dimensionnement incorrect des icônes de Windows standard.

 

 



