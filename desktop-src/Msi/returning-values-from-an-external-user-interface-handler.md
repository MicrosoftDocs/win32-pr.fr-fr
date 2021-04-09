---
description: Un gestionnaire d’interface utilisateur externe peut retourner n’importe quel nombre de valeurs à Windows Installer en fonction du type de bouton fourni dans le paramètre de type de message que le programme d’installation transmet au gestionnaire.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Retour de valeurs à partir d’un gestionnaire d’interface utilisateur externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b466f6bc3cc034551a01bd2b87caa7292824e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754204"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a>Retour de valeurs à partir d’un gestionnaire d’interface utilisateur externe

Un gestionnaire d’interface utilisateur externe peut retourner n’importe quel nombre de valeurs à Windows Installer en fonction du type de bouton fourni dans le paramètre de type de message que le programme d’installation transmet au gestionnaire.

Le gestionnaire d’interface utilisateur externe peut retourner les valeurs 1 et 0 à tout moment, car celles-ci ne sont pas liées aux types de boutons. Une valeur de retour de-1 indique qu’une erreur interne s’est produite dans le gestionnaire d’interface utilisateur externe. Une valeur de retour de 0 indique que le gestionnaire de l’interface utilisateur externe n’a pas géré le message du programme d’installation et que le programme d’installation doit gérer le message à la place.

Pour les messages qui n’incluent pas de type de bouton, tels que INSTALLMESSAGE \_ ACTIONDATA et INSTALLMESSAGE \_ Progress, le retour de IDCANCEL annule l’installation. Le renvoi de IDOK notifie le programme d’installation que le message a été géré par le gestionnaire d’interface utilisateur externe.

Les valeurs de retour restantes, comme décrit ci-dessous, sont directement liées aux types de bouton inclus avec le type de message.



| Valeur de retour de l’interface utilisateur externe | Signification                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| IDOK                     | L’utilisateur a cliqué sur le bouton **OK** . Les informations du message ont été comprises.                     |
| IDCANCEL                 | Le bouton **Annuler** a été enfoncé. Annulez l’installation.                                            |
| IDABORT                  | Le bouton **abandonner** a été enfoncé. Abandonner l’installation.                                              |
| IDRETRY                  | Le bouton **Réessayer** a été enfoncé. Recommencez l’opération.                                                |
| IDIGNORE                 | L’utilisateur a cliqué sur le bouton **Ignorer** . Ignorez l’erreur et continuez.                                      |
| IDYES                    | Le bouton **Oui** a été enfoncé. La réponse affirmative, poursuivez avec la séquence d’événements actuelle.   |
| IDNO                     | Le bouton **non** a été enfoncé. La réponse négative ne continue pas avec la séquence d’événements en cours. |



 

Par exemple, si le gestionnaire d’interface utilisateur externe reçoit un message avec l' \_ indicateur de styles de la boîte de message Mo ABORTRETRYIGNORE, le gestionnaire d’interface utilisateur externe peut retourner l’une des valeurs suivantes :

-   – 1 (erreur dans le gestionnaire d’interface utilisateur externe)
-   0 (aucune action effectuée dans le gestionnaire d’interface utilisateur externe, laissez Windows Installer le gérer)
-   IDABORT (bouton **abandonner** enfoncé)
-   IDRETRY (bouton **Réessayer** enfoncé)
-   IDIGNORE (bouton **Ignorer** enfoncé)

 

 



