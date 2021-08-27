---
title: Gestion des quotas pour les shells distants
description: La gestion des quotas permet aux utilisateurs de gérer plus efficacement les ressources système.
ms.assetid: 6651a500-a95a-45a1-b46a-27b2e9b36a1c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8cfa177d6f09552238471ff29d81d0ac0b7351
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883214"
---
# <a name="quota-management-for-remote-shells"></a>Gestion des quotas pour les shells distants

La gestion des quotas permet aux utilisateurs de gérer plus efficacement les ressources système. Windows La gestion à distance (WinRM) a ajouté un ensemble spécifique de quotas qui offrent une meilleure qualité de service, vous aident à éviter les problèmes de déni de service et à allouer des ressources serveur à des utilisateurs simultanés. l’ensemble de quotas WinRM est basé sur l’infrastructure de quota qui est implémentée pour le service Internet Information Services (IIS).

L’implémentation de quotas permet d’éviter une dégradation des performances et des problèmes de déni de service en procédant comme suit :

-   Limitation du nombre de shells et de processus de Shell qu’un utilisateur peut créer
-   Limitation du nombre maximal d’utilisateurs simultanés
-   Gestion de la quantité de mémoire allouée à un interpréteur de commandes
-   Définition d’un délai d’attente pour les shells inactifs

## <a name="quota-settings"></a>Paramètres de Quota

Les quotas suivants doivent être appliqués pour la gestion des shells distants. Ces quotas peuvent être configurés via l’utilitaire WinRM ou via les paramètres de stratégie de groupe. Paramètres configurée par un stratégie de groupe remplacent les quotas définis par l’utilitaire winrm. pour plus d’informations sur la définition de stratégies de groupe pour WinRM, consultez [Installation et Configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).

<dl> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

Durée maximale, en millisecondes, avant la suppression d’un shell distant inactif. La valeur par défaut est 180000 millisecondes. La durée minimale est de 1000 millisecondes.

</dd> <dt>

<span id="MaxProcessesPerShell"></span><span id="maxprocessespershell"></span><span id="MAXPROCESSESPERSHELL"></span>MaxProcessesPerShell
</dt> <dd>

Nombre maximal de processus autorisés par Shell, y compris les processus enfants de l’interpréteur de commandes. La valeur par défaut est 25.

</dd> <dt>

<span id="MaxMemoryPerShellMB"></span><span id="maxmemorypershellmb"></span><span id="MAXMEMORYPERSHELLMB"></span>MaxMemoryPerShellMB
</dt> <dd>

Quantité maximale de mémoire allouée par Shell, y compris les processus enfants de l’interpréteur de commandes. La valeur par défaut est 1024 Mo.

> [!Note]  
> Le comportement n’est pas pris en charge si MaxMemoryPerShellMB est défini sur une valeur inférieure à la valeur par défaut.

 

</dd> <dt>

<span id="MaxShellsPerUser"></span><span id="maxshellsperuser"></span><span id="MAXSHELLSPERUSER"></span>MaxShellsPerUser
</dt> <dd>

Nombre maximal de shells par utilisateur. La valeur par défaut est 30.

</dd> <dt>

<span id="MaxConcurrentUsers"></span><span id="maxconcurrentusers"></span><span id="MAXCONCURRENTUSERS"></span>MaxConcurrentUsers
</dt> <dd>

Nombre maximal d’utilisateurs simultanés qui peuvent ouvrir des shells. La valeur par défaut est de 10.

</dd> </dl>

## <a name="deprecated-quotas"></a>Quotas déconseillés

WinRM 2,0 définit le quota MaxShellRunTime en lecture seule. La modification de la valeur de ce quota n’aura aucun effet sur les shells distants.

## <a name="retrieving-quota-configuration-information"></a>Récupération des informations de configuration de quota

Pour vérifier les paramètres de configuration de quota, tapez **WinRM-Télécharger winrm/config**.

L’extrait de code suivant est un exemple basé sur du texte d’une configuration WinRM avec les paramètres de quota par défaut.

``` syntax
Config

          ...         

          Winrs

                   AllowRemoteShellAccess = true

                   IdleTimeout = 7200000

                   MaxConcurrentUsers = 10

                   MaxProcessesPerShell = 25

                   MaxMemoryPerShellMB = 1024

                   MaxShellsPerUser = 30
```

## <a name="configuring-shell-quotas"></a>Configuration des quotas de l’interpréteur de commandes

Les quotas peuvent être définis à l’aide d’un paramètre stratégie de groupe ou manuellement. pour plus d’informations sur les paramètres de configuration spécifiques, consultez [Installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).

**Pour définir un quota avec stratégie de groupe**

1.  Ouvrez une fenêtre d’invite de commandes en tant qu’administrateur.
2.  À l’invite de commandes, tapez **gpedit. msc**. La fenêtre de l' **éditeur d’objets stratégie de groupe** s’ouvre.
3.  recherchez les **Windows Remote Management** et Windows objets de l' **interpréteur de commandes à distance** stratégie de groupe, sous **Configuration ordinateur \\ Modèles d’administration \\ Windows composants**.
4.  Sous l’onglet **étendue** , sélectionnez un paramètre pour afficher une description. Double-cliquez sur un paramètre pour le modifier.

**Pour définir un quota manuellement**

1.  Ouvrez une fenêtre d’invite de commandes en tant qu’administrateur.
2.  À l’invite de commandes, tapez **winrm set winrm/config/Winrs' @ {**_&lt; &gt; quota_*_= "_*_&lt; value &gt;_*_"} '_*

Par exemple, pour augmenter le nombre maximal de shells par utilisateur de 5 à 7, tapez **winrm set winrm/config/Winrs' @ {MaxShellsPerUser = "7"} '**.

 

 




