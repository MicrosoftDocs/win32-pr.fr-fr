---
description: Winmgmt est le service WMI dans le processus SVCHOST s’exécutant sous le &\# 0034 ; LocalSystem&\# 0034 ; compte.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: critique
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- winmgmt
api_type:
- NA
api_location: ''
ms.openlocfilehash: d28d37faf454accd91281034d0aeb8df5e10dddb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879863"
---
# <a name="winmgmt"></a>critique

Winmgmt est le service WMI dans le processus SVCHOST s’exécutant sous le compte « LocalSystem ».

Dans tous les cas, le service WMI démarre automatiquement lorsque la première application ou le script de gestion demande une connexion à un espace de noms WMI. Pour plus d’informations, consultez [Démarrage et arrêt du service WMI](starting-and-stopping-the-wmi-service.md).

> [!Note]  
> WMI est un composant fondamental du système d’exploitation Windows qui permet aux développeurs et aux administrateurs informatiques d’écrire des scripts et des applications pour automatiser certaines tâches. Winmgmt.exe est le service qui permet à WMI de s’exécuter sur votre ordinateur local. Pour plus d’informations sur l’utilisation de WMI, consultez [utilisation de WMI](using-wmi.md). Si vous avez reçu un message d’erreur concernant winmgmt.exe, consultez [résolution des problèmes liés à WMI](wmi-troubleshooting.md). Pour plus d’informations sur la Winmgmt.exe, consultez [utilisation des outils de gestion WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).

 

Lorsqu’il est exécuté à partir de l’invite de commandes, le service WMI dispose des commutateurs suivants.

``` syntax
winmgmt 
  [/backup <filename>] 
  [/restore <filename> <mode>] 
  [/resyncperf <winmgmt service process id>] 
  [/standalonehost <level>]
  [/sharedhost]
  [/verifyrepository <path>]
  [/salvagerepository] 
  [/resetrepository]
```

## <a name="switches"></a>Commutateurs

<dl> <dt>

<span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>**/Backup** ( *&lt; nom de fichier &gt;* ) 
</dt> <dd>

Permet à WMI de sauvegarder le référentiel dans le nom de fichier spécifié. L’argument *filename* doit contenir le chemin d’accès complet à l’emplacement du fichier. Ce processus nécessite un verrou d’écriture sur le référentiel afin que les opérations d’écriture dans le référentiel soient interrompues jusqu’à la fin du processus de sauvegarde.

Si vous ne spécifiez pas de chemin d’accès pour le fichier, il est placé dans le répertoire% windir% \\ system32.

</dd> <dt>

<span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>l' *&lt; indicateur &gt;* de *&lt; nom de &gt; fichier* **/Restore** 
</dt> <dd>

Restaure manuellement le référentiel WMI à partir du fichier de sauvegarde spécifié. L’argument *filename* doit contenir le chemin d’accès complet à l’emplacement du fichier de sauvegarde. Pour effectuer l’opération de restauration, WMI enregistre le référentiel existant en écriture différée si l’opération échoue. Le référentiel est ensuite restauré à partir du fichier de sauvegarde spécifié dans l’argument de *nom de fichier* . Si l’accès exclusif au référentiel ne peut pas être effectué, les clients existants sont déconnectés de WMI.

L’argument *Flag* doit avoir la valeur 1 (forcer la déconnexion des utilisateurs et la restauration) ou 0 (restauration par défaut si aucun utilisateur n’est connecté) et spécifie le mode de restauration.

</dd> <dt>

<span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *&lt; winmgmt-service-Process-ID &gt;* 
</dt> <dd>

Inscrit les bibliothèques de performances de l’ordinateur avec WMI. PID WMI est l’ID de processus du service WMI.

Nécessaire uniquement si les classes de l’analyseur de performances ne retournent pas de résultats fiables.

</dd> <dt>

<span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost** \[ de *&lt; niveau &gt;*\]
</dt> <dd>

Déplace le service WinMgmt vers un processus Svchost autonome qui a un point de terminaison DCOM fixe. Le point de terminaison par défaut est « ncacn \_ IP \_ TCP. 0.24158 ». Toutefois, le point de terminaison peut être modifié en exécutant Dcomcnfg.exe. Pour plus d’informations sur la configuration d’un port fixe pour WMI, consultez [configuration d’un port fixe pour WMI](setting-up-a-fixed-port-for-wmi.md).

