---
description: Le modèle de sécurité Windows vous permet de contrôler l’accès au gestionnaire de contrôle des services (SCM) et aux objets de service.
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: Sécurité des services et droits d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7677b8a9f7a5e1fadf8231999d266a9474fb731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518895"
---
# <a name="service-security-and-access-rights"></a>Sécurité des services et droits d’accès

Le modèle de sécurité Windows vous permet de contrôler l’accès au gestionnaire de contrôle des services (SCM) et aux objets de service. Les sections suivantes fournissent des informations détaillées :

-   [Droits d’accès pour le gestionnaire de contrôle des services](#access-rights-for-the-service-control-manager)
-   [Droits d’accès pour un service](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a>Droits d’accès pour le gestionnaire de contrôle des services

Voici les droits d’accès spécifiques au SCM.



| Droit d’accès                                   | Description                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SC \_ \_Tous les \_ accès au gestionnaire** (0xF003F)         | Comprend **les \_ droits standard \_ requis**, ainsi que tous les droits d’accès figurant dans ce tableau.                                                                                                                                                                                                                                                                                 |
| **SC \_ \_ \_ Service de création de gestionnaire** (0x0002)      | Obligatoire pour appeler la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) afin de créer un objet de service et de l’ajouter à la base de données.                                                                                                                                                                                                                                              |
| **SC \_ Gestionnaire de \_ connexion** (0x0001)              | Requis pour se connecter au gestionnaire de contrôle des services.                                                                                                                                                                                                                                                                                                                      |
| **SC \_ \_ \_ Service d’énumération du gestionnaire** (0x0004)   | Requis pour appeler la fonction [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) ou [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) pour répertorier les services qui se trouvent dans la base de données.<br/> Requis pour appeler la fonction [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) pour recevoir une notification lorsqu’un service est créé ou supprimé.<br/> |
| **SC \_ \_Verrou du gestionnaire** (0x0008)                 | Requis pour appeler la fonction [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) pour acquérir un verrou sur la base de données.                                                                                                                                                                                                                                                      |
| **SC \_ Gestionnaire de modification de la \_ \_ \_ configuration de démarrage** (0x0020) | Requis pour appeler la fonction [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .                                                                                                                                                                                                                                                                                  |
| **SC \_ \_État du \_ verrou \_ de requête du gestionnaire** (0x0010)  | Requis pour appeler la fonction [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) pour récupérer les informations d’état de verrouillage de la base de données.                                                                                                                                                                                                                         |



 

Vous trouverez ci-dessous les [droits d’accès génériques](/windows/desktop/SecAuthZ/generic-access-rights) pour le SCM.



<table>
<thead>
<tr class="header">
<th>Droit d’accès</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SC_MANAGER_CREATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_LOCK</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_ALL</strong></td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Un processus avec les droits d’accès corrects peut ouvrir un handle vers le SCM qui peut être utilisé dans les fonctions [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)et [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) . Seuls les processus avec des privilèges d’administrateur peuvent ouvrir des descripteurs sur le SCM qui peuvent être utilisés par les fonctions [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) et [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) .

Le système crée le descripteur de sécurité pour le SCM. Pour obtenir ou définir le descripteur de sécurité pour le SCM, utilisez les fonctions [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) et [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) avec un handle vers l’objet SCManager.

**Windows Server 2003 et Windows XP :** Contrairement à la plupart des autres objets sécurisables, le descripteur de sécurité du SCM ne peut pas être modifié. Ce comportement a été modifié à partir de Windows Server 2003 avec Service Pack 1 (SP1).

Les droits d’accès suivants sont accordés.



<table>
<thead>
<tr class="header">
<th>Compte</th>
<th>Droits d’accès</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Utilisateurs authentifiés distants</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Utilisateurs authentifiés locaux (y compris LocalService et NetworkService)</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>LocalSystem</td>
<td><dl> <strong>SC_MANAGER_CONNECT</strong><br />
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong><br />
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong><br />
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Administrateurs</td>
<td><dl> <strong>SC_MANAGER_ALL_ACCESS</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Notez que les utilisateurs distants authentifiés sur le réseau mais non connectés de manière interactive peuvent se connecter au SCM mais pas effectuer des opérations qui nécessitent d’autres droits d’accès. Pour effectuer ces opérations, l’utilisateur doit être connecté de manière interactive ou le service doit utiliser l’un des comptes de service.

**Windows Server 2003 et Windows XP :** Les utilisateurs authentifiés distants reçoivent les droits de **\_ \_ connexion du gestionnaire** SC, du **\_ \_ \_ service d’énumération SC** Manager, de l' **\_ État du verrou de \_ requête \_ \_ SC Manager** et des droits d’accès **\_ \_ en lecture des droits standard** . Ces droits d’accès sont limités, comme décrit dans le tableau précédent à compter de Windows Server 2003 avec SP1.

Lorsqu’un processus utilise la fonction [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) pour ouvrir un handle vers une base de données de services installés, il peut demander des droits d’accès. Le système effectue une vérification de sécurité par rapport au descripteur de sécurité du SCM avant d’accorder les droits d’accès demandés.

## <a name="access-rights-for-a-service"></a>Droits d’accès pour un service

Les droits d’accès spécifiques à un service sont les suivants :



| Droit d’accès                                | Description                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Service \_ TOUT \_ accès** (0xF01FF)          | Comprend **les \_ droits standard \_ requis** en plus de tous les droits d’accès de ce tableau.                                                                                                                                                                                                                                                                                              |
| **Service \_ MODIFIER la \_ configuration** (0x0002)        | Requis pour appeler la fonction [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) ou [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) pour modifier la configuration du service. Étant donné que l’appelant a le droit de modifier le fichier exécutable exécuté par le système, il doit être accordé uniquement aux administrateurs.                                                              |
| **Service \_ ÉNUMÉRer les \_ dépendants** (0x0008) | Requis pour appeler la fonction [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) pour énumérer tous les services dépendants du service.                                                                                                                                                                                                                                         |
| **Service \_ Interroger** (0x0080)           | Requis pour appeler la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) pour demander au service de signaler son état immédiatement.                                                                                                                                                                                                                                                          |
| **Service \_ PAUSE \_ continue** (0x0040)       | Requis pour appeler la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) pour suspendre ou poursuivre le service.                                                                                                                                                                                                                                                                             |
| **Service \_ \_Configuration** de la requête (0x0001)         | Requis pour appeler les fonctions [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) et [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) pour interroger la configuration du service.                                                                                                                                                                                                           |
| **Service \_ \_État** de la requête (0x0004)         | Requis pour appeler la fonction [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) ou [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) pour demander au gestionnaire de contrôle des services l’état du service.<br/> Requis pour appeler la fonction [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) pour recevoir une notification quand un service change d’État.<br/> |
| **Service \_ DÉBUT** (0x0010)                 | Requis pour appeler la fonction [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) pour démarrer le service.                                                                                                                                                                                                                                                                                             |
| **Service \_ ARRÊTER** (0x0020)                  | Requis pour appeler la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) pour arrêter le service.                                                                                                                                                                                                                                                                                          |
| **Service \_ \_ \_ Contrôle défini par l’utilisateur**(0x0100) | Requis pour appeler la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) pour spécifier un code de contrôle défini par l’utilisateur.                                                                                                                                                                                                                                                                       |



 

