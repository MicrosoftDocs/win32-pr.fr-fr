---
description: Les notifications sont des valeurs qu’une fonction d’installation envoie à une routine de rappel pour spécifier un État ou un événement. Deux paramètres, param1 et param2, sont envoyés avec la notification et contiennent des informations supplémentaires relatives à la notification.
ms.assetid: 93434558-ae83-4ea2-9324-659e5873a8c3
title: Notifications (API du programme d’installation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 096d4261a99e0a837a90aa5c965a3b676843945d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520648"
---
# <a name="notifications-setup-api"></a>Notifications (API du programme d’installation)

Les notifications sont des valeurs qu’une fonction d’installation envoie à une routine de rappel pour spécifier un État ou un événement. Deux paramètres, *param1* et *param2*, sont envoyés avec la notification et contiennent des informations supplémentaires relatives à la notification.

La routine de rappel traite la notification et retourne un entier non signé à la fonction d’installation. Selon la fonction d’installation, vous pouvez utiliser cette valeur pour spécifier une opération ou une sélection de l’utilisateur, ou vous pouvez l’ignorer.

Les fonctions d’installation envoient des notifications aux routines de rappel à l’aide de la syntaxe suivante.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //notification code
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

Le paramètre de *contexte* est un pointeur void vers une structure ou une variable de contexte que la routine de rappel peut utiliser pour stocker des informations qui doivent être conservées entre les appels suivants de la routine de rappel.

Étant donné que la routine de rappel spécifie l’implémentation du contexte et qu’elle n’est jamais référencée ni modifiée par les fonctions d’installation, le contexte n’est pas documenté dans les documents de référence pour les messages de notification qui suivent.

Le paramètre de *notification* spécifie une valeur entière non signée pour un événement ou un État qui amène la fonction d’installation à appeler la routine de rappel.

*Param1* et *param2* sont des paramètres facultatifs qui peuvent contenir des informations supplémentaires relatives à la notification. Ces paramètres sont des entiers non signés. Si *param1* ou *param2* renvoient des informations qui ne sont pas un entier non signé, elles sont converties en un entier non signé et doivent être reconverties dans leur type de données d’origine avant de pouvoir être utilisées par la routine de rappel.

> [!Note]  
> Les notifications suivantes représentent chaque notification utilisée par les fonctions d’installation. Les fonctions individuelles utilisent un sous-ensemble de ces notifications. En d’autres termes, toutes les notifications ne sont pas utilisées par chaque fonction.

 

Les notifications suivantes sont utilisées par les fonctions d’installation.



| Notification                                                                     | Description                                                                                   |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md)                        | Une erreur s’est produite lors d’une opération de copie de fichier.                                               |
| [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)                    | Une erreur s’est produite lors d’une opération de suppression de fichier.                                           |
| [**SPFILENOTIFY \_ ENDCOPY**](spfilenotify-endcopy.md)                            | Une opération de copie de fichier est terminée.                                                              |
| [**SPFILENOTIFY \_ ENDDELETE**](spfilenotify-enddelete.md)                        | Une opération de suppression de fichier s’est terminée.                                                          |
| [**SPFILENOTIFY \_ ENDQUEUE**](spfilenotify-endqueue.md)                          | La file d’attente a terminé la validation.                                                            |
| [**SPFILENOTIFY \_ ENDREGISTRATION**](spfilenotify-endregistration.md)            | L’inscription ou l’annulation de l’inscription du fichier est terminée.                                  |
| [**SPFILENOTIFY \_ ENDRENAME**](spfilenotify-endrename.md)                        | Une opération de changement de nom de fichier s’est terminée.                                                            |
| [**SPFILENOTIFY \_ ENDSUBQUEUE**](spfilenotify-endsubqueue.md)                    | Une sous-file d’attente (copier, renommer ou supprimer) s’est terminée.                                         |
| [**SPFILENOTIFY \_ FILEEXTRACTED**](spfilenotify-fileextracted.md)                | Le fichier a été extrait de l’armoire.                                                 |
| [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)                | Un fichier est trouvé dans le fichier CAB.                                                         |
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md)                | Le fichier était en cours d’utilisation et l’opération actuelle a été retardée jusqu’au redémarrage du système. |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)                  | Le langage de l’opération en cours ne correspond pas à la langue du système.                     |
| [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md)                        | Un nouveau média source est requis.                                                                 |
| [**SPFILENOTIFY \_ NEEDNEWCABINET**](spfilenotify-neednewcabinet.md)              | Le fichier actuel se poursuit dans le fichier CAB suivant.                                            |
| [**SPFILENOTIFY \_ QUEUESCAN**](spfilenotify-queuescan.md)                        | Un nœud de la file d’attente de fichiers a été analysé.                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ ex**](spfilenotify-queuescan-ex.md)                 | Un nœud de la file d’attente de fichiers a été analysé.                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ signataires**](spfilenotify-queuescan-signerinfo.md) | Un nœud de la file d’attente de fichiers a été analysé.                                                    |
| [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md)                    | Une erreur s’est produite lors d’une opération de changement de nom de fichier.                                             |
| [**SPFILENOTIFY \_ STARTCOPY**](spfilenotify-startcopy.md)                        | Une opération de copie de fichier a démarré.                                                            |
| [**SPFILENOTIFY \_ STARTDELETE**](spfilenotify-startdelete.md)                    | Une opération de suppression de fichier a démarré.                                                          |
| [**SPFILENOTIFY \_ STARTQUEUE**](spfilenotify-startqueue.md)                      | La file d’attente a commencé la validation.                                                              |
| [**SPFILENOTIFY \_ STARTREGISTRATION**](spfilenotify-startregistration.md)        | L’inscription ou l’annulation de l’inscription du fichier a démarré.                                   |
| [**SPFILENOTIFY \_ STARTRENAME**](spfilenotify-startrename.md)                    | Une opération de changement de nom de fichier a démarré.                                                          |
| [**SPFILENOTIFY \_ STARTSUBQUEUE**](spfilenotify-startsubqueue.md)                | Une sous-file d’attente (copier, renommer ou supprimer) a démarré.                                       |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)                  | Une copie du fichier spécifié existe déjà sur la cible.                                    |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)                    | Une version plus récente du fichier spécifié existe sur la cible.                                   |



 

 

 



