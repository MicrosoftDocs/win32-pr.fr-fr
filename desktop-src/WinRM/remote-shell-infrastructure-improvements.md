---
title: Améliorations de l’infrastructure du shell distant
description: Windows La gestion à distance 2,0 (WinRM 2,0) offre de nombreuses améliorations de l’infrastructure de l’interpréteur de commandes à distance.
ms.assetid: b22693ba-fa43-44bb-9b2d-0c64fad6e3cc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf88a472319b4b4677992f97509a3603cfe4a32f272388caf9db100b6e7457ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121659"
---
# <a name="remote-shell-infrastructure-improvements"></a>Améliorations de l’infrastructure du shell distant

Windows La gestion à distance 2,0 (WinRM 2,0) offre de nombreuses améliorations de l’infrastructure de l’interpréteur de commandes à distance. Les rubriques suivantes décrivent ces améliorations en détail :

-   [Prise en charge de plusieurs tronçons](multi-hop-support.md)
-   [Gestion des quotas pour les shells distants](quotas.md)

L’une des améliorations apportées à l’infrastructure de l’interpréteur de commandes distant WinRM est l’ajout d’un gestionnaire de Shell plus robuste qui gère les informations de l’interpréteur de commandes spécifiques à l’utilisateur. Les utilisateurs WinRM peuvent créer des shells sur des ordinateurs distants pour exécuter des commandes ou des scripts. En outre, les utilisateurs peuvent créer plusieurs shells sur un ordinateur. Les utilisateurs et les administrateurs doivent tous deux pouvoir gérer des shells. Les utilisateurs peuvent énumérer, obtenir et supprimer les shells qu’ils ont créés. Les administrateurs peuvent énumérer tous les shells actifs et récupérer des détails sur des shells spécifiques sur un hôte local ou distant. Les administrateurs peuvent également supprimer des shells actifs sur un hôte local ou distant.

Lorsqu’un utilisateur ou un administrateur énumère les interpréteurs de commande actifs, les informations suivantes peuvent être retournées par le service WinRM.

<dl> <dt>

<span id="ShellId"></span><span id="shellid"></span><span id="SHELLID"></span>ShellId
</dt> <dd>

Spécifie l’identificateur unique de l’interpréteur de commandes.

</dd> <dt>

<span id="Environment_variables"></span><span id="environment_variables"></span><span id="ENVIRONMENT_VARIABLES"></span>Variables d’environnement
</dt> <dd>

Spécifie toutes les variables d’environnement définies par l’utilisateur.

</dd> <dt>

<span id="WorkingDirectory"></span><span id="workingdirectory"></span><span id="WORKINGDIRECTORY"></span>WorkingDirectory
</dt> <dd>

Spécifie le répertoire de démarrage de l’interpréteur de commandes.

</dd> <dt>

<span id="ResourceURI"></span><span id="resourceuri"></span><span id="RESOURCEURI"></span>URI
</dt> <dd>

Spécifie l’URI de ressource pour l’opération de Shell. L’URI de ressource peut être utilisé pour récupérer la configuration de plug-in qui est spécifique à l’instance de l’interpréteur de commandes.

</dd> <dt>

<span id="IdleTimeout"></span><span id="idletimeout"></span><span id="IDLETIMEOUT"></span>IdleTimeout
</dt> <dd>

Spécifie la durée maximale, en millisecondes, pendant laquelle l’interpréteur de commandes restera ouvert sans aucune demande.

</dd> <dt>

<span id="InputStreams"></span><span id="inputstreams"></span><span id="INPUTSTREAMS"></span>InputStreams
</dt> <dd>

Spécifie les flux d’entrée pour l’interpréteur de commandes.

</dd> <dt>

<span id="OutputStreams"></span><span id="outputstreams"></span><span id="OUTPUTSTREAMS"></span>OutputStreams
</dt> <dd>

Spécifie les flux de sortie de l’interpréteur de commandes.

</dd> <dt>

<span id="Shell_creation_time"></span><span id="shell_creation_time"></span><span id="SHELL_CREATION_TIME"></span>Heure de création de l’interpréteur de commandes
</dt> <dd>

