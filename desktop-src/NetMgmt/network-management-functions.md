---
title: Fonctions de gestion de réseau
description: Les fonctions de gestion de réseau peuvent être regroupées comme suit.
ms.assetid: dd159e2e-f37e-46b2-b980-008b73d40b39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a169d097fbe86c95aa9aa3120c3f732a8edd2c0
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "106542854"
---
# <a name="network-management-functions"></a>Fonctions de gestion de réseau

Les fonctions de gestion de réseau peuvent être regroupées comme suit.

## <a name="alert-functions"></a>Fonctions d’alerte



| Fonction                                   | Description                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Avertit tous les clients inscrits qu’un événement particulier s’est produit.                                                                                                                                  |
| [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Simplifie la notification des clients inscrits qu’un événement particulier s’est produit, car, contrairement à **NetAlertRaise**, **NetAlertRaiseEx** ne nécessite pas de structure d' [**\_ alerte STD**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) . |



 

## <a name="api-buffer-functions"></a>Fonctions de mémoire tampon d’API



| Fonction                                                 | Description                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Alloue de la mémoire à partir du tas. Appelez cette fonction lorsque vous avez besoin d’une compatibilité avec la fonction **NetApiBufferFree** . |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Libère de la mémoire allouée par la fonction **NetApiBufferAllocate** et d’autres fonctions de gestion de réseau.                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Modifie la taille d’une mémoire tampon allouée par un appel à la fonction **NetApiBufferAllocate** .                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Retourne la taille, en octets, d’une mémoire tampon allouée par un appel à la fonction **NetApiBufferAllocate** .                     |



 

## <a name="azure-active-directory-join-information-functions"></a>Fonctions d’informations de jointure Azure Active Directory



| Fonction                                                       | Description                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetFreeAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netfreeaadjoininformation) | Libère la mémoire allouée pour la structure d' [**\_ \_ informations de jointure DSREG**](/windows/desktop/api/lmjoin/ns-lmjoin-dsreg_join_info) spécifiée, qui contient des informations de jointure pour un locataire et que vous avez récupérée en appelant la fonction [**NetGetAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation) . |
| [**NetGetAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation)   | Récupère les informations de jointure pour le locataire spécifié. Cette fonction examine les informations de jointure pour Microsoft Azure Active Directory et le compte professionnel ajouté par l’utilisateur actuel.                                                                     |



 

## <a name="directory-service-and-domain-join-functions"></a>Fonctions de service d’annuaire et de jonction de domaine



