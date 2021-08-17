---
title: Schtasks.exe
description: Permet à un administrateur de créer, supprimer, interroger, modifier, exécuter et terminer des tâches planifiées sur un ordinateur local ou distant.
ms.assetid: 3cf973de-14c4-4ca9-86a7-7f97181bd9e0
keywords:
- Schtasks.exe Planificateur de tâches
topic_type:
- apiref
api_name:
- Schtasks.exe
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 0da33bf63d999ddad42f58dfa15a1c36571a664855ac20e48ef43bfd7aecd55b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139382"
---
# <a name="schtasksexe"></a>Schtasks.exe

Permet à un administrateur de créer, supprimer, interroger, modifier, exécuter et terminer des tâches planifiées sur un ordinateur local ou distant. L’exécution de Schtasks.exe sans arguments affiche l’État et l’heure de la prochaine exécution pour chaque tâche inscrite. 

Pour plus d’informations sur Planificateur de tâches, consultez l’introduction suivante : [Planificateur de tâches pour les développeurs](task-scheduler-start-page.md).

## <a name="creating-a-task"></a>Création d’une tâche

La syntaxe suivante est utilisée pour créer une tâche sur l’ordinateur local ou distant.

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

### <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span> **Système** /s
</dt> <dd>

Valeur qui spécifie l’ordinateur distant auquel se connecter. En cas d’omission, le paramètre système est défini par défaut sur l’ordinateur local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nom d’utilisateur**
</dt> <dd>

Valeur qui spécifie le contexte utilisateur sous lequel Schtasks.exe doit s’exécuter.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ mot \] de passe**
</dt> <dd>

Valeur qui spécifie le mot de passe pour un contexte utilisateur donné. En cas d’omission, Schtasks.exe invite l’utilisateur à entrer des données.

</dd> <dt>

<span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span> **Nom d’utilisateur** /ru
</dt> <dd>

Valeur qui spécifie le contexte utilisateur sous lequel la tâche s’exécute. Pour le compte système, les valeurs valides sont « », «NT AUTHORITY \\ System » ou « System ». Pour les tâches Planificateur de tâches 2,0, « NT AUTHORITY \\ LOCALSERVICE » et « NT Authority \\ NetworkService » sont également des valeurs valides.

</dd> <dt>

<span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[ mot_de_passe \]**
</dt> <dd>

Valeur qui spécifie le mot de passe de l’utilisateur spécifié avec le paramètre/RU. Pour demander le mot de passe, la valeur doit être « \* » ou aucune valeur. Ce mot de passe est ignoré pour le compte système. Ce paramètre doit être combiné avec le commutateur/RU ou/XML.

</dd> <dt>

<span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** **planification**
</dt> <dd>

Valeur qui spécifie la fréquence de planification. Les valeurs valides sont : MINUTE, heure, quotidien, hebdomadaire, mensuelle, ONCE, ONLOGON, ONIDLE et ONEVENT.

</dd> <dt>

<span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**/Mo** ( **modificateur** )
</dt> <dd>

Valeur qui affine le type de planification pour permettre un contrôle plus fin de la périodicité de la planification. Les valeurs autorisées sont :

-   MINUTE : 1-1439 minutes.
-   Toutes les heures : 1-23 heures.
-   QUOTIDIENNE : 1-365 jours.
-   HEBDOMADAIRE : semaines 1-52.
-   UNE fois : aucun modificateur.
-   ONSTARt : aucun modificateur.
-   ONLOGON : aucun modificateur.
-   ONIDLE : aucun modificateur.
-   MENSUELLE : 1-12 ou premier, deuxième, troisième, quatrième, dernier et LASTDAY.
-   ONEVENT : chaîne de requête d’événement XPath.

</dd> <dt>

<span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **jours**
</dt> <dd>

Valeur qui spécifie le jour de la semaine où exécuter la tâche. Les valeurs valides sont les suivantes : Lun, Mar, WED, Thou, Ven, SAT, SUN et pour les planifications MENSUELles 1-31 (jours du mois). Le caractère générique ( \* ) spécifie tous les jours.