Les [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights) pour un service sont les suivants :



| Droit d’accès                 | Description                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ACCÉDER à la \_ sécurité du système \_** | Requis pour appeler la fonction [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) ou [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) pour accéder à la liste SACL. La méthode appropriée pour obtenir cet accès consiste à activer le [**privilège**](/windows/desktop/SecAuthZ/privileges) **\_ \_ nom de sécurité se** dans le jeton d’accès actuel de l’appelant, à ouvrir le handle pour accès à la **\_ \_ sécurité du système** , puis à désactiver le privilège. |
| **Supprimer**   (0x10000)       | Requis pour appeler la fonction [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) pour supprimer le service.                                                                                                                                                                                                                                                                                                                                                  |
| **Lecture \_ CONTRÔLE**  (0x20000)    | Requis pour appeler la fonction [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) pour interroger le descripteur de sécurité de l’objet de service.                                                                                                                                                                                                                                                                                  |
| **Écriture \_ DAC**  (0x40000)    | Requis pour appeler la fonction [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) pour modifier le membre **DACL** du descripteur de sécurité de l’objet de service.                                                                                                                                                                                                                                                                   |
| **Écriture \_ PROPRIÉTAIRE** (0x80000)   | Requis pour appeler la fonction [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) pour modifier les membres **propriétaire** et **groupe** du descripteur de sécurité de l’objet de service.                                                                                                                                                                                                                                                   |



 

