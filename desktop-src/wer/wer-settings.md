---
title: Paramètres des Rapports d’erreurs Windows
description: Paramètres pour personnaliser l’expérience de signalement des problèmes. Tous ces paramètres peuvent être définis à l’aide de stratégie de groupe. certains peuvent également être modifiés dans le centre de maintenance pour Windows 7 et Windows 8. pour Windows 10, utilisez la fonction de recherche dans Paramètres pour rechercher afficher les paramètres système avancés.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Windows Rapport d’erreurs Windows de rapport d’erreurs, paramètres
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 4586c4f282cbc5c4e2f683c0764eac048f6c05d22a1972cb0ceb84f9699c7925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118442228"
---
# <a name="wer-settings"></a>Paramètres des Rapports d’erreurs Windows

Rapport d’erreurs Windows (WER) fournit de nombreux paramètres pour personnaliser l’expérience de signalement des problèmes. Tous ces paramètres peuvent être définis à l’aide de stratégie de groupe. certains peuvent également être modifiés dans le **centre de maintenance** pour Windows 7 et Windows 8. pour Windows 10, utilisez la fonction de recherche dans Paramètres pour rechercher **afficher les paramètres système avancés**. Les paramètres WER se trouvent dans l’une des sous-clés de Registre suivantes :

-   **HKEY \_ logiciel \_ utilisateur actuel** \\  \\ **Microsoft** \\ **Windows** \\ **Rapport d’erreurs Windows**
-   **HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** \\ **Rapport d’erreurs Windows**

## <a name="windows-error-reporting-subkey"></a>sous-clé Rapport d’erreurs Windows

<dl> <dt>

<span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>

0-désactiver la limitation de contournement de données. Si le contournement est désactivé ou n’est pas configuré en tant que paramètre de stratégie, WER limite les données par défaut. WER ne télécharge pas plus d’un fichier CAB pour un rapport qui contient des données sur les mêmes types d’événements.

</dd> <dd>

1-activer la limitation de contournement des données. WER ne limite pas les données. WER télécharge des fichiers CAB supplémentaires qui peuvent contenir des données sur les mêmes types d’événements qu’un rapport téléchargé précédemment.

</dd> </dl>

Indique s’il faut activer le contournement de la limitation des données du client WER

</dd> <dt>

<span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>1-paramètres uniquement (valeur par défaut sur Windows 7)</dd> <dd>2-toutes les données (par défaut sur Windows Vista)</dd> </dl>

Indique s’il faut archiver les paramètres uniquement ou toutes les données

</dd> <dt>

<span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**DefaultConsent de consentement \\**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>1-toujours demander (par défaut)</dd> <dd>2-paramètres uniquement</dd> <dd>3-paramètres et données sécurisées</dd> <dd>4-toutes les données</dd> </dl>

Choix de consentement par défaut

</dd> <dt>

<span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**DefaultOverrideBehavior de consentement \\**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>0-le consentement vertical remplace le consentement par défaut (par défaut)</dd> <dd>1-le consentement par défaut remplacera le consentement propre à l’application</dd> </dl>

Indique si le consentement par défaut remplace le consentement vertical

</dd> <dt>

<span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**VerticalName de consentement \\ \[\]**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>1-toujours demander (par défaut)</dd> <dd>2-paramètres uniquement</dd> <dd>3-paramètres et données sécurisées</dd> <dd>4-toutes les données</dd> </dl>

Choix du consentement pour le plug-in WER

</dd> <dt>

<span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**
</dt> <dd>

**SZ de REG \_**

Chemin d’accès au répertoire

Répertoire cible sur le serveur

</dd> <dt>

<span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**
</dt> <dd>

**\_valeur DWORD reg**

Le numéro de port

Numéro de port à utiliser avec le serveur d’entreprise

</dd> <dt>

<span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**
</dt> <dd>

**SZ de REG \_**

Le nom du serveur

Nom du serveur d’entreprise

</dd> <dt>

<span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>0-non (valeur par défaut)</dd> <dd>1 - Oui</dd> </dl>

indique s’il faut utiliser l’authentification Windows intégrée

</dd> <dt>

<span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>0-non (valeur par défaut)</dd> <dd>1 - Oui</dd> </dl>

Indique s’il faut utiliser SSL

</dd> <dt>

<span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications \\ \[ exeName \] (remplacez « \[ exeName \] » par le nom réel d’un fichier .exe, par exemple, « notepad.exe »)**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :

<dl> <dd>0-les processus avec un nom d’image exécutable de **\[ exeName \]** ne nécessitent pas que l’utilisateur choisisse **Déboguer** ou **Continuer** (par défaut)</dd> <dd>1-les processus avec un nom d’image exécutable de **\[ exeName \]** obligent l’utilisateur à choisir **Déboguer** ou **Continuer**</dd> </dl> </dd> <dt>

<span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications \\ \* (" \* " est le nom de la valeur littérale)**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :

<dl> <dd>0-tous les processus à l’exception de ceux spécifiés explicitement dans le paramètre **DebugApplications \\ \[ \] exeName** ne nécessitent pas que l’utilisateur choisisse **Debug** ou **continue** (valeur par défaut)</dd> <dd>1-tous les processus à l’exception de ceux spécifiés explicitement dans le paramètre **DebugApplications \\ \[ exeName \]** obligent l’utilisateur à choisir **Déboguer** ou **Continuer**</dd> </dl> </dd> <dt>

<span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>0 - Activé</dd> <dd>1 - Désactivé</dd> </dl>

Activer ou désactiver l’archive

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Activée**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>0-activé (valeur par défaut)</dd> <dd>1 - Désactivé</dd> </dl>

Activer ou désactiver le WER

</dd> <dt>

<span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>0 - Activé</dd> <dd>1 - Désactivé</dd> </dl>

Activer ou désactiver la mise en file d’attente de rapports

</dd> <dt>

<span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>0-UI (valeur par défaut)</dd> <dd>1-aucune interface utilisateur</dd> </dl>

Activer ou désactiver l’interface utilisateur WER

</dd> <dt>

<span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>0-envoyer (par défaut)</dd> <dd>1-ne pas envoyer</dd> </dl>

Indique s’il faut empêcher l’envoi de données de second niveau

</dd> <dt>

<span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**Nom de l' \\ \[ application ExcludedApplications\]**
</dt> <dd>

**SZ de REG \_**

Utiliser [ **WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)

Liste des applications exclues

</dd> <dt>

<span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>0-non (valeur par défaut)</dd> <dd>1 - Oui</dd> </dl>

Indique si tous les rapports doivent être envoyés à la file d’attente de l’utilisateur

</dd> <dt>

<span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps \\ DumpFolder** ou **LocalDumps nom de l' \\ \[ application \] \\ DumpFolder**
</dt> <dd>

**REG \_ développer \_ SZ**

Chemin d'accès du répertoire. La valeur par défaut est% LOCALAPPDATA% \\ CrashDumps. Si la valeur par défaut n’est pas utilisée, l’application doit s’assurer que le dossier possède un ACL suffisant.

**Windows Vista :** Les valeurs de Registre sous la clé **LocalDumps** ne sont pas prises en charge. notez que ce comportement a changé avec Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1).

Chemin d’accès où les fichiers de vidage doivent être stockés.

Notez que les paramètres par processus remplacent tous les paramètres globaux qui existent pour plus d’informations, consultez [collecte des vidages de User-Mode](collecting-user-mode-dumps.md).

Ce paramètre n’est pas pris en charge dans la ruche de Registre **HKEY \_ Current \_ User** .

</dd> <dt>

<span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps \\ DumpCount** ou **LocalDumps nom de l' \\ \[ application \] \\ DumpCount**
</dt> <dd>

**\_valeur DWORD reg**

Nombre maximal. La valeur par défaut est de 10. Lorsque la valeur maximale est dépassée, le fichier de vidage le plus ancien dans le dossier sera remplacé par le nouveau fichier de vidage.

**Windows Vista :** Les valeurs de Registre sous la clé **LocalDumps** ne sont pas prises en charge. notez que ce comportement a changé avec Windows Server 2008 et Windows Vista avec SP1.

Nombre maximal de fichiers de vidage dans le dossier.

Ce paramètre n’est pas pris en charge dans la ruche de Registre **HKEY \_ Current \_ User** .

</dd> <dt>

<span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps \\ DumpType** ou **LocalDumps nom de l' \\ \[ application \] \\ DumpType**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>0-vidage personnalisé</dd> <dd>1-Minidump (par défaut)</dd> <dd>2-vidage complet</dd> </dl>

**Windows Vista :** Les valeurs de Registre sous la clé **LocalDumps** ne sont pas prises en charge. notez que ce comportement a changé avec Windows Server 2008 et Windows Vista avec SP1.

Type de vidage.

Ce paramètre n’est pas pris en charge dans la ruche de Registre **HKEY \_ Current \_ User** .