</dd> <dt>

<span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **mois**
</dt> <dd>

Valeur qui spécifie les mois de l’année. La valeur par défaut est le premier jour du mois. Les valeurs valides sont les suivantes : JAN, fév, MAR, APR, mai, JUN, JUL, aoû, SEP, OCT, NOV et DEC. Le caractère générique ( \* ) spécifie tous les mois.

</dd> <dt>

<span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **IdleTime**
</dt> <dd>

Valeur qui spécifie la durée d’inactivité en attente avant l’exécution d’une tâche ONIDLE planifiée. La plage valide est de 1-999 minutes.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nom_tâche**
</dt> <dd>

Valeur qui spécifie un nom qui identifie de façon unique la tâche planifiée.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **exécution_tâche**
</dt> <dd>

Valeur qui spécifie le chemin d’accès et le nom de fichier de la tâche à exécuter à l’heure planifiée. par exemple : C : \\ Windows \\ System32 \\calc.exe.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**
</dt> <dd>

Valeur qui spécifie l’heure de début de l’exécution de la tâche. Le format de l’heure est HH : mm (24 heures). Par exemple, 14:30 spécifie 2:30. La valeur par défaut est l’heure actuelle:/ST n’est pas spécifié. Cette option est requise pour l’argument/SC ONCE.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **intervalle**
</dt> <dd>

Valeur qui spécifie l’intervalle de répétition en minutes. Cela ne s’applique pas aux types de planification suivants : MINUTE, HOURly, ONSTARt, ONLOGON, ONIDLE et ONEVENT. La plage valide est de 1-599940 minutes. Si les paramètres/ET ou/DU sont spécifiés, la valeur par défaut est 10 minutes.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **heure_fin**
</dt> <dd>

Valeur qui spécifie l’heure de fin de l’exécution de la tâche. Le format de l’heure est HH : mm (24 heures). Par exemple, 14:50 spécifie 2:50PM. Cela ne s’applique pas aux types de planification suivants : ONSTARt, ONLOGON, ONIDLE et ONEVENT.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span> **Durée** /du
</dt> <dd>

Valeur qui spécifie la durée d’exécution de la tâche. Le format de l’heure est HH : mm (24 heures). Par exemple, 14:50 spécifie 2:50PM. Cela ne s’applique pas à/ET et aux types de planification suivants : ONSTARt, ONLOGON, ONIDLE et ONEVENT. Pour les tâches/v1 (tâches Planificateur de tâches 1,0), si/RI est spécifié, la durée par défaut est d’une heure.

**Windows XP :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/K** 
</dt> <dd>

Valeur qui termine la tâche à l’heure de fin ou de la durée. Cela ne s’applique pas aux types de planification suivants : ONSTARt, ONLOGON, ONIDLE et ONEVENT. Vous devez spécifier/ET ou/DU.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **DateDébut**
</dt> <dd>

Valeur qui spécifie la première date à laquelle la tâche doit être exécutée. Le format est mm/jj/aaaa. La valeur par défaut est la date actuelle. Cela ne s’applique pas aux types de planification suivants : ONCE, ONSTARt, ONLOGON, ONIDLE et ONEVENT.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**
</dt> <dd>

Valeur qui spécifie la dernière date à laquelle la tâche s’exécutera. Le format est mm/jj/aaaa. Cela ne s’applique pas aux types de planification suivants : ONCE, ONSTARt, ONLOGON, ONIDLE et ONEVENT.

</dd> <dt>

<span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/Ce** **ChannelName**
</dt> <dd>

Valeur qui spécifie le canal d’événement pour les déclencheurs ONEVENT.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Valeur qui permet à la tâche de s’exécuter de manière interactive uniquement si l’utilisateur/RU est actuellement connecté au moment de l’exécution de la tâche. La tâche s’exécute uniquement si l’utilisateur a ouvert une session.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_NP_"></span><span id="_np_"></span>**/NP** 
</dt> <dd>

