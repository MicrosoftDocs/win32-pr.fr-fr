---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: 77d0ffc2-76a2-4a21-88e1-1ca85b8c5d2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0a56272ba095f244e48e335049ec5b88b64855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509815"
---
# <a name="iagentcharacter"></a>IAgentCharacter

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

**IAgentCharacter** définit une interface qui permet aux applications d’interroger les propriétés de caractères et de lire les animations. Ces fonctions sont également disponibles à partir de [**IAgentCharacterEx**](iagentcharacterex.md). Vous pouvez utiliser des ID de demande de retour de méthode pour suivre leur état dans la file d’attente du caractère et synchroniser votre code avec l’état actuel de l’animation du caractère.

**Méthodes dans l'ordre Vtable**



| Méthodes IAgentCharacter                                           | Description                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**GetVisible**](iagentcharacter--getvisible.md)                 | Retourne une valeur indiquant si le caractère (Frame) est actuellement visible.                       |
| [**SetPosition**](iagentcharacter--setposition.md)               | Définit la position du cadre de caractère.                                         |
| [**GetPosition**](iagentcharacter--getposition.md)               | Retourne la position du cadre de caractère.                                      |
| [**SetSize**](iagentcharacter--setsize.md)                       | Définit la taille du cadre de caractère.                                             |
| [**GetSize,**](iagentcharacter--getsize.md)                       | Retourne la taille du cadre de caractère.                                          |
| [**GetName**](iagentcharacter--getname.md)                       | Retourne le nom du caractère.                                                |
| [**GetDescription**](iagentcharacter--getdescription.md)         | Retourne la description du caractère.                                        |
| [**GetTTSSpeed**](iagentcharacter--getttsspeed.md)               | Retourne le paramètre de vitesse de sortie TTS actuel pour le caractère.                   |
| [**GetTTSPitch**](iagentcharacter--getttspitch.md)               | Retourne le paramètre de pas de police TTS actuel pour le caractère.                          |
| [**Déclencher**](iagentcharacter--activate.md)                     | Définit si un client est actif ou si un caractère est le plus haut.                        |
| [**SetIdleOn**](iagentcharacter--setidleon.md)                   | Définit le traitement inactif du serveur.                                                |
| [**GetIdleOn**](iagentcharacter--getidleon.md)                   | Retourne le paramètre du traitement inactif du serveur.                              |
| [**Préparation**](iagentcharacter--prepare.md)                       | Récupère les données d’animation pour le caractère.                                       |
| [**Lire**](iagentcharacter--play.md)                             | Lit une animation spécifiée.                                                      |
| [**Erreur**](iagentcharacter--stop.md)                             | Arrête une animation pour un caractère.                                               |
| [**StopAll**](iagentcharacter--stopall.md)                       | Arrête toutes les animations d’un caractère.                                             |
| [**Wait**](iagentcharacter--wait.md)                             | Contient la file d’attente d’animation du caractère.                                            |
| [**Suspendre**](iagentcharacter--interrupt.md)                   | Interrompt l’animation d’un caractère.                                               |
| [**Afficher**](iagentcharacter--show.md)                             | Affiche le caractère et lit l’animation de l’état d' **affichage** du caractère.     |
| [**Masquer**](iagentcharacter--hide.md)                             | Lit l’animation de l’état de **masquage** du caractère et masque le frame du caractère. |
| [**Speak**](iagentcharacter--speak.md)                           | Lit une sortie orale pour le caractère.                                            |
| [**DéplacerVers**](iagentcharacter--moveto.md)                         | Déplace le cadre de caractère vers l’emplacement spécifié.                              |
| [**GestureAt**](iagentcharacter--gestureat.md)                   | Lit une animation gesturing en fonction de l’emplacement spécifié.                      |
| [**GetMoveCause**](iagentcharacter--getmovecause.md)             | Récupère la cause du dernier déplacement du caractère.                                 |
| [**GetVisibilityCause**](iagentcharacter--getvisibilitycause.md) | Récupère la cause de la dernière modification de l’état de visibilité du caractère.       |
| [**HasOtherClients**](iagentcharacter--hasotherclients.md)       | Récupère si le caractère a d’autres clients actuels.                        |
| [**SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md)   | Détermine si les effets sonores d’une animation de caractères jouent.                    |
| [**GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md)   | Récupère si le paramètre effets sonores d’un caractère est activé.                 |
| [**SetName**](iagentcharacter--setname.md)                       | Définit le nom du caractère.                                                        |
| [**SetDescription**](iagentcharacter--setdescription.md)         | Définit la description du caractère.                                                 |
| [**GetExtraData**](iagentcharacter--getextradata.md)             | Récupère des données supplémentaires stockées avec le caractère.                              |



 

 

 




