---
title: Description des informations d’erreur étendues
description: Les informations d’erreur étendues sont un tableau d’enregistrements, chacun indiquant le passage du code d’erreur via une couche particulière du système ou de l’application.
ms.assetid: 1b112e49-bdb2-4014-b86d-3c6d8ebe4fcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2918caa446f7cee9c4eaa609a5713c9cb385e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011389"
---
# <a name="understanding-extended-error-information"></a>Description des informations d’erreur étendues

Les informations d’erreur étendues sont un tableau d’enregistrements, chacun indiquant le passage du code d’erreur via une couche particulière du système ou de l’application. Si une erreur se produit sur un ordinateur C, tel qu’il est appelé à partir de l’ordinateur B, qui à son tour est appelé à partir de l’ordinateur A, le temps d’exécution RPC sur l’ordinateur C génère un ou plusieurs enregistrements décrivant l’erreur et les transmet à l’ordinateur B. l’ordinateur B peut ajouter un ou plusieurs enregistrements au début de la chaîne existante.  et passe la chaîne complète à un. Un peut ajouter un ou plusieurs enregistrements, et afficher ou enregistrer les informations. La chaîne d’erreur étendue représente essentiellement l’historique de l’erreur.

Les informations d’erreur étendues ne remplacent pas le code d’erreur ( \_ code d’état RPC S \_ \* ). Quelle que soit la quantité d’informations d’erreur étendues générées, le code d’erreur reste inchangé.

Chaque enregistrement d’informations sur les erreurs étendues contient les éléments suivants. Pour plus d’informations, consultez [**\_ \_ \_ informations d’erreur étendues RPC**](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info) :

-   ComputerName : nom DNS non qualifié de l’ordinateur d’où provient l’erreur. Seuls les enregistrements sur les limites de la machine contiennent ces informations. Par exemple, dans le scénario décrit précédemment avec les machines A, B et C, le nom d’ordinateur est défini pour les champs suivants :

    | Enregistrement                            | Champ ComputerName |
    |-----------------------------------|--------------------|
    | Enregistrement \# 1 généré par l’ordinateur C | \-                 |
    | Enregistrement \# 2 généré par l’ordinateur C | \-                 |
    | Enregistrement \# 3 généré par l’ordinateur C | C                  |
    | Enregistrement \# 1 généré par l’ordinateur B | \-                 |
    | Enregistrement \# 2 généré par l’ordinateur B | \-                 |
    | Enregistrement \# 3 généré par l’ordinateur B | B                  |
    | Enregistrement \# 1 généré par l’ordinateur A | \-                 |
    | Enregistrement \# 2 généré par l’ordinateur A | \-                 |
    | Enregistrement \# 3 généré par l’ordinateur A | \-                 |
    | En-tête de la chaîne                 |                    |

    

     

<!-- -->

-   ProcessID : identificateur du processus qui a généré l’erreur.
-   TimeStamp : heure à laquelle l’erreur s’est produite, exprimée au format UTC.
-   Génération du composant : définition de code entier du composant logique qui a généré l’erreur. Les composants suivants sont actuellement définis :

    | Code | Nom              | Description                                                                                                                                                                           |
    |------|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1    | Application       | Composant propriétaire de la routine du gestionnaire pour l’appel RPC particulier                                                                                                                  |
    | 2    | Runtime           | Heure d’exécution RPC                                                                                                                                                                      |
    | 3    | Fournisseur de sécurité | Fournisseur de sécurité pour cet appel.                                                                                                                                                  |
    | 4    | NPFS              | Le système de fichiers NPFS                                                                                                                                                                  |
    | 5    | RDR               | Le redirecteur                                                                                                                                                                        |
    | 6    | NNOM du Pack               | Système de canal nommé. Il peut s’agir de NPFS ou de RDR, mais dans de nombreux cas, la durée d’exécution RPC ne sait pas qui a effectué l’opération demandée, et dans ce cas, NNOM du Pack est retourné. |
    | 7    | IO                | Le système d’e/s ou un pilote utilisé par le système d’e/s. Il peut s’agir de NPFS, de RDR ou d’un fournisseur Winsock.                                                                                 |
    | 8    | Winsock           | Fournisseur Winsock                                                                                                                                                                  |
    | 9    | Code d’autorisation        | API d’autorisation.                                                                                                                                                               |
    | 10   | LPC               | Fonctionnalité d’appel de procédure locale.                                                                                                                                                    |

    

     

<!-- -->

-   État : code d’erreur généré ou retourné par la couche
-   DetectionLocation : numéro unique identifiant l’emplacement du code où l’erreur a été détectée. Ce champ est lié au code et passe de la version à la version. Une liste distincte des emplacements de détection les plus fréquemment rencontrés sera publiée.
-   Flags : indicateurs spécifiant des informations sur l’enregistrement. Les indicateurs actuellement définis sont EEInfoPreviousRecordsMissing et EEInfoNextRecordsMissing, qui correspondent respectivement aux valeurs numériques 1 et 2. Si EEInfoPreviousRecordsMissing est défini, un ou plusieurs enregistrements avant cet enregistrement sont manquants. Si EEInfoNextRecordsMissing est défini, un ou plusieurs enregistrements sont manquants après cet enregistrement. Pour obtenir une description de la raison pour laquelle des enregistrements sont manquants, consultez [fiabilité des informations d’erreur étendues](reliability-of-extended-error-information.md).
-   Jusqu’à quatre paramètres d’erreur. Un paramètre d’erreur est une structure de variante légère fournissant des informations supplémentaires sur l’erreur. Les informations supplémentaires dépendent de l’erreur et de l’emplacement de détection. Les paramètres peuvent être de type chaîne ANSI (LPSTR), chaîne Unicode (LPWSTR), valeur long (long), valeur Short (short), pointer (Int64) ou None.

 

 




