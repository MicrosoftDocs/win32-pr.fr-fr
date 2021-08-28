---
description: Tous les paramètres d’authentification sont effectués via le Gestionnaire des services Internet.
ms.assetid: 9b118120-f0cb-4973-b537-dd3d12a7a6d5
ms.tgt_platform: multiple
title: Configuration d’IIS 5,0 et versions ultérieures pour les scripts ASP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ade580408337c2b559ce46f8125e7d639205d8014e288a7a63d9730fde3fba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131621"
---
# <a name="configuring-iis-50-and-later-for-wmi-asp-scripting"></a>Configuration d’IIS 5,0 et versions ultérieures pour les scripts ASP WMI

Tous les paramètres d’authentification sont effectués via le Gestionnaire des services Internet.

Lors de la configuration d’Internet Information Server (IIS) 5,0 et de la sécurité IIS 6,0 pour les scripts ASP WMI, tenez compte des points suivants :

-   [Niveau d'authentification](#authentication-level)

    Vous pouvez configurer au niveau du serveur, du répertoire ou du fichier.

-   [Paramètre d’authentification](#authentication-setting)

    vous pouvez définir l’authentification sur Anonymous, Windows intégrée, ou les deux.

-   [Protection](#protection)

    Vous pouvez configurer la page ASP pour qu’elle s’exécute in-process (protection faible) ou hors processus à l’aide de Dllhost.exe (protection moyenne ou élevée).

## <a name="authentication-level"></a>Niveau d’authentification

Pour renforcer la sécurité, vous pouvez configurer l’authentification au niveau du répertoire ou du fichier.

Si l’authentification est définie au niveau du serveur, tous les fichiers et répertoires suivants adhèrent à l’authentification du serveur, sauf s’ils sont explicitement modifiés au niveau du répertoire ou du fichier. Vous pouvez créer une structure de répertoires contenant tous les scripts WMI ASP où les pages HTML et les ASP spécifiques à WMI peuvent être configurés indépendamment du reste du serveur. Pour modifier le niveau d’authentification d’un serveur, d’un répertoire ou d’un fichier, procédez comme suit.

**Pour définir l’authentification à n’importe quel niveau**

1.  Dans le panneau de configuration, double-cliquez sur **Outils d’administration**, puis double-cliquez sur le composant logiciel enfichable IIS.

2.  Recherchez l’icône de page ASP, puis ouvrez les propriétés du niveau à définir, qui peut être serveur, répertoire ou fichier.

    > [!Note]  
    > Les paramètres d’authentification se trouvent sous l’onglet sécurité de **répertoire** ou **sécurité de fichier** de la feuille de **Propriétés**.

     

## <a name="authentication-setting"></a>Paramètre d’authentification

pour les scripts ASP WMI, la combinaison de l’authentification anonyme est désactivée (désactivée), et l’authentification Windows intégrée activée (activée) offre une plus grande possibilité de définir la sécurité. Pour utiliser les paramètres d’authentification IIS NT LAN Manager (NTLM), Passport ou Digest, vous devez activer les privilèges d’activation à distance, car l’utilisateur est traité comme une identité réseau et enregistré à distance. Le paramètre d’activation à distance n’est pas requis pour l’authentification anonyme et de base. Toutefois, le système est bien moins sécurisé lorsque vous utilisez l’authentification anonyme et de base.

si l’authentification anonyme est utilisée avec ou sans l’authentification Windows intégrée, l’approche la plus sécurisée consiste à utiliser une ouverture de session qui exige que l’utilisateur entre un nom d’utilisateur et un mot de passe. L’ouverture de session par défaut est l’identité IIS, mais une ouverture de session peut être créée en utilisant des autorisations spécifiques adaptées aux scripts ASP WMI qui peuvent être utilisés comme compte pour les connexions anonymes ou invitées.

Si vous choisissez un identificateur de connexion qui n’est pas une identité IIS, désactivez la case à cocher **autoriser les services Internet à contrôler le mot de passe** , puis entrez le mot de passe correct. Cela force toutes les connexions anonymes ou invitées à utiliser l’identificateur de connexion. En créant une connexion distincte de l’identité IIS, les privilèges d’un compte qui accède à WMI peuvent être contrôlés sans affecter les autres répertoires ou fichiers sur le serveur IIS, sauf si l’authentification est définie au niveau du serveur.

Procédez comme suit pour définir les conditions d’authentification pour la page ASP à l’aide du composant logiciel enfichable IIS dans le panneau de configuration.

**Pour accéder au paramètre de compte**

1.  Dans le panneau de configuration, double-cliquez sur l’icône **Outils d’administration** , ouvrez le composant logiciel enfichable IIS, localisez votre page ASP, puis ouvrez les propriétés du niveau à définir, qui peut être serveur, répertoire ou fichier.

    Les paramètres d’authentification se trouvent sous l’onglet sécurité de **répertoire** ou **sécurité de fichier** de la feuille de **Propriétés** .

2.  Dans la zone authentification anonyme, cliquez sur **modifier**.

3.  Si un identificateur de connexion autre que l’identité IIS est sélectionné, désactivez la case à cocher **autoriser les services Internet à contrôler le mot de passe**, puis entrez le mot de passe correct. Cela force toutes les connexions anonymes ou invitées à utiliser l’identificateur de connexion.

En utilisant une ouverture de session différente de l’identité IIS, les privilèges du compte qui accède à WMI peuvent être contrôlés sans affecter les autres répertoires ou fichiers sur le serveur IIS, sauf si l’authentification est définie au niveau du serveur.

la configuration précédente permet au serveur IIS d’utiliser l’authentification anonyme dans certains domaines, et l’authentification intégrée Windows ou mixte dans d’autres.

## <a name="protection"></a>Protection

La dernière considération à prendre en compte lors de la configuration du serveur IIS est la protection à utiliser lors de l’exécution d’une ASP.

Vous pouvez définir un ASP pour exécuter ce qui suit :

-   Dans le processus vers IIS (protection faible).

-   Externe à IIS avec Dllhost.exe en tant que pool ou hors processus (protection moyenne regroupée).

-   Self-of-process auto-Host (protection élevée).

> [!Note]  
> Pour un meilleur équilibre entre sécurité et performances, utilisez un hôte mis en pool.

 

 

 