</dd> <dt>

<span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps \\ CustomDumpFlags** ou **LocalDumps nom de l' \\ \[ application \] \\ CustomDumpFlags**
</dt> <dd>

**\_valeur DWORD reg**

Une ou plusieurs valeurs de l’énumération de [**\_ type Minidump**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) . La valeur par défaut est {**MiniDumpWithDataSegs** \| **MiniDumpWithUnloadedModules** \| **MiniDumpWithProcessThreadData**}.

**Windows Vista :** Les valeurs de Registre sous la clé **LocalDumps** ne sont pas prises en charge. notez que ce comportement a changé avec Windows Server 2008 et Windows Vista avec SP1.

Options de vidage personnalisées à utiliser. Cette valeur est utilisée uniquement lorsque **DumpType** a la valeur 0.

Ce paramètre n’est pas pris en charge dans la ruche de Registre **HKEY \_ Current \_ User** .

</dd> <dt>

<span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**
</dt> <dd>

**\_valeur DWORD reg**

Valeurs possibles :<dl> <dd>0 – activé (valeur par défaut)</dd> <dd>1 – désactivé</dd> </dl>

Activer ou désactiver la journalisation

</dd> <dt>

<span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**
</dt> <dd>

**\_valeur DWORD reg**

Plage de valeurs possibles : 1 – 5000. La valeur par défaut est 1000.

Taille maximale de l’archive, dans les fichiers

</dd> <dt>

<span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**
</dt> <dd>

**\_valeur DWORD reg**

Plage de valeurs possibles : 1 à 500. La valeur par défaut est de 50.

Taille maximale de la file d’attente

</dd> <dt>

<span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**
</dt> <dd>

**\_valeur DWORD reg**

Nombre de jours

Intervalle entre les rappels à l’utilisateur pour rechercher des solutions, en jours

</dd> <dt>

<span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules ! \[ nom de pwszOutOfProcessCallbackDll incluant le chemin d’accès\]**
</dt> <dd>

**\_valeur DWORD reg**

Le contenu de la valeur est ignoré.

Le nom de la valeur est utilisé pour extraire la valeur pwszOutOfProcessCallbackDll.

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Cette valeur de Registre n’est pas prise en charge.

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a>rapports du noyau en temps réel WER Paramètres

Les paramètres des rapports du noyau en direct de WER, décrits ci-après, se trouvent tous deux dans la sous-clé de Registre suivante :

-   **HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local CrashControl

## <a name="fulllivekernelreports-subkey"></a>Sous-clé FullLiveKernelReports

<dl> <dt>

<span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**
</dt> <dd>

**\_valeur DWORD reg**

Seuil (en heures) de la fréquence à laquelle un seul composant peut créer un vidage dynamique complet. Cette valeur doit être supérieure ou égale à **SystemThrottleThreshold**. La définition de la valeur zéro (0) désactivera toutes les limitations temporelles. La valeur par défaut est 168 (7 jours).

</dd> <dt>

<span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**
</dt> <dd>

**\_valeur DWORD reg**

Nombre maximal de dumps dynamiques complets qui peuvent se trouver sur le disque à un moment donné. La valeur par défaut est 1. Si vous définissez cette valeur sur zéro (0), la fonctionnalité de vidage dynamique est désactivée.

</dd> <dt>

<span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**
</dt> <dd>

**\_q QWord**

[SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) indiquant la dernière heure de rapport dynamique complète, pour le système ou un ReportType spécifique. Utilisé pour déterminer si un seuil de stratégie a été respecté.

</dd> <dt>

<span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**
</dt> <dd>

**\_valeur DWORD reg**

Seuil (en heures) de la fréquence à laquelle un composant sur le système peut créer un vidage dynamique complet. La valeur par défaut est 120 (5 jours).

</dd> </dl>

## <a name="livekernelreports-subkey"></a>Sous-clé LiveKernelReports

<dl> <dt>

<span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**
</dt> <dd>

**SZ de REG \_**


Emplacement de stockage Redirigé des rapports de noyau en direct. L’emplacement par défaut est%systemroot%\LiveKernelReports. Cette valeur doit être un chemin d’accès valide. Le chemin d’accès doit être au format de chemin d’accès NT. Par exemple, \? ? \c : \LiveDumpsFolder.  pour plus d’informations sur les formats de chemin d’accès, consultez [formats de chemin de fichier sur les systèmes de Windows](/dotnet/standard/io/file-path-formats).

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence WER](wer-reference.md)
</dt> </dl>

 

 
