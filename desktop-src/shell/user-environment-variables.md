---
description: Les variables d’environnement spécifient des chemins de recherche pour les fichiers, les répertoires de fichiers temporaires, les options spécifiques à l’application et d’autres informations similaires.
ms.assetid: 6180e54e-4bd9-4692-83fd-f3f7f1d8f8d7
title: Variables d’environnement utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4f898c7a9135c0421fdd67a7bed1d97655556f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991613"
---
# <a name="user-environment-variables"></a>Variables d’environnement utilisateur

Les variables d’environnement spécifient des chemins de recherche pour les fichiers, les répertoires de fichiers temporaires, les options spécifiques à l’application et d’autres informations similaires. Le système gère un bloc d’environnement pour chaque utilisateur et un pour l’ordinateur. Le bloc environnement système représente les variables d’environnement pour tous les utilisateurs de l’ordinateur en question. Le bloc environnement d’un utilisateur représente les variables d’environnement gérées par le système pour cet utilisateur particulier, y compris l’ensemble de variables d’environnement système.

Par défaut, chaque processus reçoit une copie du bloc d’environnement pour son processus parent. En règle générale, il s’agit du bloc d’environnement de l’utilisateur qui a ouvert une session. Un processus peut spécifier différents blocs d’environnement pour ses processus enfants à l’aide de la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ou [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .

Pour ajouter ou modifier des variables d’environnement, l’utilisateur sélectionne **système** dans le **panneau de configuration**, puis il sélectionne l’onglet **environnement** . L’utilisateur peut également ajouter ou modifier des variables d’environnement à partir d’une invite de commandes à l’aide de la commande **Set** . Les variables d’environnement créées avec la commande **Set** s’appliquent uniquement à la fenêtre de commande dans laquelle elles sont définies, et à ses processus enfants. Pour plus d’informations, tapez **Set/ ?** à une invite de commandes.

Pour récupérer une copie du bloc d’environnement pour un utilisateur donné, utilisez la fonction [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) . Pour libérer un bloc d’environnement créé par **CreateEnvironmentBlock**, utilisez la fonction [**DestroyEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock) . Ces fonctions font référence à un pointeur vers un bloc d’environnement. Le bloc environnement est un tableau de chaînes Unicode se terminant par un caractère null. La liste se termine par deux valeurs null ( \\ 0 \\ 0).

Pour développer une chaîne qui contient des variables d’environnement à l’aide du bloc d’environnement d’un utilisateur spécifié, utilisez la fonction [**ExpandEnvironmentStringsForUser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) .

 

 