Spécifie l’horodateur de création de l’interpréteur de commandes.

</dd> <dt>

<span id="IdleTime"></span><span id="idletime"></span><span id="IDLETIME"></span>IdleTime
</dt> <dd>

Spécifie la durée, en millisecondes, pendant laquelle l’interpréteur de commandes a été inactif.

</dd> <dt>

<span id="UserId"></span><span id="userid"></span><span id="USERID"></span>IDutilisateur
</dt> <dd>

Spécifie l’ID utilisateur.

</dd> <dt>

<span id="Hostname_or_IP_address"></span><span id="hostname_or_ip_address"></span><span id="HOSTNAME_OR_IP_ADDRESS"></span>Nom d’hôte ou adresse IP
</dt> <dd>

Spécifie le nom d’hôte ou l’adresse IP de l’ordinateur qui a créé l’interpréteur de commandes.

</dd> <dt>

<span id="Shell_memory_usage"></span><span id="shell_memory_usage"></span><span id="SHELL_MEMORY_USAGE"></span>Utilisation de la mémoire de l’environnement
</dt> <dd>

Spécifie la quantité de mémoire qui a été utilisée par l’interpréteur de commandes.

</dd> <dt>

<span id="Number_of_processes"></span><span id="number_of_processes"></span><span id="NUMBER_OF_PROCESSES"></span>Nombre de processus
</dt> <dd>

Spécifie le nombre de processus qui ont été créés par l’interpréteur de commandes.

</dd> </dl>

## <a name="enumerating-a-shell-on-a-local-host"></a>Énumération d’un interpréteur de commandes sur un hôte local

La commande suivante montre comment utiliser l’utilitaire WinRM pour énumérer des shells sur un client WinRM : **WinRM Enumerate Shell**.

L’exemple de texte suivant affiche la sortie de l’énumération de l’interpréteur de commandes :

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S

Shell
    ShellId = EE3F11CE-FB3C-4C4E-B113-6F4D643C97D8
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M46S
    ShellInactivity = P0DT0H0M45S
    MemoryUsed = 48MB
    ChildProcesses = 0

Shell
    ShellId = 8FD7F2C4-A434-4D58-A7E8-46F8BF202D0B
    ResourceUri = http://schemas.microsoft.com/powershell/Microsoft.PowerShell
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin pr
    OutputStreams = stdout
    ShellRunTime = P0DT0H1M47S
    ShellInactivity = P0DT0H0M47S
    MemoryUsed = 48MB
    ChildProcesses = 0
```

Pour plus d’informations, consultez l’aide en ligne fournie en exécutant la commande suivante : **WinRM Enumerate- ?**.

## <a name="retrieving-information-about-a-specific-shell"></a>Récupération d’informations sur un interpréteur de commandes spécifique

Un administrateur ou un utilisateur peut également utiliser l’identificateur ShellId pour récupérer des informations sur l’interpréteur de commandes. La commande suivante montre comment utiliser l’utilitaire WinRM pour obtenir des informations sur un interpréteur de commandes spécifique : **WinRM obtenir l’interpréteur de commandes ? ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E**.

L’exemple de texte suivant affiche la sortie des informations de l’interpréteur de commandes :

``` syntax
Shell
    ShellId = 0A6E6A01-8AB2-4037-86CC-BFC826A1244E
    ResourceUri = http://schemas.microsoft.com/wbem/wsman/1/windows/shell/cmd
    Owner = FABRIKAM\myAccount
    ClientIP = ::1
    IdleTimeOut = PT180.000S
    InputStreams = stdin
    OutputStreams = stdout stderr
    ShellRunTime = P0DT0H0M36S
    ShellInactivity = P0DT0H0M35S
```

Pour plus d’informations, consultez l’aide en ligne fournie par la commande suivante : **WinRM obtenir- ?**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge de plusieurs tronçons](multi-hop-support.md)
</dt> <dt>

[Gestion des quotas pour les shells distants](quotas.md)
</dt> <dt>

[Référence managée pour les commandes WS-Management PowerShell](winrm-powershell-commandlets.md)
</dt> </dl>

 

 




