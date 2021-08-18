---
title: Suivi d’événements dans ADSI
description: Windows le serveur 2008 et Windows Vista introduisent le suivi d’événements dans les Interfaces ADSI (Active Directory Service Interfaces).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- suivi d’événements (ADSI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59b2db3775c8c578ad361667a2d89c36240caf4b3bbb4bcd5cdd2798011514b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023977"
---
# <a name="event-tracing-in-adsi"></a>Suivi d’événements dans ADSI

Windows le serveur 2008 et Windows Vista introduisent [le suivi d’événements](/windows/desktop/ETW/event-tracing-portal) dans les Interfaces ADSI ( [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) ). Certaines zones du fournisseur LDAP ADSI ont une implémentation sous-jacente qui est complexe ou qui implique une séquence d’étapes qui complique le diagnostic des problèmes. Pour aider les développeurs d’applications à résoudre les problèmes, le suivi d’événements a été ajouté aux domaines suivants :

## <a name="schema-parsing-and-downloading"></a>Analyse et téléchargement de schéma

L’interface IADs dans ADSI exige que le schéma LDAP soit mis en cache sur le client afin que les attributs puissent être correctement marshalés (comme décrit dans le [modèle de schéma ADSI](adsi-schema-model.md)). Pour ce faire, ADSI charge le schéma pour chaque processus (et pour chaque serveur/domaine LDAP) dans la mémoire soit à partir d’un fichier de schéma (. SCH) qui est enregistré sur le disque local, soit en le téléchargeant à partir du serveur LDAP. Des processus différents sur le même ordinateur client utilisent le schéma mis en cache sur le disque, s’il est disponible et applicable.

Si le schéma ne peut pas être obtenu à partir du disque ou du serveur, ADSI utilise un schéma par défaut codé en dur. Lorsque cela se produit, les attributs qui ne font pas partie de ce schéma par défaut ne peuvent pas être marshalés et ADSI retourne une erreur lors de la récupération de ces attributs. Un certain nombre de facteurs peuvent être à l’origine de ce problème, y compris des problèmes d’analyse du schéma et des privilèges insuffisants pour télécharger le schéma. Il est souvent difficile de déterminer la raison pour laquelle un certain schéma par défaut est utilisé. L’utilisation du suivi d’événements dans cette zone permet de diagnostiquer plus rapidement le problème et de le résoudre.

## <a name="changing-and-setting-the-password"></a>Modification et définition du mot de passe

[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) et [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) utilisent plusieurs mécanismes pour effectuer l’opération demandée en fonction de la configuration disponible (comme décrit dans [définition et modification des mots de passe utilisateur à l’aide du fournisseur LDAP](setting-user-passwords-for-ldap-providers.md)). Lorsque **ChangePassword** et **SetPassword** échouent, il peut être difficile de déterminer précisément pourquoi et le suivi d’événements vous aidera à résoudre les problèmes liés à ces méthodes.

## <a name="adsi-bind-cache"></a>Cache de liaison ADSI

ADSI tente de réutiliser les connexions LDAP en interne chaque fois que cela est possible (voir [mise en cache de connexion](connection-caching.md)). Lors de la résolution des problèmes, il est utile de déterminer si une nouvelle connexion a été ouverte pour la communication avec le serveur ou si une connexion existante a été utilisée. Il peut également être utile pour effectuer le suivi du cycle de vie du cache de connexion (parfois appelé cache de liaison) et de sa création ou de sa fermeture, et si une référence de connexion a eu lieu. Dans le cas d’une [liaison sans serveur](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI appelle le localisateur de contrôleur de domaine pour sélectionner un serveur pour le domaine du contexte de l’utilisateur. ADSI gère ensuite un cache du mappage du serveur de domaine pour les connexions suivantes. Le suivi d’événements permet de suivre la sélection du contrôleur de périphérique et est donc utile pour résoudre les problèmes liés à la connexion.

## <a name="enabling-tracing-and-starting-a-tracing-session"></a>Activation du traçage et du démarrage d’une session de suivi

Pour activer le suivi ADSI, créez la clé de Registre suivante :

**HKEY \_ \_Ordinateur local** \\ **système** de \\ **CurrentControlSet** \\ **services** de CurrentControlSet \\  \\ **suivi** \\ **** ADSI

*ProcessName* est le nom complet du processus que vous souhaitez suivre, y compris son extension (par exemple, « Svchost.exe »). En outre, vous pouvez placer une valeur facultative de type **DWORD** nommée PID dans cette clé. Il est fortement recommandé de définir cette valeur et de tracer ainsi un seul processus particulier. Dans le cas contraire, toutes les instances de l’application spécifiées par *ProcessName* sont tracées.

Exécutez ensuite la commande suivante :

**tracelog.exe-Start** *nom_session* **-GUID \#** _Provider \_ GUID_ **-f** *nom* **-indicateur** *traceFlags* **-Level** *TraceLevel*

*NomSession* est simplement un identificateur arbitraire utilisé pour étiqueter la session de suivi (vous devrez faire référence à ce nom de session ultérieurement lorsque vous arrêtez la session de suivi). Le GUID du fournisseur de suivi ADSI est « 7288c9f8-D63C-4932-A345-89d6b060174d ». *filename* spécifie le fichier journal dans lequel les événements seront écrits. *traceFlags* doit avoir l’une des valeurs suivantes :



|         Indicateur                        |         Valeur              |
|---------------------------------|-----------------------|
| **schéma de débogage \_**<br/>    | 0x00000001<br/> |
| **CHANGEPWD de débogage \_**<br/> | 0x00000002<br/> |
| **déboguer \_ setpwd**<br/>    | 0x00000004<br/> |
| **BINDCACHE de débogage \_**<br/> | 0x00000008<br/> |



 

Ces indicateurs déterminent les méthodes [ADSI](active-directory-service-interfaces-adsi.md) qui seront suivies, en fonction du tableau suivant :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>DEBUG_SCHEMA</strong><br/></td>
<td><ul>
<li>LdapGetSchema</li>
<li>GetSchemaInfoTime</li>
<li>LdapReadSchemaInfoFromServer</li>
<li>ProcessSchemaInfo</li>
<li>HelperReadLdapSchemaInfo</li>
<li>ProcessClassInfoArray</li>
<li>ReadSchemaInfoFromRegistry</li>
<li>StoreSchemaInfoFromRegistry</li>
<li>AttributeTypeDescription</li>
<li>ObjectClassDescription</li>
<li>DITContentRuleDescription</li>
<li>DirectoryString</li>
<li>DirectoryStrings</li>
<li>DITContentRuleDescription</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DEBUG_CHANGEPWD</strong><br/></td>
<td><ul>
<li>CADsUser :: ChangePassword</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><strong>DEBUG_SETPWD</strong><br/></td>
<td><ul>
<li>CADsUser :: SetPassword</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DEBUG_BINDCACHE</strong><br/></td>
<td><ul>
<li>GetServerBasedObject</li>
<li>GetServerLessBasedObject</li>
<li>GetGCDomainName</li>
<li>GetDefaultDomainName</li>
<li>GetUserDomainFlatName</li>
<li>BindCacheLookup</li>
<li>EquivalentPortNumbers</li>
<li>CanCredentialsBeReused</li>
<li>BindCacheAdd</li>
<li>BindCacheAddRef</li>
<li>AddReferralLink</li>
<li>CommonRemoveEntry</li>
<li>BindCacheDerefHelper</li>
<li>NotifyNewConnection</li>
<li>QueryForConnection</li>
<li>LdapOpenBindWithCredentials</li>
<li>LdapOpenBindWithDefaultCredentials</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

Vous pouvez combiner des indicateurs en combinant les bits appropriés dans l’argument *traceFlags* . Par exemple, pour spécifier le **\_ schéma de débogage** et **déboguer les indicateurs \_ BINDCACHE** , la valeur *traceFlags* appropriée est 0x00000009.

Enfin, l’indicateur *TraceLevel* doit avoir l’une des valeurs suivantes :



|      Indicateur                                    |       Valeur                |
|------------------------------------------|-----------------------|
| **\_erreur au niveau de la trace \_**<br/>       | 0x00000002<br/> |
| **\_informations sur le niveau de suivi \_**<br/> | 0x00000004<br/> |



 

**Trace \_ Les \_ informations de niveau** entraînent l’enregistrement de tous les événements par le processus de suivi, tandis que le suivi de l' **\_ \_ erreur** entraîne l’enregistrement des événements d’erreur par le processus de suivi.

Pour terminer le suivi, exécutez la commande suivante :

**tracelog.exe-Stop** *nom_session*

Dans l’exemple précédent, *NomSession* est le même nom que celui fourni avec la commande qui a démarré la section de suivi.

## <a name="remarks"></a>Remarques

Il est plus efficace de suivre uniquement des processus spécifiques en spécifiant un PID particulier pour suivre tous les processus sur un ordinateur. Si vous avez besoin d’effectuer le suivi de plusieurs applications sur le même ordinateur, il peut y avoir un impact sur les performances. Il y a une sortie de débogage substantielle dans les sections orientées performance du code. En outre, les administrateurs doivent veiller à définir correctement les autorisations des fichiers journaux lors du suivi de plusieurs processus. dans le cas contraire, n’importe quel utilisateur peut être en mesure de lire les journaux de suivi, et les autres utilisateurs pourront suivre les processus qui contiennent des informations sécurisées.

Par exemple, supposons que l’administrateur configure le suivi pour une application « Test.exe » et ne spécifie pas un PID dans le registre pour suivre plusieurs instances du processus. À présent, un autre utilisateur souhaite suivre l’application « Secure.exe ». Si les fichiers journaux de suivi ne sont pas correctement restreints, il suffit à l’utilisateur de renommer « Secure.exe » en « Test.exe », et il sera suivi. En général, il est préférable de suivre uniquement des processus spécifiques pendant la résolution des problèmes et de supprimer la clé de registre de suivi dès que le dépannage est terminé.

Étant donné que l’activation du suivi d’événements génère des fichiers journaux supplémentaires, les administrateurs doivent surveiller attentivement les tailles des fichiers journaux. un manque d’espace disque sur l’ordinateur local peut provoquer un déni de service.

## <a name="example-scenarios"></a>Exemples de scénarios

Scénario 1 : l’administrateur voit une erreur inattendue dans une application qui définit des mots de passe pour les comptes d’utilisateur. par conséquent, ils prennent les mesures suivantes pour résoudre le problème à l’aide du suivi d’événements.

1.  Écrire un script qui reproduit le problème et créer la clé de Registre

    **HKEY \_ \_** \\  \\  \\  \\  \\ **Suivi** ADSI des services \\ **** de CurrentControlSet de système d’ordinateur localcscript.exe

2.  Démarrez une session de suivi, en affectant à *traceFlags* la valeur 0X2 (**Déboguer \_ CHANGEPASSWD**) et *TraceLevel* à 0x4 (**informations de \_ niveau \_ de suivi**), à l’aide de la commande suivante :

    **tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ ADSI. etl-indicateur 0X2-niveau 0x4**

3.  Exécutez cscript.exe avec le script de test pour reproduire le problème, puis terminez la session de suivi :

    **tracelog.exe-arrêter scripttrace**

4.  Supprimer la clé de Registre

    **HKEY \_ \_** \\  \\  \\  \\  \\ **Suivi** ADSI des services \\ **** de CurrentControlSet de système d’ordinateur localcscript.exe

5.  Exécutez l’outil ETW Tracerpt.exe pour analyser les informations de suivi du journal :

    **tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ ADSI. etl-indicateur 0X2-niveau 0x4**

Scénario 2 : l’administrateur souhaite suivre les opérations d’analyse et de téléchargement du schéma dans une application [asp](https://msdn.microsoft.com/asp.net/default.aspx) nommée w3wp.exe qui est déjà en cours d’exécution. Pour ce faire, l’administrateur doit effectuer les étapes suivantes :

1.  Créer la clé de Registre

    **HKEY \_ \_** \\  \\  \\  \\  \\ **Suivi** ADSI des services \\ **** de CurrentControlSet de système d’ordinateur localw3wp.exe

    et à l’intérieur de cette clé, créez une valeur de type DWORD nommée PID et affectez-lui l’ID de processus de l’instance de w3wp.exe en cours d’exécution sur l’ordinateur local.

2.  Ensuite, ils créent une session de suivi, en affectant à *traceFlags* la valeur 0x1 (**\_ schéma de débogage**) et *TraceLevel* à 0x4 (**\_ \_ informations de niveau de suivi**) :

    **tracelog.exe-Start w3wptrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ w3wp. etl-indicateur 0x1-niveau 0x4**

3.  Reproduisez l’opération qui nécessite un dépannage.
4.  Mettre fin à la session de suivi :

    **tracelog.exe-arrêter w3wptrace**

5.  Supprimez la clé de Registre **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\ **service** \\ **ADSI** \\ **Tracing** \\ **w3wp.exe**.
6.  Exécutez l’outil ETW tracerpt.exe pour analyser les informations de suivi du journal :

    **tracerpt.exe. \\ w3wp. etl-o-Report**

 

