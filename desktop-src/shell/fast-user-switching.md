---
description: Dans les systèmes d’exploitation plus anciens, un utilisateur était obligé de fermer la session pour qu’un autre utilisateur puisse ouvrir une session. À compter de Windows XP, un utilisateur n’a pas à se déconnecter pour permettre à un autre utilisateur de se connecter.
ms.assetid: 72f99d32-184f-4f0b-bec1-6068c6e32f88
title: Changement rapide d'utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d79f16ef8a1ea8c97bfb61d34dfa727f3d0cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991605"
---
# <a name="fast-user-switching"></a>Changement rapide d'utilisateur

Lorsqu’un utilisateur se connecte à un ordinateur, le système charge son profil. Étant donné que chaque utilisateur dispose d’un compte d’utilisateur unique, cela permet à plusieurs utilisateurs de partager un ordinateur. Lorsqu’un utilisateur ouvre une session, les paramètres du bureau, les fichiers, les favoris et l’historique qu’il affiche sont les mêmes. ils ne sont pas accessibles par d’autres utilisateurs. Lorsque cet utilisateur ferme une session, son profil est conservé pour la prochaine fois qu’il ouvre une session. Dans les systèmes d’exploitation plus anciens, un utilisateur était obligé de fermer la session pour qu’un autre utilisateur puisse ouvrir une session. À compter de Windows XP, un utilisateur n’a pas à se déconnecter pour permettre à un autre utilisateur de se connecter. Au lieu de cela, il est possible pour plusieurs utilisateurs de se connecter et de basculer rapidement entre leurs comptes ouverts. Cette fonctionnalité est appelée *changement rapide d’utilisateur*. Le basculement vers un autre compte ne modifie pas l’état des applications qu’un utilisateur exécute actuellement. Supposons, par exemple, qu’un utilisateur autorise un autre utilisateur à basculer vers son compte lorsque le premier utilisateur a ouvert une session. Lorsque le premier utilisateur revient à son compte, ses applications sont en cours d’exécution et leurs connexions réseau sont conservées. Par conséquent, il semble que les deux utilisateurs utilisent l’ordinateur simultanément.

Si vos applications sont conformes aux exigences du logo Windows 2000, elles doivent fonctionner avec le changement rapide d’utilisateur sur les systèmes d’exploitation Windows XP et versions ultérieures. Toutefois, il est important de garder ce scénario à l’esprit lorsque vous développez une application afin qu’elle se comporte comme les utilisateurs l’attendent. Utilisez les instructions suivantes lors de l’écriture de vos applications :

-   Implémentez une véritable séparation de profil. Le système fournit une infrastructure sous-jacente qui prend en charge la séparation des données utilisateur, des paramètres utilisateur et des paramètres de l’ordinateur. Par exemple, utilisez le dossier **documents** de l’utilisateur pour stocker les données créées par l’utilisateur. Pour localiser un répertoire pour les données spécifiques à l’application, utilisez le système de [dossiers connu](known-folders.md) avec [**FOLDERID \_ RoamingAppData**](knownfolderid.md)) ou, pour les systèmes d’exploitation plus anciens, le système [**CSIDL**](csidl.md) avec [**CSIDL \_ AppData**](csidl.md)). Utilisez **FOLDERID \_ LocalAppData** ou **CSIDL \_ local \_ AppData** pour les données qui ne doivent pas être accessibles à l’utilisateur sur d’autres ordinateurs, tels que les fichiers temporaires.
-   S’inscrire pour la notification d’un changement d’utilisateur. En règle générale, une application n’a pas besoin d’être averti lorsque le commutateur se produit. Toutefois, si votre application doit être avertie d’une modification de session, elle peut s’inscrire pour recevoir un message de [**\_ \_ modification WM WTSSESSION**](../termserv/wm-wtssession-change.md) .
-   Tenez compte des autres instances de votre application. Par exemple, il peut arriver qu’une application doive télécharger une mise à jour à partir d’Internet. La mise à jour peut échouer si un autre utilisateur exécute simultanément une instance de l’application dans une autre session. Même si la mise à jour a abouti, la mise à jour peut entraîner un comportement imprévisible des autres instances de l’application en cours d’exécution. Par conséquent, il est préférable d’effectuer une mise à niveau dynamique uniquement si aucune autre instance de l’application n’est en cours d’exécution. Avant de télécharger une mise à jour d’application, il peut être utile d’implémenter une méthode qui signale toutes les instances de l’application en cours d’exécution pour enregistrer les données et s’arrêter correctement.

 

 
