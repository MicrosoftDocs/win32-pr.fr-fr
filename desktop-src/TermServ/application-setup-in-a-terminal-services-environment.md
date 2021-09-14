---
title: Configuration des applications
description: L’installation d’une application pour un seul utilisateur peut créer des problèmes dans un environnement multi-utilisateur Services Bureau à distance.
ms.assetid: 3e60e95a-3580-48aa-a9f9-8fd899aa7fca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3c53f2370f4123352489ac747546e3335c558
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217516"
---
# <a name="application-setup"></a>Configuration des applications

La procédure d’installation automatisée pour de nombreuses applications existantes suppose que l’application est en cours d’installation pour un seul utilisateur. Dans un environnement multi-utilisateur Services Bureau à distance, cette hypothèse peut créer les problèmes suivants :

-   Si la procédure d’installation met à jour l’environnement du Registre et des postes de travail pour un seul utilisateur, les utilisateurs supplémentaires doivent réinstaller le package entier ou un administrateur doit copier manuellement les informations du Registre et du Bureau d’un utilisateur vers les autres utilisateurs.
-   Avec certaines procédures de configuration, vous pouvez personnaliser l’application au moment de l’installation en excluant les fonctionnalités. Si le programme d’installation initial exclut une partie de l’application, les utilisateurs supplémentaires doivent réinstaller l’application pour obtenir les fonctionnalités exclues.

Pour éviter ces problèmes, les procédures de configuration doivent suivre les instructions suivantes lors de l’installation d’une application sur un serveur hôte de session Bureau à distance (hôte de session Bureau à distance) :

-   Installer des applications dans l’environnement utilisateur par défaut commun à tous les utilisateurs. Avant d’installer l’application, exécutez la commande **change user/install** console et, une fois l’installation terminée, exécutez la commande **change user/execute** console. Utilisez un script de compatibilité Services Bureau à distance pour l’installation.
-   Prendre en charge la personnalisation propre à l’utilisateur via l’utilisation de profils utilisateur. Pour ce faire, créez un [format de fichier de modèle d’administration](/previous-versions/windows/desktop/Policy/administrative-template-file-format) afin qu’un administrateur puisse configurer le registre pour indiquer les fonctionnalités disponibles pour chaque utilisateur. Ensuite, au moment de l’exécution, l’application peut activer ou désactiver les fonctionnalités en fonction des paramètres des paramètres du registre de l’utilisateur actuel. L’application peut stocker la configuration par utilisateur dans la ruche de Registre **HKEY CURRENT USER** et laisser chaque utilisateur configurer l’application en fonction de ses préférences.

 

 