---
description: La routine de rappel de file d’attente par défaut gère les notifications envoyées par SetupCommitFileQueue de manière générique.
ms.assetid: 6f2b3b9f-86e5-42af-8adc-29a1c768d106
title: À propos de la routine de rappel de file d’attente par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dfd22a9fa260aa1e98a2085e0cb925ed1f3438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862378"
---
# <a name="about-the-default-queue-callback-routine"></a>À propos de la routine de rappel de file d’attente par défaut

La routine de rappel de file d’attente par défaut gère les notifications envoyées par [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) de manière générique. À l’aide de la routine par défaut, vous disposez d’une interface utilisateur prête à l’emploi pour créer des boîtes de dialogue d’installation communes. Il est recommandé d’utiliser la routine de rappel de file d’attente par défaut, à la fois pour faciliter l’utilisation et pour garantir une apparence et un comportement cohérents des boîtes de dialogue générées pendant l’installation.

La routine de rappel par défaut nécessite une structure de contexte pour assurer la conservation des enregistrements internes. En outre, la file d’attente transmet des informations supplémentaires relatives à la notification actuelle dans un ensemble de paramètres, *param1* et *param2*.

Par exemple, si la file d’attente envoie une \_ notification SPFILENOTIFY NEEDMEDIA à la routine de rappel par défaut, *param1* pointe vers une structure de [**\_ média source**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) qui contient des informations sur les supports nécessaires et *param2* pointe vers un tableau de caractères qui peut recevoir de nouvelles informations de chemin d’accès de l’utilisateur.

La routine de rappel par défaut utilise ces informations pour inviter l’utilisateur à insérer le média source nécessaire, à spécifier un nouveau chemin d’accès, à ignorer la copie du fichier actuel ou à annuler l’opération en cours. La routine de rappel de file d’attente par défaut retourne FILEOP \_ NewPath, FILEOP \_ doit, FILEOP \_ Skip ou FILEOP \_ Abort dans la file d’attente, en fonction de l’action effectuée par l’utilisateur.

Pour plus d’informations sur la façon dont la routine de rappel de file d’attente par défaut gère chaque notification de file d’attente, consultez [files d’attente de fichiers](file-queue-notifications.md).

Pour plus d’informations sur les routines de rappel de file d’attente personnalisées, consultez [création d’une routine de rappel de file d’attente personnalisée](creating-a-custom-queue-callback-routine.md).

 

 



