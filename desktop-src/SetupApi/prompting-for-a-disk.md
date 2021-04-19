---
description: Pour générer une boîte de dialogue qui invite l’utilisateur à insérer le disque suivant ou à spécifier un nouveau chemin d’accès source, appelez SetupPromptForDisk.
ms.assetid: a780e7ab-bd96-43e4-9425-e15a758391f4
title: Demande de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404e88611ec21b7a29d69ab306dc0e7c4e1b98e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521231"
---
# <a name="prompting-for-a-disk"></a>Demande de disque

Pour générer une boîte de dialogue qui invite l’utilisateur à insérer le disque suivant ou à spécifier un nouveau chemin d’accès source, appelez [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska). Cette fonction est utilisée par les routines de rappel pour générer une interface utilisateur lorsque la notification, [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md), est envoyée à la routine de rappel.

La boîte de dialogue générée par [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) donne à l’utilisateur la possibilité d’insérer un disque, de spécifier un nouveau chemin d’accès source ou d’annuler l’installation.

Vous pouvez utiliser des indicateurs spécifiés lors de l’appel à [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) pour modifier la disposition et le comportement de la boîte de dialogue. À l’aide de ces indicateurs, vous pouvez contrôler si la boîte de dialogue contient des boutons qui permettent à l’utilisateur de rechercher un nouveau chemin d’accès source ou d’ignorer le fichier actif. Les indicateurs vous permettent également de contrôler le comportement de la boîte de dialogue, comme le signal sonore lors de la première affichage, et la possibilité d’être affichée sous la forme d’une fenêtre de premier plan.

 

 