Valeur qui indique qu’aucun mot de passe n’est stocké. La tâche ne s’exécute pas de manière interactive en tant qu’utilisateur donné. Seules les ressources locales sont disponibles.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**Z** 
</dt> <dd>

Valeur qui marque la tâche à supprimer après sa dernière exécution.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **xmlfile**
</dt> <dd>

Valeur qui crée une tâche à partir d’un fichier XML. Ce paramètre peut être combiné avec les commutateurs/RU et/RP, ou avec le commutateur/RP seul lorsque le fichier XML de la tâche contient déjà le principal.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_V1_"></span><span id="_v1_"></span>**/V1** 
</dt> <dd>

valeur qui crée une tâche visible pour les plateformes Windows 2000, Windows Server 2003 et Windows XP.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/F** 
</dt> <dd>

Valeur qui force la création de la tâche et supprime les avertissements si la tâche spécifiée existe déjà.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Niveau** /RL
</dt> <dd>

Valeur qui définit le niveau d’exécution de la tâche. Les valeurs valides sont LIMITED et HIGHEST. La valeur par défaut est LIMITED.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **DelayTime**
</dt> <dd>

Valeur qui spécifie le temps d’attente pour retarder la tâche après le déclenchement du déclencheur. Le format de l’heure est mmmm : SS. Cette option est valide uniquement pour les types de planification ONSTARt, ONLOGON et ONEVENT.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Valeur qui affiche le message d’aide pour Schtasks.exe.

</dd> </dl>

## <a name="remarks"></a>Remarques

lorsque vous créez une tâche sur un ordinateur distant qui exécute le système d’exploitation Windows XP, Windows Server 2003 ou Windows 2000, utilisez le commutateur/V1

Vous ne pouvez pas créer une tâche de Planificateur de tâches à distance non interactive 1,0 (créez une tâche en n’utilisant pas le commutateur/IT et en utilisant le commutateur/v1) si l’exception de pare-feu de partage de fichiers et d’imprimantes est activée sur l’ordinateur distant et que l’exception de pare-feu de gestion des tâches planifiées distantes est désactivée.

## <a name="deleting-a-task"></a>Suppression d’une tâche

La syntaxe suivante est utilisée pour supprimer une ou plusieurs tâches planifiées.

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

### <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span> **Système** /s
</dt> <dd>

Valeur qui spécifie l’ordinateur distant auquel se connecter. En cas d’omission, le paramètre système est défini par défaut sur l’ordinateur local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nom d’utilisateur**
</dt> <dd>

Valeur qui spécifie le contexte utilisateur sous lequel Schtasks.exe doit s’exécuter.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ mot \] de passe**
</dt> <dd>

Valeur qui spécifie le mot de passe pour le contexte utilisateur donné. En cas d’omission, Schtasks.exe invite l’utilisateur à entrer des données.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nom_tâche**
</dt> <dd>

Valeur qui spécifie le nom de la tâche planifiée à supprimer. Le caractère générique ( \* ) peut être utilisé pour supprimer toutes les tâches.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/F** 
</dt> <dd>

Valeur qui supprime la tâche de force et supprime les avertissements si la tâche spécifiée est en cours d’exécution.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valeur qui affiche l’aide pour Schtasks.exe.

</dd> </dl>

## <a name="running-a-task"></a>Exécution d’une tâche

La syntaxe suivante est utilisée pour exécuter immédiatement une tâche planifiée.

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span> **Système** /s
</dt> <dd>

Valeur qui spécifie l’ordinateur distant auquel se connecter. En cas d’omission, le paramètre système est défini par défaut sur l’ordinateur local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nom d’utilisateur**
</dt> <dd>

Valeur qui spécifie le contexte utilisateur sous lequel Schtasks.exe doit s’exécuter.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ mot \] de passe**
</dt> <dd>

Valeur qui spécifie le mot de passe pour le contexte utilisateur donné. En cas d’omission, Schtasks.exe invite l’utilisateur à entrer des données.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nom_tâche**
</dt> <dd>