Les [droits d’accès génériques](/windows/desktop/SecAuthZ/generic-access-rights) pour un service sont les suivants :



<table>
<thead>
<tr class="header">
<th>Droit d’accès</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SERVICE_CHANGE_CONFIG</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_EXECUTE</strong></td>
<td><dl> <strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Le SCM crée le descripteur de sécurité d’un objet de service lorsque le service est installé par la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) . Le descripteur de sécurité par défaut d’un objet de service accorde l’accès suivant.



<table>
<thead>
<tr class="header">
<th>Compte</th>
<th>Droits d’accès</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Utilisateurs authentifiés distants</td>
<td>Non accordé par défaut. <strong>Windows Server 2003 avec SP1 : SERVICE_USER_DEFINED_CONTROL</strong><br/> <strong>Windows Server 2003 et Windows XP :</strong> Les droits d’accès pour les utilisateurs authentifiés distants sont les mêmes que pour les utilisateurs authentifiés locaux.<br/></td>
</tr>
<tr class="even">
<td>Utilisateurs authentifiés locaux (y compris LocalService et NetworkService)</td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td>LocalSystem</td>
<td><dl> <strong>READ_CONTROL</strong><br />
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong><br />
<strong>SERVICE_INTERROGATE</strong><br />
<strong>SERVICE_PAUSE_CONTINUE</strong><br />
<strong>SERVICE_QUERY_CONFIG</strong><br />
<strong>SERVICE_QUERY_STATUS</strong><br />
<strong>SERVICE_START</strong><br />
<strong>SERVICE_STOP</strong><br />
<strong>SERVICE_USER_DEFINED_CONTROL</strong><br />
</dl></td>
</tr>
<tr class="even">
<td>Administrateurs</td>
<td><dl> <strong>DELETE</strong><br />
<strong>READ_CONTROL</strong><br />
<strong>SERVICE_ALL_ACCESS</strong><br />
<strong>WRITE_DAC</strong><br />
<strong>WRITE_OWNER</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Pour effectuer des opérations, l’utilisateur doit être connecté de manière interactive ou le service doit utiliser l’un des comptes de service.

Pour obtenir ou définir le descripteur de sécurité d’un objet de service, utilisez les fonctions [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) et [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) . Pour plus d’informations, consultez [modification de la liste DACL pour un service](modifying-the-dacl-for-a-service.md).

Lorsqu’un processus utilise la fonction [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) , le système vérifie les droits d’accès demandés par rapport au descripteur de sécurité de l’objet de service.

L’octroi de certains droits d’accès à des utilisateurs non approuvés (tels que la **\_ \_ configuration** de la modification du service ou l' **\_ arrêt du service**) peut leur permettre d’interférer avec l’exécution de votre service et éventuellement de les autoriser à exécuter des applications sous le compte LocalSystem.

Quand la [**fonction EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) est appelée, si l’appelant n’a pas le droit d’accès à l’état de la **\_ requête \_ de service** à un service, le service est omis en mode silencieux de la liste des services renvoyés au client.

 