L’argument *Level* est le niveau d’authentification pour le processus Svchost. WMI s’exécute normalement dans le cadre d’un hôte de service partagé et vous ne pouvez pas augmenter le niveau d’authentification pour WMI seul. Si le *niveau* n’est pas spécifié, la valeur par défaut est 4 (**RPC \_ C \_ Authn \_ niveau \_ PKT** ou **WbemAuthenticationLevelPkt**).

Vous pouvez exécuter WMI de manière plus sécurisée en accroissant le niveau d’authentification à la confidentialité des paquets (RPC-niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité** ou **WbemAuthenticationLevelPktPrivacy**). les niveaux d’authentification pour les Visual Basic et les scripts sont décrits dans [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum). Pour C++, consultez [définition du niveau de sécurité de processus par défaut à l’aide de c++](setting-the-default-process-security-level-using-c-.md). Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).

</dd> <dt>

<span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**
</dt> <dd>

Déplace le service WinMgmt dans le processus Svchost partagé.

</dd> <dt>

<span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>**/verifyrepository** *&lt; chemin &gt; d’accès* 
</dt> <dd>

Effectue une vérification de cohérence sur le référentiel WMI. Lorsque vous ajoutez le commutateur **/verifyrepository** sans l’argument *&lt; path &gt;* , le référentiel Live actuellement utilisé par WMI est vérifié. Lorsque vous spécifiez l’argument *path* , vous pouvez vérifier toute copie enregistrée du dépôt. Dans ce cas, l’argument Path doit contenir le chemin d’accès complet à la copie enregistrée du dépôt. Le référentiel enregistré doit être une copie de l’intégralité du dossier de dépôt. Pour plus d’informations sur les erreurs retournées par cette commande, consultez la section Notes.

</dd> <dt>

<span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**
</dt> <dd>

Effectue une vérification de cohérence sur le référentiel WMI et, si une incohérence est détectée, reconstruit le référentiel. Le contenu du référentiel incohérent est fusionné dans le référentiel reconstruit, s’il peut être lu par défaut. L’opération de récupération fonctionne toujours avec le référentiel actuellement utilisé par le service WMI. Pour plus d’informations sur les erreurs retournées par cette commande, consultez la section Notes.

Les fichiers MOF qui contiennent l’instruction de préprocesseur [**\# pragma AutoRecover**](pragma-autorecover.md) sont restaurés dans le référentiel.

</dd> <dt>

<span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**
</dt> <dd>

Le référentiel est réinitialisé à l’état initial lors de la première installation du système d’exploitation. Les fichiers MOF qui contiennent l’instruction de préprocesseur [**\# pragma autoautorecover**](pragma-autorecover.md) sont restaurés dans le référentiel.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cet outil se trouve dans le répertoire% windir% \\ system32 \\ WBEM. Pour obtenir la liste des commutateurs disponibles, tapez `WinMgmt /?` à l’invite de commandes.

L’espace de stockage WMI, également connu sous le nom de référentiel CIM, n’est pas un simple fichier, mais une collection de fichiers dans le dossier du référentiel qui fonctionnent ensemble comme une base de données. Lorsque vous utilisez le commutateur **/Backup** pour sauvegarder le dépôt, la sauvegarde obtenue est un fichier compressé unique.

WMI retourne l’erreur erreur de **\_ \_ \_ défaillance** de la base de donnes (net helpmsg 1358) si une opération de vérification indique que le référentiel n’est pas dans un état cohérent. Cette erreur peut être retournée à partir de toute commande qui effectue une vérification de référentiel, telle que **/verifyrepository** ou **/salvagerepository**.

> [!Note]
>
> Si WMI renvoie des messages d’erreur, sachez qu’ils ne peuvent pas indiquer des problèmes dans le service WMI ou les fournisseurs WMI. Les échecs peuvent provenir d’autres parties du système d’exploitation et émerger comme des erreurs via WMI. Dans tous les cas, ne supprimez pas le référentiel WMI en tant que première action, car la suppression du dépôt peut endommager le système ou les applications installées.
>
> pour plus d’informations sur la source du problème, téléchargez et exécutez l’outil en ligne de commande [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic. Cet outil génère un rapport qui peut généralement isoler la source du problème et fournir des instructions sur la façon de le résoudre. Le rapport aide également les services de support technique Microsoft à vous aider. vous pouvez télécharger le [WMI Diagnosis Utility](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Résolution des problèmes WMI](wmi-troubleshooting.md)
</dt> <dt>

[Connexion à WMI à distance à partir de Vista](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