Valeur qui spécifie le nom de la tâche planifiée à exécuter.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valeur qui affiche l’aide pour Schtasks.exe.

</dd> </dl>

## <a name="ending-a-running-task"></a>Fin d’une tâche en cours d’exécution

La syntaxe suivante est utilisée pour arrêter une tâche planifiée en cours d’exécution.

> [!Note]  
> Pour arrêter l’exécution d’une tâche à distance, assurez-vous que le partage de fichiers et d’imprimantes et les exceptions de pare-feu de gestion à distance des tâches planifiées sont activés sur l’ordinateur distant.

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span> **Système** /s
</dt> <dd>

Valeur qui spécifie l’ordinateur distant auquel se connecter. En cas d’omission, le paramètre système est défini par défaut sur l’ordinateur local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nom d’utilisateur**
</dt> <dd>

Valeur qui spécifie le contexte utilisateur sous lequel Schtasks.exe doit s’exécuter.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ mot \] de passe**
</dt> <dd>

Valeur qui spécifie le mot de passe pour le contexte utilisateur donné. En cas d’omission, Schtasks.exe invite l’utilisateur à entrer des données.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nom_tâche**
</dt> <dd>

Valeur qui spécifie le nom de la tâche planifiée à arrêter.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valeur qui affiche l’aide pour Schtasks.exe.

</dd> </dl>

## <a name="querying-for-task-information"></a>Interrogation des informations sur les tâches

La syntaxe suivante est utilisée pour afficher les tâches planifiées à partir de l’ordinateur local ou distant.

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

### <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span> **Système** /s
</dt> <dd>

Valeur qui spécifie l’ordinateur distant auquel se connecter. En cas d’omission, le paramètre système est défini par défaut sur l’ordinateur local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nom d’utilisateur**
</dt> <dd>

Valeur qui spécifie le contexte utilisateur sous lequel Schtasks.exe doit s’exécuter.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ mot \] de passe**
</dt> <dd>

Valeur qui spécifie le mot de passe pour le contexte utilisateur donné. En cas d’omission, Schtasks.exe invite l’utilisateur à entrer des données.

</dd> <dt>

<span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**/FO** **format**
</dt> <dd>

Valeur qui spécifie le format de sortie. Les valeurs valides sont TABLE, LIST et CSV.

</dd> <dt>

<span id="_NH_"></span><span id="_nh_"></span>**/NH** 
</dt> <dd>

Valeur qui spécifie que l’en-tête de colonne ne doit pas être affiché dans la sortie. Cela est valide uniquement pour les formats TABLE et CSV.

</dd> <dt>

<span id="_V_"></span><span id="_v_"></span>**/F** 
</dt> <dd>

Valeur qui affiche la sortie de tâche détaillée.

> [!Note]  
> Si une tâche était planifiée pour s’exécuter une seule fois, les informations de planification affichées sont « les données de planification ne sont pas disponibles dans ce format ».

 

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nom_tâche**
</dt> <dd>

Valeur qui spécifie le nom de la tâche pour laquelle les informations doivent être récupérées. Si aucun nom de tâche n’est spécifié, les informations relatives à toutes les tâches sont affichées.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_XML_"></span><span id="_xml_"></span>**/XML** 
</dt> <dd>

Valeur utilisée pour afficher les définitions de tâche au format XML.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valeur utilisée pour afficher l’aide de Schtasks.exe.

</dd> </dl>

## <a name="changing-a-task"></a>Modification d’une tâche

La syntaxe suivante est utilisée pour modifier le mode d’exécution du programme, ou pour modifier le compte d’utilisateur et le mot de passe utilisés par une tâche planifiée.

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

### <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span> **Système** /s
</dt> <dd>

Valeur qui spécifie l’ordinateur distant auquel se connecter. En cas d’omission, le paramètre système est défini par défaut sur l’ordinateur local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nom d’utilisateur**
</dt> <dd>

Valeur qui spécifie le contexte utilisateur sous lequel Schtasks.exe doit s’exécuter.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ mot \] de passe**
</dt> <dd>

