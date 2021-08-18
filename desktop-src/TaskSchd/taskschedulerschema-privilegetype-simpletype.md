---
title: Type simple privilegeType
description: Les privilèges déterminent le type d’opérations système qu’un compte d’utilisateur peut effectuer. Un administrateur attribue des privilèges aux comptes d’utilisateurs et de groupes. Les privilèges de chaque utilisateur incluent ceux octroyés à l’utilisateur et aux groupes auxquels l’utilisateur appartient.
ms.assetid: 813b0886-ca76-4523-a1e6-42ca656851a7
keywords:
- Planificateur de tâches de type simple privilegeType
topic_type:
- apiref
api_name:
- privilegeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4502c22e31ca131dabd6d776337c3693a4d4bf4d7753734cf0e6291cf234fbe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002287"
---
# <a name="privilegetype-simple-type"></a>Type simple privilegeType

Les privilèges déterminent le type d’opérations système qu’un compte d’utilisateur peut effectuer. Un administrateur attribue des privilèges aux comptes d’utilisateurs et de groupes. Les privilèges de chaque utilisateur incluent ceux octroyés à l’utilisateur et aux groupes auxquels l’utilisateur appartient.

``` syntax
<xs:simpleType name="privilegeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="SeCreateTokenPrivilege"
         />
        <xs:enumeration
            value="SeAssignPrimaryTokenPrivilege"
         />
        <xs:enumeration
            value="SeLockMemoryPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseQuotaPrivilege"
         />
        <xs:enumeration
            value="SeUnsolicitedInputPrivilege"
         />
        <xs:enumeration
            value="SeMachineAccountPrivilege"
         />
        <xs:enumeration
            value="SeTcbPrivilege"
         />
        <xs:enumeration
            value="SeSecurityPrivilege"
         />
        <xs:enumeration
            value="SeTakeOwnershipPrivilege"
         />
        <xs:enumeration
            value="SeLoadDriverPrivilege"
         />
        <xs:enumeration
            value="SeSystemProfilePrivilege"
         />
        <xs:enumeration
            value="SeSystemtimePrivilege"
         />
        <xs:enumeration
            value="SeProfileSingleProcessPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseBasePriorityPrivilege"
         />
        <xs:enumeration
            value="SeCreatePagefilePrivilege"
         />
        <xs:enumeration
            value="SeCreatePermanentPrivilege"
         />
        <xs:enumeration
            value="SeBackupPrivilege"
         />
        <xs:enumeration
            value="SeRestorePrivilege"
         />
        <xs:enumeration
            value="SeShutdownPrivilege"
         />
        <xs:enumeration
            value="SeDebugPrivilege"
         />
        <xs:enumeration
            value="SeAuditPrivilege"
         />
        <xs:enumeration
            value="SeSystemEnvironmentPrivilege"
         />
        <xs:enumeration
            value="SeChangeNotifyPrivilege"
         />
        <xs:enumeration
            value="SeRemoteShutdownPrivilege"
         />
        <xs:enumeration
            value="SeUndockPrivilege"
         />
        <xs:enumeration
            value="SeSyncAgentPrivilege"
         />
        <xs:enumeration
            value="SeEnableDelegationPrivilege"
         />
        <xs:enumeration
            value="SeManageVolumePrivilege"
         />
        <xs:enumeration
            value="SeImpersonatePrivilege"
         />
        <xs:enumeration
            value="SeCreateGlobalPrivilege"
         />
        <xs:enumeration
            value="SeTrustedCredManAccessPrivilege"
         />
        <xs:enumeration
            value="SeRelabelPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseWorkingSetPrivilege"
         />
        <xs:enumeration
            value="SeTimeZonePrivilege"
         />
        <xs:enumeration
            value="SeCreateSymbolicLinkPrivilege"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valeurs d’énumération

Le type simple **privilegeType** définit les valeurs suivantes.



| Valeur                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SeCreateTokenPrivilege          | Requis pour créer un jeton principal. Droit d’utilisateur : créez un objet de jeton.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeAssignPrimaryTokenPrivilege   | Requis pour assigner le jeton principal d’un processus. Droit de l’utilisateur : remplacez un jeton au niveau du processus.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeLockMemoryPrivilege           | Requis pour verrouiller des pages physiques en mémoire. Droit de l’utilisateur : verrouiller les pages en mémoire. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeIncreaseQuotaPrivilege        | Requis pour augmenter le quota affecté à un processus. Droit d’utilisateur : ajuster les quotas de mémoire pour un processus. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeUnsolicitedInputPrivilege     | Requis pour lire une entrée non sollicitée à partir d’un périphérique terminal. Droit de l’utilisateur : non applicable. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SeMachineAccountPrivilege       | Requis pour créer un compte d’ordinateur. Droit d’utilisateur : ajouter des stations de travail au domaine. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeTcbPrivilege                  | Ce privilège identifie son détenteur dans le cadre de la base de l’ordinateur approuvé. Certains sous-systèmes protégés approuvés bénéficient de ce privilège. Droit de l’utilisateur : agir en tant que partie du système d’exploitation. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SeSecurityPrivilege             | Requis pour effectuer un certain nombre de fonctions liées à la sécurité, telles que le contrôle et l’affichage des messages d’audit. Ce privilège identifie son détenteur comme un opérateur de sécurité. Droit d’utilisateur : gérer l’audit et le journal de sécurité. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeTakeOwnershipPrivilege        | Requis pour prendre possession d’un objet sans disposer d’un accès discrétionnaire. Ce privilège permet de définir la valeur owner uniquement sur les valeurs que le détenteur peut légitimement attribuer en tant que propriétaire d’un objet. Droit d’utilisateur : appropriation de fichiers ou d’autres objets. <br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| SeLoadDriverPrivilege           | Requis pour charger ou décharger un pilote de périphérique. Droit de l’utilisateur : charger et décharger les pilotes de périphérique. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemProfilePrivilege        | Requis pour collecter des informations de profilage pour l’ensemble du système. Droit de l’utilisateur : profiler les performances du système. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemtimePrivilege           | Requis pour modifier l’heure système. Droit de l’utilisateur : modifier l’heure système. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeProfileSingleProcessPrivilege | Requis pour collecter des informations de profilage pour un seul processus. Droit de l’utilisateur : profiler un processus unique. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseBasePriorityPrivilege | Requis pour augmenter la priorité de base d’un processus. Droit de l’utilisateur : augmenter la priorité de planification. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeCreatePagefilePrivilege       | Requis pour créer un fichier d’échange. Droit d’utilisateur : créer un fichier d’échange. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| SeCreatePermanentPrivilege      | Requis pour créer un objet permanent. Droit d’utilisateur : créez des objets partagés permanents. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| SeBackupPrivilege               | Requis pour effectuer des opérations de sauvegarde. Ce privilège force le système à accorder tout contrôle d’accès en lecture à n’importe quel fichier, quelle que soit la liste de contrôle d’accès (ACL) spécifiée pour le fichier. Toute demande d’accès autre que Read est toujours évaluée avec la liste de contrôle d’accès. Ce privilège est requis par RegSaveKey et RegSaveKeyExfunctions. Les droits d’accès suivants sont accordés si ce privilège est détenu : \_ contrôle de lecture, sécurité du système d’accès \_ \_ , \_ \_ lecture générique de fichier, parcours de fichier \_ . Droit d’utilisateur : sauvegarde des fichiers et des répertoires. <br/>                                                                                                                                     |
| SeRestorePrivilege              | Requis pour effectuer des opérations de restauration. Ce privilège force le système à accorder tout contrôle d’accès en écriture à n’importe quel fichier, quelle que soit la liste ACL spécifiée pour le fichier. Toute demande d’accès autre que l’écriture est toujours évaluée avec la liste de contrôle d’accès. En outre, ce privilège vous permet de définir un identificateur de sécurité (SID) d’utilisateur ou de groupe valide en tant que propriétaire d’un fichier. Ce privilège est requis par la fonction RegLoadKey. Les droits d’accès suivants sont accordés si ce privilège est détenu : écriture \_ DAC, \_ propriétaire en écriture, \_ sécurité système Access \_ , \_ écriture générique fichier, fichier d' \_ \_ Ajout de fichier \_ , \_ \_ sous-répertoire d’ajout de fichier, supprimer. Droit de l’utilisateur : restaurez les fichiers et les répertoires. <br/> |
| SeShutdownPrivilege             | Requis pour arrêter un système local. Droit de l’utilisateur : Arrêtez le système. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeDebugPrivilege                | Requis pour déboguer et ajuster la mémoire d’un processus appartenant à un autre compte. Droit de l’utilisateur : déboguer les programmes. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeAuditPrivilege                | Requis pour générer des entrées de journal d’audit. Accordez ce privilège à des serveurs sécurisés. Droit d’utilisateur : générer des audits de sécurité. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| SeSystemEnvironmentPrivilege    | Requis pour modifier la mémoire RAM non volatile des systèmes qui utilisent ce type de mémoire pour stocker les informations de configuration. Droit de l’utilisateur : modifier les valeurs de l’environnement du microprogramme. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeChangeNotifyPrivilege         | Requis pour recevoir des notifications des modifications apportées aux fichiers ou aux répertoires. Ce privilège oblige également le système à ignorer toutes les vérifications d’accès Traversal. Il est activé par défaut pour tous les utilisateurs. Droit d’utilisateur : contourner la vérification de parcours. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeRemoteShutdownPrivilege       | Requis pour arrêter un système à l’aide d’une demande réseau. Droit de l’utilisateur : forcer l’arrêt à partir d’un système distant. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SeUndockPrivilege               | Requis pour déconnecter un ordinateur portable. Droit d’utilisateur : supprimer l’ordinateur de la station d’accueil. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeSyncAgentPrivilege            | Requis pour qu’un contrôleur de domaine utilise les services de synchronisation d’annuaires LDAP. Ce privilège permet au détenteur de lire tous les objets et propriétés de l’annuaire, quelle que soit la protection des objets et des propriétés. Par défaut, il est affecté aux comptes administrateur et LocalSystem sur les contrôleurs de domaine. Droit de l’utilisateur : synchroniser les données du service d’annuaire. <br/>                                                                                                                                                                                                                                                                                |
| SeEnableDelegationPrivilege     | Requis pour marquer les comptes d’utilisateurs et d’ordinateurs comme approuvés pour la délégation. Droit d’utilisateur : activez les comptes d’ordinateur et d’utilisateur pour qu’ils soient approuvés pour la délégation. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeManageVolumePrivilege         | Requis pour activer les privilèges de gestion du volume. Droit de l’utilisateur : gérez les fichiers sur un volume. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeImpersonatePrivilege          | Requis pour emprunter l’identité. Droit d’utilisateur : emprunter l’identité d’un client après l’authentification. Windows XP/2000 : ce privilège n’est pas pris en charge. <br/> notez que cette valeur est prise en charge à partir de Windows Server 2003, Windows XP avec SP2 et Windows 2000 avec SP4.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateGlobalPrivilege         | Requis pour créer des objets de mappage de fichiers nommés dans l’espace de noms global pendant les sessions des services Terminal Server. Ce privilège est activé par défaut pour les administrateurs, les services et le compte système local. Droit de l’utilisateur : créer des objets globaux. Windows XP/2000 : ce privilège n’est pas pris en charge. <br/> notez que cette valeur est prise en charge à partir de Windows Server 2003, Windows XP avec SP2 et Windows 2000 avec SP4.<br/>                                                                                                                                                                                                                                        |
| SeTrustedCredManAccessPrivilege | Requis pour accéder au gestionnaire d’informations d’identification en tant qu’appelant approuvé. Droit de l’utilisateur : accédez au gestionnaire des informations d’identification en tant qu’appelant approuvé. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeRelabelPrivilege              | Requis pour modifier le niveau d’intégrité obligatoire d’un objet. Droit de l’utilisateur : modifier l’étiquette d’un objet. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseWorkingSetPrivilege   | Requis pour allouer davantage de mémoire pour les applications qui s’exécutent dans le contexte des utilisateurs. Droit d’utilisateur : augmenter une plage de travail de processus. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| SeTimeZonePrivilege             | Requis pour ajuster le fuseau horaire associé à l’horloge interne de l’ordinateur. Droit de l’utilisateur : modifiez le fuseau horaire. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateSymbolicLinkPrivilege   | Requis pour créer un lien symbolique. Droit d’utilisateur : créez des liens symboliques. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



 

 





