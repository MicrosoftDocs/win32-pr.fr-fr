---
description: Les codes de raison de l’arrêt sont utilisés par les fonctions ExitWindowsEx et InitiateSystemShutdownEx dans le paramètre dwReason. Un nombre maximal de \_ \_ raisons pour lesquelles les codes de raison Max sont traités par le système. Le \_ nombre maximal \_ de motifs est défini dans Reason. h.
ms.assetid: db1ecee0-40eb-4761-b5d8-9cc3c1c98cdf
title: Codes de raison de l’arrêt du système (Reason. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee2b8b2795dcf350d627b3cf59f85eb374a22cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524925"
---
# <a name="system-shutdown-reason-codes"></a>Codes de raison de l’arrêt du système

Les codes de raison de l’arrêt sont utilisés par les fonctions [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) et [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) dans le paramètre *dwReason* .

Un nombre maximal de \_ \_ raisons pour lesquelles les codes de raison Max sont traités par le système. Le \_ nombre maximal \_ de motifs est défini dans Reason. h.

Les indicateurs de raison principale sont les suivants. Ils indiquent le type de problème général.



| Constante/valeur                                                                                                                                                                                                                                                                                 | Description                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_MAJOR_APPLICATION"></span><span id="shtdn_reason_major_application"></span><dl> <dt>**SHTDN \_ RAISON de l' \_ \_ application**</dt> de la plus importante <dt></dt> </dl>             | Problème de l’application.<br/>                                                                                                                                      |
| <span id="SHTDN_REASON_MAJOR_HARDWARE"></span><span id="shtdn_reason_major_hardware"></span><dl> <dt>**SHTDN \_ RAISON \_ principale du \_ matériel**</dt> <dt>0x00010000</dt> </dl>                      | Problème matériel.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_LEGACY_API"></span><span id="shtdn_reason_major_legacy_api"></span><dl> <dt>**SHTDN \_ RAISON \_ principale de l' \_ \_ API héritée**</dt> <dt>0x00070000</dt> </dl>               | La fonction [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) a été utilisée à la place de [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa).<br/> |
| <span id="SHTDN_REASON_MAJOR_OPERATINGSYSTEM"></span><span id="shtdn_reason_major_operatingsystem"></span><dl> <dt>**SHTDN \_ CAUSE \_ principale \_ OPERATINGSYSTEM**</dt> <dt>0x00020000</dt> </dl> | Problème lié au système d’exploitation.<br/>                                                                                                                                 |
| <span id="SHTDN_REASON_MAJOR_OTHER"></span><span id="shtdn_reason_major_other"></span><dl> <dt>**SHTDN \_ RAISON \_ principale \_ autre**</dt> <dt>0x00000000</dt> </dl>                               | Autre problème.<br/>                                                                                                                                            |
| <span id="SHTDN_REASON_MAJOR_POWER"></span><span id="shtdn_reason_major_power"></span><dl> <dt>**SHTDN \_ RAISON \_ principale \_**</dt> de l’alimentation <dt>0x00060000</dt> </dl>                               | Panne d’alimentation.<br/>                                                                                                                                          |
| <span id="SHTDN_REASON_MAJOR_SOFTWARE"></span><span id="shtdn_reason_major_software"></span><dl> <dt>**SHTDN \_ RAISON des \_ principaux \_ logiciels**</dt> <dt>0x00030000</dt> </dl>                      | Problème logiciel.<br/>                                                                                                                                         |
| <span id="SHTDN_REASON_MAJOR_SYSTEM"></span><span id="shtdn_reason_major_system"></span><dl> <dt>**SHTDN \_ RAISON \_ principale du \_ système**</dt> <dt>0x00050000</dt> </dl>                            | Défaillance du système.<br/>                                                                                                                                         |



Voici les indicateurs de raison mineurs. Ils modifient l’indicateur de raison principale spécifié. Vous pouvez utiliser n’importe quelle raison mineure avec n’importe quelle raison principale, mais certaines combinaisons n’ont pas de sens.



| Constante/valeur                                                                                                                                                                                                                                                                                                    | Description                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------|
| <span id="SHTDN_REASON_MINOR_BLUESCREEN"></span><span id="shtdn_reason_minor_bluescreen"></span><dl> <dt>**SHTDN \_ MOTIF \_ \_ bleu-bleu mineur**</dt> <dt>0x0000000F</dt> </dl>                                   | Événement d’incident d’écran bleu.<br/>       |
| <span id="SHTDN_REASON_MINOR_CORDUNPLUGGED"></span><span id="shtdn_reason_minor_cordunplugged"></span><dl> <dt>**SHTDN \_ RAISON \_ \_ CORDUNPLUGGED**</dt> <dt>0x0000000b</dt> </dl>                          | Débranché.<br/>                     |
| <span id="SHTDN_REASON_MINOR_DISK"></span><span id="shtdn_reason_minor_disk"></span><dl> <dt>**SHTDN \_ MOTIF \_ \_ disque secondaire**</dt> <dt>0x00000007</dt> </dl>                                                     | disque.<br/>                          |
| <span id="SHTDN_REASON_MINOR_ENVIRONMENT"></span><span id="shtdn_reason_minor_environment"></span><dl> <dt>**SHTDN \_ RAISON 0x0000000c de l' \_ \_ environnement mineur**</dt> <dt></dt> </dl>                                | Environnement.<br/>                   |
| <span id="SHTDN_REASON_MINOR_HARDWARE_DRIVER"></span><span id="shtdn_reason_minor_hardware_driver"></span><dl> <dt>**SHTDN \_ RAISON \_ du \_ \_ pilote matériel mineur**</dt> <dt>0x0000000d</dt> </dl>                   | Pilote.<br/>                        |
| <span id="SHTDN_REASON_MINOR_HOTFIX"></span><span id="shtdn_reason_minor_hotfix"></span><dl> <dt>**SHTDN \_ RAISON \_ 0x00000011 \_ correctif mineur**</dt> <dt></dt> </dl>                                               | Correction à chaud.<br/>                       |
| <span id="SHTDN_REASON_MINOR_HOTFIX_UNINSTALL"></span><span id="shtdn_reason_minor_hotfix_uninstall"></span><dl> <dt>**SHTDN \_ RAISON de la \_ \_ \_ désinstallation du correctif mineur**</dt> <dt>0x00000017</dt> </dl>                | Désinstallation des correctifs à chaud.<br/>        |
| <span id="SHTDN_REASON_MINOR_HUNG"></span><span id="shtdn_reason_minor_hung"></span><dl> <dt>**SHTDN \_ RAISON \_ du \_ blocage mineur**</dt> du <dt>0x00000005</dt> </dl>                                                     | Ne répond pas.<br/>                  |
| <span id="SHTDN_REASON_MINOR_INSTALLATION"></span><span id="shtdn_reason_minor_installation"></span><dl> <dt>**SHTDN \_ RAISON \_ de \_ l’installation mineure**</dt> <dt>0x00000002</dt> </dl>                             | Installation.<br/>                  |
| <span id="SHTDN_REASON_MINOR_MAINTENANCE"></span><span id="shtdn_reason_minor_maintenance"></span><dl> <dt>**SHTDN \_ RAISON de la \_ \_ maintenance mineure**</dt> <dt>0x00000001</dt> </dl>                                | Jour.<br/>                   |
| <span id="SHTDN_REASON_MINOR_MMC"></span><span id="shtdn_reason_minor_mmc"></span><dl> <dt>**SHTDN \_ RAISON de la 0x00000019 \_ \_ MMC mineure**</dt> <dt></dt> </dl>                                                        | Problème de MMC.<br/>                     |
| <span id="SHTDN_REASON_MINOR_NETWORK_CONNECTIVITY"></span><span id="shtdn_reason_minor_network_connectivity"></span><dl> <dt>**SHTDN \_ RAISON de la \_ \_ \_ connectivité réseau mineure**</dt> <dt>0x00000014</dt> </dl>    | Connectivité réseau<br/>          |
| <span id="SHTDN_REASON_MINOR_NETWORKCARD"></span><span id="shtdn_reason_minor_networkcard"></span><dl> <dt>**SHTDN \_ RAISON \_ \_ NETWORKCARD**</dt> <dt>0x00000009</dt> </dl>                                | Carte réseau.<br/>                  |
| <span id="SHTDN_REASON_MINOR_OTHER"></span><span id="shtdn_reason_minor_other"></span><dl> <dt>**SHTDN \_ RAISON \_ secondaire \_ autre**</dt> <dt>0x00000000</dt> </dl>                                                  | Autre problème.<br/>                   |
| <span id="SHTDN_REASON_MINOR_OTHERDRIVER"></span><span id="shtdn_reason_minor_otherdriver"></span><dl> <dt>**SHTDN \_ RAISON \_ \_ OTHERDRIVER**</dt> <dt>0x0000000E</dt> </dl>                                | Autre événement du pilote.<br/>            |
| <span id="SHTDN_REASON_MINOR_POWER_SUPPLY"></span><span id="shtdn_reason_minor_power_supply"></span><dl> <dt>**SHTDN \_ RAISON \_ du \_ \_ bloc d’alimentation secondaire**</dt> <dt>0x0000000A</dt> </dl>                            | Alimentation.<br/>                  |
| <span id="SHTDN_REASON_MINOR_PROCESSOR"></span><span id="shtdn_reason_minor_processor"></span><dl> <dt>**SHTDN \_ RAISON \_ du \_ processeur secondaire**</dt> <dt>0x00000008</dt> </dl>                                      | Processeur.<br/>                     |
| <span id="SHTDN_REASON_MINOR_RECONFIG"></span><span id="shtdn_reason_minor_reconfig"></span><dl> <dt>**SHTDN \_ RAISON de la \_ \_ reconfiguration mineure**</dt> <dt>0x00000004</dt> </dl>                                         | Reconfigurer.<br/>                   |
| <span id="SHTDN_REASON_MINOR_SECURITY"></span><span id="shtdn_reason_minor_security"></span><dl> <dt>**SHTDN \_ MOTIF \_ de \_ sécurité mineure**</dt> <dt>0x00000013</dt> </dl>                                         | Problème de sécurité.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX"></span><span id="shtdn_reason_minor_securityfix"></span><dl> <dt>**SHTDN \_ RAISON \_ \_ SECURITYFIX**</dt> <dt>0x00000012</dt> </dl>                                | Correctif de sécurité.<br/>                |
| <span id="SHTDN_REASON_MINOR_SECURITYFIX_UNINSTALL"></span><span id="shtdn_reason_minor_securityfix_uninstall"></span><dl> <dt>**SHTDN \_ REASON \_ \_ SECURITYFIX \_ désinstaller**</dt> <dt>0x00000018</dt> </dl> | Désinstallation des correctifs de sécurité.<br/> |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK"></span><span id="shtdn_reason_minor_servicepack"></span><dl> <dt>**SHTDN \_ RAISON \_ mineure de \_ SERVICEPACK**</dt> <dt>0x00000010</dt> </dl>                                | Service Pack.<br/>                  |
| <span id="SHTDN_REASON_MINOR_SERVICEPACK_UNINSTALL"></span><span id="shtdn_reason_minor_servicepack_uninstall"></span><dl> <dt>**SHTDN \_ RAISON de la \_ \_ \_ désinstallation**</dt> de <dt>0x00000016</dt> du SERVICEPACK mineur </dl> | Désinstallation du Service Pack.<br/>   |
| <span id="SHTDN_REASON_MINOR_TERMSRV"></span><span id="shtdn_reason_minor_termsrv"></span><dl> <dt>**SHTDN \_ RAISON d’un \_ \_ termsrv mineur**</dt> <dt>0x00000020</dt> </dl>                                            | Services Terminal Server.<br/>             |
| <span id="SHTDN_REASON_MINOR_UNSTABLE"></span><span id="shtdn_reason_minor_unstable"></span><dl> <dt>**SHTDN \_ RAISON de la 0x00000006 \_ \_ instable mineure**</dt> <dt></dt> </dl>                                         | Stable.<br/>                      |
| <span id="SHTDN_REASON_MINOR_UPGRADE"></span><span id="shtdn_reason_minor_upgrade"></span><dl> <dt>**SHTDN \_ RAISON de la \_ \_ mise à niveau mineure**</dt> <dt>0x00000003</dt> </dl>                                            | Mettre à niveau.<br/>                       |
| <span id="SHTDN_REASON_MINOR_WMI"></span><span id="shtdn_reason_minor_wmi"></span><dl> <dt>**SHTDN \_ RAISON de la 0x00000015 \_ \_ WMI mineure**</dt> <dt></dt> </dl>                                                        | Problème WMI.<br/>                     |



Les indicateurs facultatifs suivants fournissent des informations supplémentaires sur l’événement.



| Constante/valeur                                                                                                                                                                                                                                                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SHTDN_REASON_FLAG_USER_DEFINED"></span><span id="shtdn_reason_flag_user_defined"></span><dl> <dt>**SHTDN \_ \_Indicateur de \_ raison \_ défini par l’utilisateur**</dt> <dt>0x40000000</dt> </dl> | Le code de raison est défini par l’utilisateur. Pour plus d’informations, consultez Définition d’un code de raison personnalisé. <br/> Si cet indicateur n’est pas présent, le code de raison est défini par le système.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SHTDN_REASON_FLAG_PLANNED"></span><span id="shtdn_reason_flag_planned"></span><dl> <dt>**SHTDN \_ Indicateur de raison \_ \_ planifié**</dt> <dt>0x80000000</dt> </dl>                 | L’arrêt a été planifié. Le système génère un fichier de données d’État du système (SSD). Ce fichier contient des informations sur l’état du système, telles que les processus, les threads, l’utilisation de la mémoire et la configuration. <br/> Si cet indicateur n’est pas présent, l’arrêt n’a pas été planifié. Les options de notification et de rapport sont contrôlées par un ensemble de stratégies. Par exemple, après la connexion, le système affiche une boîte de dialogue signalant l’arrêt non planifié si la stratégie a été activée. Un fichier SSD est créé uniquement si la stratégie de disque SSD est activée sur le système. L’administrateur peut utiliser [rapport d’erreurs Windows](../wer/windows-error-reporting.md) pour envoyer les données SSD à un emplacement central ou à Microsoft.<br/> |



## <a name="remarks"></a>Notes

Les combinaisons suivantes sont reconnues par le système. Le tableau indique la chaîne qui s’affiche dans le moniteur d’événements de mise hors tension et fournit une description plus détaillée. La chaîne par défaut est « aucun titre pour cette raison n’a été trouvé ».



| Combinaison                                                                                                | Description                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_raison SHTDN \_ principale \_ application \| SHTDN \_ motif \_ de \_ blocage mineur                                            | « Application : non réactive » un redémarrage ou un arrêt non planifié pour dépanner une application qui ne répond pas.<br/>                                                                                                                             |
| SHTDN \_ raison \_ principale \_ application \| SHTDN \_ raison de \_ l’installation mineure d’un \_ indicateur de \| \_ motif SHTDN \_ \_ planifié    | « Application : installation (planifiée) » un redémarrage ou un arrêt planifié pour effectuer l’installation de l’application.<br/>                                                                                                                              |
| SHTDN \_ raison \_ principale \_ application \| SHTDN \_ raison de la \_ maintenance mineure \_                                     | « Application : maintenance (non planifiée) » un redémarrage ou un arrêt non planifié pour traiter une application.<br/>                                                                                                                                    |
| SHTDN \_ raison \_ principale \_ application \| SHTDN \_ motif \_ mineur \_ maintenance \| SHTDN \_ motif de raison \_ \_ planifiée     | « Application : maintenance (planifiée) » un redémarrage ou un arrêt planifié pour effectuer une maintenance planifiée sur une application.<br/>                                                                                                                  |
| SHTDN \_ raison \_ principale \_ application \| SHTDN \_ raison \_ mineure \_ instable                                        | « Application : instable » un redémarrage ou un arrêt non planifié pour dépanner une application instable.<br/>                                                                                                                                     |
| SHTDN \_ raison \_ principale du \_ matériel \| SHTDN raison de \_ \_ \_ l’installation mineure                                       | « Matériel : installation (non planifiée) » un redémarrage ou un arrêt non planifié pour commencer ou terminer l’installation matérielle.<br/>                                                                                                                     |
| SHTDN \_ raison \_ principale \_ matérielle \| SHTDN \_ raison \_ de \_ l’installation mineure de l’indicateur de \| \_ motif SHTDN \_ \_ planifié       | « Matériel : installation (planifiée) » un redémarrage ou un arrêt planifié pour démarrer ou terminer l’installation matérielle.<br/>                                                                                                                          |
| SHTDN \_ raison \_ principale du \_ matériel \| SHTDN motif de \_ \_ maintenance mineure \_                                        | « Matériel : maintenance (non planifiée) » un redémarrage ou un arrêt non planifié pour le matériel de service sur le système.<br/>                                                                                                                               |
| SHTDN \_ raison \_ principale \_ matérielle \| SHTDN \_ raison de la \_ maintenance mineure de \_ SHTDN raison de l' \| \_ \_ indicateur \_ planifié        | « Matériel : maintenance (planifiée) » un redémarrage ou un arrêt planifié pour le matériel de service sur le système.<br/>                                                                                                                                    |
| SHTDN \_ raison de l' \_ \_ API héritée principale \_                                                                          | « Arrêt de l’API héritée » cet arrêt a été initié par la fonction [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna) héritée. Les applications doivent utiliser la fonction [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) .<br/> |
| SHTDN \_ cause \_ principale \_ OPERATINGSYSTEM \| SHTDN \_ motif \_ \_ correctif mineur                                      | « Système d’exploitation : correctif à chaud (non planifié) » un redémarrage ou un arrêt non planifié pour installer un correctif.<br/>                                                                                                                                        |
| SHTDN \_ cause \_ majeure \_ OPERATINGSYSTEM \| SHTDN \_ motif \_ mineur \_ correctif \| SHTDN \_ raison de l' \_ indicateur \_ planifié      | « Système d’exploitation : correctif logiciel (planifié) » un redémarrage ou un arrêt planifié pour installer un correctif.<br/>                                                                                                                                             |
| SHTDN \_ cause \_ principale \_ OPERATINGSYSTEM \| SHTDN \_ raison de la \_ \_ reconfiguration mineure                                    | « Système d’exploitation : reconfiguration (non planifiée) » un redémarrage ou un arrêt non planifié pour modifier la configuration du système d’exploitation.<br/>                                                                                                        |
| SHTDN \_ cause \_ principale \_ OPERATINGSYSTEM \| SHTDN \_ motif de la \_ reconfiguration mineure de \_ \| SHTDN \_ motif de raison \_ \_ planifiée    | « Système d’exploitation : reconfiguration (planifié) » un redémarrage ou un arrêt planifié pour modifier la configuration du système d’exploitation.<br/>                                                                                                             |
| SHTDN \_ cause \_ principale \_ OPERATINGSYSTEM \| SHTDN \_ motif \_ mineur \_ SECURITYFIX                                 | « Système d’exploitation : correctif de sécurité (non planifié) » un redémarrage ou un arrêt non planifié pour installer un correctif de sécurité.<br/>                                                                                                                            |
| SHTDN \_ raison \_ principale \_ OPERATINGSYSTEM \| SHTDN \_ raison de l' \_ \_ indicateur mineur SECURITYFIX \| SHTDN \_ motif \_ \_ | « Système d’exploitation : correctif de sécurité (planifié) » un redémarrage ou un arrêt planifié pour installer un correctif de sécurité.<br/>                                                                                                                                 |
| SHTDN \_ raison \_ principale \_ OPERATINGSYSTEM \| SHTDN \_ raison de l' \_ \_ \| \_ indicateur de \_ raison \_ | « Système d’exploitation : Service Pack (planifié) » un redémarrage ou un arrêt planifié pour installer un Service Pack.<br/>                                                                                                                                   |
| SHTDN \_ cause \_ principale \_ OPERATINGSYSTEM \| SHTDN \_ motif de la \_ mise à niveau mineure d’un \_ indicateur de \| \_ raison SHTDN \_ \_ planifié     | « Système d’exploitation : mise à niveau (planifiée) » un redémarrage ou un arrêt planifié pour mettre à niveau la configuration du système d’exploitation.<br/>                                                                                                                    |
| SHTDN \_ raison \_ principale \_ autre \| SHTDN \_ motif \_ mineur \_ autre                                                 | « Autre (non planifié) » un arrêt ou un redémarrage non planifié.<br/>                                                                                                                                                                                 |
| SHTDN \_ raison \_ principale \_ autre \| SHTDN \_ motif \_ mineur \_ autre \| SHTDN \_ raison de l' \_ indicateur \_ planifié                 | « Autre (planifié) » un arrêt ou un redémarrage planifié.<br/>                                                                                                                                                                                      |
| SHTDN \_ raison \_ principale \_ autre \| SHTDN \_ motif \_ mineur \_ suspendu                                                  | « Autre échec : le système ne répond pas » le système ne répond pas.<br/>                                                                                                                                                                  |
| SHTDN raison principale de la SHTDN de la raison de l' \_ \_ \_ énergie \| \_ \_ mineure \_ CORDUNPLUGGED                                         | « Panne d’alimentation : cordon débranché » l’ordinateur a été débranché.<br/>                                                                                                                                                                           |
| SHTDN \_ raison \_ principale de l' \_ alimentation \| SHTDN \_ motif \_ mineur \_                                           | « Panne d’alimentation : environnement » une panne d’alimentation s’est produite.<br/>                                                                                                                                                                                |
| SHTDN \_ raison \_ principale du \_ système \| SHTDN \_ motif bleu- \_ \_ bleu mineur                                           | « Défaillance du système : erreur d’arrêt » l’ordinateur affichait un événement d’incident d’écran bleu.<br/>                                                                                                                                                        |
| SHTDN \_ raison \_ principale \_ système \| SHTDN \_ raison de la \_ \_ connectivité réseau mineure \_                                | « Perte de connectivité réseau (non planifiée) » l’ordinateur doit être arrêté en raison d’un problème de connectivité réseau.<br/>                                                                                                                    |
| SHTDN \_ raison \_ principale \_ système \| SHTDN \_ motif \_ sécurité mineure \_                                             | « Problème de sécurité », l’ordinateur doit être arrêté en raison d’un problème de sécurité.<br/>                                                                                                                                                          |



 

Vous pouvez également définir vos propres raisons d’arrêt et les ajouter au registre. Chaque code de raison doit être stocké sous la forme d’une valeur de Registre dans la clé suivante :**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ FIABILITE \\ UserDefined \\<ID de langue par défaut du \_ système \_ \_>**

Cette clé contient des noms de valeur de la forme suivante : *xxxxx*; *nnn*; *nnnnn*. Les points-virgules délimitent les composants d’un nom de valeur.

<dl> <dt>

<span id="xxxxx"></span><span id="XXXXX"></span>*xxxxx*
</dt> <dd>

Un à cinq des indicateurs de contrôle suivants (aucun autre caractère ne peut être utilisé).



| Indicateur | Description                                                                                       |
|------|---------------------------------------------------------------------------------------------------|
| P    | Arrêt planifié ; dans le cas contraire, un arrêt non planifié.                                               |
| C    | Un commentaire est requis. Cet indicateur doit être utilisé avec les.<br/>                                  |
| B    | Un ID est requis. Cet indicateur doit être utilisé avec D.<br/>                                      |
| S    | Affiche la boîte de dialogue arrêt attendu. Les options S, D, ou les deux et D doivent être utilisées.<br/>   |
| D    | Affiche la boîte de dialogue arrêt inattendu. Les options S, D, ou les deux et D doivent être utilisées.<br/> |



 

L’ordre dans lequel les indicateurs sont utilisés n’a pas d’importance. Par exemple, CSP indique un arrêt planifié où la boîte de dialogue d’arrêt attendue s’affiche et un commentaire est nécessaire.

</dd> <dt>

<span id="nnn"></span><span id="NNN"></span>*nnn*
</dt> <dd>

Raison principale. Ce composant doit être un nombre compris dans la plage 64-255. La plage 0-63 est réservée à une utilisation par le système.

</dd> <dt>

<span id="nnnnn"></span><span id="NNNNN"></span>*nnnnn*
</dt> <dd>

Raison mineure. Ce composant doit se trouver dans la plage 0-65535.

</dd> </dl>

Les raisons personnalisées sont triées dans l’interface utilisateur par le numéro de raison principale, puis par le numéro de raison mineur. Deux raisons personnalisées ne peuvent pas utiliser les mêmes raisons majeures et secondaires, sauf si l’une d’elles est planifiée et l’autre non planifiée. Dans le cas contraire, le système utilisera la première instance et ignorera les autres.

Les données de chaque valeur de Registre sont deux chaînes séparées par \\ n \\ r. La première chaîne est une chaîne de titre à afficher dans la boîte de dialogue d’arrêt et écrite dans le journal des événements. La taille maximale est de 64 caractères. Les chaînes de titre doivent être uniques. Les titres personnalisés ne peuvent pas correspondre aux titres standard définis par le système, ou à un autre titre personnalisé. La deuxième chaîne est une chaîne de description à afficher dans la boîte de dialogue d’arrêt. elle est facultative. La taille maximale est de 256 caractères.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP- \[ \| applications UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ \| apps UWP\]<br/>                         |
| En-tête<br/>                   | <dl> <dt>Raison. h</dt> </dl> |



 

 
