---
title: États suspendus
description: Au cours d’une opération de connexion, il peut arriver que le serveur distant ne puisse pas continuer sans informations supplémentaires de la part de l’utilisateur local.
ms.assetid: a1a36b2a-33df-4cba-85a6-f4225779cd63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec66a63adbee524ec231b5c9dd9b0b410c8f4fbc73746ae9b924294c680b4a9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029139"
---
# <a name="paused-states"></a>États suspendus

Au cours d’une opération de connexion, il peut arriver que le serveur distant ne puisse pas continuer sans informations supplémentaires de la part de l’utilisateur local. À partir de Windows NT 3,5, la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) prend en charge les États suspendus. Un état suspendu permet au gestionnaire de connexions d’accès à distance de suspendre une opération de connexion afin que l’application cliente RAS puisse collecter des informations auprès de l’utilisateur.

Les États suspendus sont utiles dans les situations suivantes :

-   Lorsque l’utilisateur doit fournir un numéro de [rappel](callback-connections.md) .
-   En cas d’échec de l’authentification de l’utilisateur, l’utilisateur peut taper un nom d’utilisateur et un mot de passe différents.
-   Lorsque le mot de passe de l’utilisateur a expiré, l’utilisateur peut fournir un nouveau mot de passe.

Par défaut, la prise en charge de l’état suspendu est désactivée. Les clients RAS qui souhaitent prendre en charge les États suspendus doivent définir l' \_ indicateur RDEOPTS PausedStates dans la structure [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) transmise en tant que paramètre à [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

Lorsqu’un état suspendu se produit, le gestionnaire de connexions d’accès à distance appelle le gestionnaire de notification du client. Si la prise en charge de l’état suspendu est désactivée, le message de notification indique une erreur et l’opération de connexion échoue. S’il est activé, le gestionnaire de connexions interrompt l’opération de connexion pour attendre la réponse du client RAS. Le client RAS peut reprendre l’opération de connexion par un deuxième appel de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) , ou l’arrêter en appelant la fonction [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) .

Après avoir obtenu l’entrée de l’utilisateur, le client RAS redémarre l’opération de connexion en appelant à nouveau [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . Ce deuxième appel de **rasdial** doit spécifier les informations suivantes :

-   Handle de connexion qui a été retourné par l’appel de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) d’origine.
-   Le même gestionnaire de notification que l’appel de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) d’origine.
-   Entrée de l’utilisateur dans les membres appropriés de la structure [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) . Les autres membres de la structure **RASDIALPARAMS** doivent avoir les mêmes informations que celles spécifiées dans l’appel de la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) d’origine.

Le deuxième appel de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) ne peut pas être effectué à partir du gestionnaire de notifications.

 

 