Valeur qui spécifie le mot de passe pour le contexte utilisateur donné. En cas d’omission, Schtasks.exe invite l’utilisateur à entrer des données.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nom_tâche**
</dt> <dd>

Valeur qui spécifie la tâche planifiée à modifier.

</dd> <dt>

<span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/Ru** **nom_d’emprunt**
</dt> <dd>

Valeur qui modifie le nom d’utilisateur (contexte utilisateur) sous lequel la tâche planifiée s’exécute. Pour le compte système, les valeurs valides sont « », «NT AUTHORITY \\ System » ou « System ». Pour les tâches Planificateur de tâches 2,0, les \\ \\ valeurs valides sont également valides : « NT Authority LOCALSERVICE » et « NT Authority NetworkService ».

</dd> <dt>

<span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**
</dt> <dd>

Valeur qui spécifie un nouveau mot de passe pour le contexte utilisateur existant ou le mot de passe d’un nouveau compte d’utilisateur. Ce mot de passe est ignoré pour le compte système.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **exécution_tâche**
</dt> <dd>

Valeur qui spécifie un nouveau programme que la tâche exécutera.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**
</dt> <dd>

Valeur qui spécifie l’heure de début de l’exécution de la tâche. Le format de l’heure est HH : mm (24 heures). Par exemple, 14:30 spécifie 2:30.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **intervalle**
</dt> <dd>

Valeur qui spécifie l’intervalle de répétition, en minutes. La plage valide est de 1-599940 minutes.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **heure_fin**
</dt> <dd>

Valeur qui spécifie l’heure de fin de la tâche. Le format de l’heure est HH : mm (24 heures). Par exemple, 14:50 spécifie 2:50PM.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span> **Durée** /du
</dt> <dd>

Valeur qui spécifie la durée d’exécution de la tâche. Le format de l’heure est HH : mm (24 heures). Par exemple, 14:50 spécifie 2:50PM. Cela ne s’applique pas au paramètre/ET.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/K** 
</dt> <dd>

Valeur qui termine la tâche à l’heure de fin ou de la durée.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **DateDébut**
</dt> <dd>

Valeur qui spécifie la première date à laquelle la tâche doit être exécutée. Le format est mm/jj/aaaa.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**
</dt> <dd>

Valeur qui spécifie la dernière date à laquelle la tâche s’exécutera. Le format est mm/jj/aaaa.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Valeur qui permet à la tâche de s’exécuter de manière interactive uniquement si l’utilisateur/RU est actuellement connecté au moment de l’exécution de la tâche. La tâche s’exécute uniquement si l’utilisateur a ouvert une session.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Niveau** /RL
</dt> <dd>

Valeur qui définit le niveau d’exécution de la tâche. Les valeurs valides sont LIMITED et HIGHEST.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE** 
</dt> <dd>

Valeur qui active la tâche planifiée. Une tâche activée peut s’exécuter et une tâche désactivée ne peut pas s’exécuter.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE** 
</dt> <dd>

Valeur qui désactive l’exécution de la tâche planifiée.

> [!Note]  
> Si une tâche Planificateur de tâches distante 1,0 est désactivée par Schtasks.exe et que l’exception de pare-feu partage de fichiers et d’imprimantes est activée et que l’exception de pare-feu de gestion des tâches planifiées distantes est désactivée, la tâche ne sera pas désactivée lors de la lecture à partir d’une API Planificateur de tâches 2,0.

 

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**Z** 
</dt> <dd>

Valeur qui marque la tâche à supprimer après sa dernière exécution.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **DelayTime**
</dt> <dd>

Valeur qui spécifie le temps d’attente pour retarder l’exécution de la tâche après le déclenchement du déclencheur. Le format de l’heure est mmmm : SS. Cette option est valide uniquement pour les tâches avec les types de planification ONSTARt, ONLOGON et ONEVENT.

**Windows XP et Windows Server 2003 :** Cette option n’est pas disponible.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Valeur qui affiche le message d’aide pour Schtasks.exe.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



 

 