| Fonction                                                                             | Description                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)                   | Ajoute un autre nom pour l’ordinateur spécifié.                                                                                                                                                                                                                      |
| [**NetCreateProvisioningPackage**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                  | Provisionne un compte d’ordinateur pour une utilisation ultérieure dans une opération de jonction de domaine hors connexion.                                                                                                                                                                                        |
| [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)                       | Énumère les noms de l’ordinateur spécifié.                                                                                                                                                                                                                            |
| [**NetGetJoinableOUs**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                                       | Récupère une liste d’unités d’organisation dans laquelle un compte d’ordinateur peut être créé.                                                                                                                                                                              |
| [**NetGetJoinInformation**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                               | Récupère les informations sur l’état de la jointure pour l’ordinateur spécifié.                                                                                                                                                                                                           |
| [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                               | Joint un ordinateur à un groupe de travail ou à un domaine.                                                                                                                                                                                                                              |
| [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                   | Provisionne un compte d’ordinateur pour une utilisation ultérieure dans une opération de jonction de domaine hors connexion.                                                                                                                                                                                       |
| [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)             | Supprime un autre nom pour l’ordinateur spécifié.                                                                                                                                                                                                                   |
| [**NetRenameMachineInDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)                         | Modifie le nom d’un ordinateur dans un domaine.                                                                                                                                                                                                                             |
| [**NetRequestOfflineDomainJoin**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)                   | S’exécute localement sur un ordinateur pour modifier une image du système d’exploitation Windows montée sur un volume. Le Registre est chargé pour l’image et l’approvisionnement des données BLOB est écrit là où elles peuvent être récupérées au cours de la phase d’achèvement d’une opération de jonction de domaine hors connexion.     |
| [**NetRequestProvisioningPackageInstall**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall) | S’exécute localement sur un ordinateur pour modifier une image du système d’exploitation Windows montée sur un volume. Le Registre est chargé à partir de l’image et les données du package de configuration sont écrites à l’emplacement où elles peuvent être récupérées au cours de la phase d’achèvement d’une opération de jonction de domaine hors connexion. |
| [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)                       | Définit le nom de l’ordinateur principal pour l’ordinateur spécifié.                                                                                                                                                                                                              |
| [**NetUnjoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                                           | Disjoint un ordinateur d’un groupe de travail ou d’un domaine.                                                                                                                                                                                                                        |
| [**NetValidateName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                                           | Vérifie la validité d’un nom d’ordinateur, d’un nom de groupe de travail ou d’un nom de domaine.                                                                                                                                                                                               |



 

## <a name="get-functions"></a>Fonctions d’extraction



| Fonction                                                               | Description                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetGetAnyDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Retourne le nom d’un contrôleur de domaine pour un domaine qui est directement approuvé par un serveur spécifié.                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Retourne le nom du contrôleur de domaine principal (PDC) pour le domaine spécifié.                                                        |
| [**NetGetDisplayInformationIndex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Retourne l’index de la première entrée d’informations d’affichage dont le nom commence par une chaîne spécifiée ou qui suit la chaîne par ordre alphabétique. |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Retourne des informations sur le compte de l’utilisateur, de l’ordinateur ou du groupe global.                                                                             |



 

## <a name="group-functions"></a>Fonctions de groupe



| Fonction                                     | Description                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | Crée un groupe global.                                                           |
| [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | Ajoute un utilisateur à un groupe global existant.                                        |
| [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | Supprime un groupe global, que le groupe ait ou non des membres.                  |
| [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | Supprime un nom d’utilisateur d’un groupe global.                                        |
| [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | Répertorie tous les groupes globaux sur un serveur.                                              |
| [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | Retourne des informations sur un groupe global particulier.                              |
| [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | Répertorie tous les membres d’un groupe global particulier.                                   |
| [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | Définit des informations générales sur un groupe global.                                    |
| [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | Attribue des membres à un nouveau groupe global ; remplace les membres d’un groupe existant. |



 

## <a name="local-group-functions"></a>Fonctions de groupe locales



| Fonction                                                   | Description                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | Crée un groupe local.                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | Ajoute un ou plusieurs utilisateurs ou groupes globaux à un groupe local existant.     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | Supprime un groupe local, en supprimant tous les membres existants du groupe.    |
| [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | Supprime un ou plusieurs membres d’un groupe local existant.               |
| [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | Retourne des informations sur chaque compte de groupe local sur un serveur.         |
| [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | Retourne des informations sur un compte de groupe local particulier sur un serveur. |
| [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | Répertorie tous les membres d’un groupe local spécifié.                           |
| [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | Définit des informations générales sur un groupe local.                           |
| [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | Attribue des membres à un groupe local.                                       |



 

## <a name="message-functions"></a>Fonctions de message



| Fonction                                               | Description                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Envoie un message à un alias de message enregistré.                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Inscrit un alias de message dans la table de noms de message.                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Supprime un alias de message de la table de noms de messages.                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Répertorie tous les alias de messages stockés dans la table des noms de message.                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Retourne des informations sur un alias de message particulier dans la table des noms de messages. |



 

## <a name="netfile-functions"></a>Fonctions Netfile



| Fonction                                | Description                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | Force la fermeture d’une ressource.                                          |
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | Retourne des informations sur les fichiers ouverts sur un serveur.                    |
| [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | Retourne des informations sur une ouverture particulière d’une ressource de serveur. |



 

## <a name="remote-utility-functions"></a>Fonctions utilitaires distantes



| Fonction                                                       | Description                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**NetRemoteComputerSupports**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotecomputersupports) | Interroge le redirecteur pour récupérer les fonctionnalités facultatives prises en charge par un système distant. |
| [**NetRemoteTOD**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotetod)                           | Permet aux applications d’accéder aux informations relatives à l’heure d’un jour sur un serveur distant.          |



 

## <a name="schedule-functions"></a>Fonctions de planification



| Fonction                                                                     | Description                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | Soumet un travail à exécuter à une date et une heure futures spécifiées.        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | Annule une plage de travaux en file d’attente d’exécution sur un ordinateur.             |
| [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | Répertorie les travaux en file d’attente sur un ordinateur spécifié.                   |
| [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | Retourne des informations sur un travail particulier mis en file d’attente sur un ordinateur. |
| [**GetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | Récupère le nom du compte de service AT.                           |
| [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | Définit le nom du compte de service AT et le mot de passe.                   |



 

## <a name="server-functions"></a>Fonctions du serveur



| Fonction                                       | Description                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Retourne une liste de lecteurs de disque locaux sur un serveur.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Répertorie tous les serveurs visibles d’un type particulier (ou types) dans le domaine spécifié. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Retourne les informations de configuration relatives à un serveur spécifié.                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Définit les paramètres de fonctionnement d’un serveur.                                        |



 

## <a name="server-and-workstation-transport-functions"></a>Fonctions de transport serveur et station de travail



| Fonction                                                     | Description                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetServerComputerNameAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | Lie un nom de serveur émulé à chacun des protocoles de transport sur lesquels un serveur est actif. (Combine les fonctionnalités de la fonction [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) et de la fonction [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) .)                                            |
| [**NetServerComputerNameDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | Déconnecte chaque protocole de transport réseau d’un nom de serveur émulé défini par un appel précédent à la fonction **NetServerComputerNameAdd** .                                                                                                                                                                               |
| [**NetServerTransportAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | Lie le serveur spécifié au protocole de transport. (Cette fonction prend en charge uniquement le niveau d’information [**Server \_ transport \_ information \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) .)                                                                                                                                                |
| [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | Lie le serveur spécifié au protocole de transport. (Cette fonction étendue prend en charge les niveaux d’information Server transport information [**\_ \_ \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1), [**Server \_ transport \_ information \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)et [**Server \_ transport \_ information \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) .) |
| [**NetServerTransportDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | Déconnecte le protocole de transport du serveur.                                                                                                                                                                                                                                                                         |
| [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | Énumère les protocoles de transport gérés par le serveur.                                                                                                                                                                                                                                                                   |
| [**NetWkstaTransportEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum)       | Répertorie les protocoles de transport qui sont gérés par le redirecteur.                                                                                                                                                                                                                                                           |



 

## <a name="use-functions"></a>Utiliser des fonctions



| Fonction                               | Description                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Crée une connexion entre un ordinateur local et un serveur.                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Met fin à une connexion à une ressource partagée.                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Répertorie toutes les connexions en cours entre l’ordinateur local et les ressources sur les serveurs distants. |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Retourne des informations sur une connexion à une ressource partagée.                              |



 

## <a name="user-functions"></a>Fonctions utilisateur



| Fonction                                               | Description                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Ajoute un compte d’utilisateur et attribue un mot de passe et un niveau de privilège.     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Modifie le mot de passe d’un utilisateur pour un serveur réseau ou un domaine spécifié. |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Supprime un compte d’utilisateur du serveur.                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Répertorie tous les comptes d’utilisateur sur un serveur.                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Retourne une liste de noms de groupes globaux auxquels appartient un utilisateur.       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Retourne des informations sur un compte d’utilisateur particulier sur un serveur.    |
| [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Retourne la liste des noms de groupes locaux auxquels appartient un utilisateur.        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Définit les appartenances aux groupes globaux pour un compte d’utilisateur spécifié.         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Définit le mot de passe et d’autres éléments d’un compte d’utilisateur.             |



 

## <a name="user-modals-functions"></a>Fonctions modales utilisateur



| Fonction                                     | Description                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Retourne des informations globales pour tous les utilisateurs et groupes globaux dans la base de données de sécurité, qui est la base de données du gestionnaire de comptes de sécurité (SAM) ou, dans le cas des contrôleurs de domaine, la Active Directory. |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Définit des informations globales pour tous les utilisateurs et groupes globaux dans la base de données de sécurité.                                                                                                                       |



 

## <a name="validation-functions"></a>Fonctions de validation



| Fonction                                                               | Description                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Libère la mémoire allouée par la fonction [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) pour le paramètre *OutputArg* ,                                                                                      |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Permet à une application de vérifier la conformité du mot de passe par rapport à une base de données de comptes fournie par l’application et de vérifier que les mots de passe répondent aux exigences de complexité, d’antériorité, de longueur minimale et d’historique de la stratégie de mot de passe. |



 

## <a name="workstation-and-workstation-user-functions"></a>Fonctions utilisateur de station de travail et de station de travail



| Fonction                                           | Description                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo)         | Retourne des informations sur les éléments de configuration d’une station de travail.             |
| [**NetWkstaSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo)         | Configure une station de travail.                                                           |
| [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | Répertorie des informations sur tous les utilisateurs actuellement connectés à la station de travail.           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | Retourne des informations sur un utilisateur actuellement connecté.                             |
| [**NetWkstaUserSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | Définit les informations spécifiques à l’utilisateur pour les éléments de configuration d’une station de travail. |



 

## <a name="obsolete-functions"></a>Fonctions obsolètes

-   [**NetAccessAdd**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessadd)
-   [**NetAccessCheck**](/previous-versions/windows/desktop/legacy/aa370291(v=vs.85))
-   [**NetAccessDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessdel)
-   [**NetAccessEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessenum)
-   [**NetAccessGetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetinfo)
-   [**NetAccessGetUserPerms**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetuserperms)
-   [**NetAccessSetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccesssetinfo)
-   [**NetAuditClear**](netauditclear.md)
-   [**NetAuditRead**](netauditread.md)
-   [**NetAuditWrite**](netauditwrite.md)
-   [**NetConfigGet**](netconfigget.md)
-   [**NetConfigGetAll**](netconfiggetall.md)
-   [**NetConfigSet**](netconfigset.md)
-   [**NetErrorLogClear**](neterrorlogclear.md)
-   [**NetErrorLogRead**](neterrorlogread.md)
-   [**NetErrorLogWrite**](neterrorlogwrite.md)
-   [**NetLocalGroupAddMember**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupaddmember)
-   [**NetLocalGroupDelMember**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdelmember)
-   [**NetServiceControl**](netservicecontrol.md)
-   [**NetServiceEnum**](netserviceenum.md)
-   [**NetServiceGetInfo**](netservicegetinfo.md)
-   [**NetServiceInstall**](netserviceinstall.md)
-   [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)
-   [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de réseau Windows](/windows/desktop/WNet/windows-networking-functions)
</dt> </dl>

 

 