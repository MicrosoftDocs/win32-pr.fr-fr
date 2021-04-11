---
title: Fonctions de gestion de la réplication et du contrôleur de domaine
description: Cette rubrique contient la liste des fonctions utilisées pour le contrôleur de domaine et la gestion de la réplication.
ms.assetid: a92783c2-ffb8-473e-8484-1c05ca5453ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00660658874bad4e34a8f6917e08289007cec4d7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031027"
---
# <a name="domain-controller-and-replication-management-functions"></a>Fonctions de gestion de la réplication et du contrôleur de domaine

Le contrôleur de domaine (DC) et les fonctions de gestion de la réplication fournissent des outils pour rechercher des données sur un contrôleur de domaine, convertir les noms d’objets réseau entre différents formats, manipuler des noms de principal du service (SPN) et des agents de service d’annuaire (DSA) et gérer la réplication de serveurs. Les fonctions suivantes permettent aux développeurs de travailler avec les contrôleurs de domaine, la réplication et le service d’annuaire :

-   [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)
-   [**DsBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbinda)
-   [**DsBindingSetTimeout**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindingsettimeout)
-   [**DsBindToISTG**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindtoistga)
-   [**DsBindWithCred**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithcreda)
-   [**DsBindWithSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithspna)
-   [**DsBindWithSpnEx**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithspnexa)
-   [**DsClientMakeSpnForTargetServer**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsclientmakespnfortargetservera)
-   [**DsCrackNames**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dscracknamesa)
-   [**DsCrackSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dscrackspna)
-   [**DsCrackUnquotedMangledRdn**](/windows/desktop/api/Dsparse/nf-dsparse-dscrackunquotedmangledrdna)
-   [**DsFreeDomainControllerInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreedomaincontrollerinfoa)
-   [**DsFreeNameResult**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreenameresulta)
-   [**DsFreePasswordCredentials**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreepasswordcredentials)
-   [**DsFreeSchemaGuidMap**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreeschemaguidmapa)
-   [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya)
-   [**DsGetDomainControllerInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa)
-   [**DsGetRdnW**](/windows/desktop/api/Dsparse/nf-dsparse-dsgetrdnw)
-   [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna)
-   [**DsInheritSecurityIdentity**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsinheritsecurityidentitya)
-   [**DsIsMangledDn**](/windows/desktop/api/Dsparse/nf-dsparse-dsismangleddna)
-   [**DsIsMangledRdnValue**](/windows/desktop/api/Dsparse/nf-dsparse-dsismangledrdnvaluea)
-   [**DsListDomainsInSite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistdomainsinsitea)
-   [**DsListInfoForServer**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistinfoforservera)
-   [**DsListRoles**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistrolesa)
-   [**DsListServersForDomainInSite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistserversfordomaininsitea)
-   [**DsListServersInSite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistserversinsitea)
-   [**DsListSites**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistsitesa)
-   [**DsMakePasswordCredentials**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa)
-   [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna)
-   [**DsMapSchemaGuids**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsmapschemaguidsa)
-   [**DsQuerySitesByCost**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsquerysitesbycosta)
-   [**DsQuerySitesFree**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsquerysitesfree)
-   [**DsQuoteRdnValue**](/windows/desktop/api/Dsparse/nf-dsparse-dsquoterdnvaluea)
-   [**DsRemoveDsDomain**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsremovedsdomaina)
-   [**DsRemoveDsServer**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsremovedsservera)
-   [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda)
-   [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck)
-   [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela)
-   [**DsReplicaFreeInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicafreeinfo)
-   [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow)
-   [**DsReplicaGetInfo2**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfo2w)
-   [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya)
-   [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca)
-   [**DsReplicaSyncAll**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasyncalla)
-   [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa)
-   [**DsReplicaVerifyObjects**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaverifyobjectsa)
-   [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna)
-   [**DsUnBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsunbinda)
-   [**DsUnquoteRdnValue**](/windows/desktop/api/Dsparse/nf-dsparse-dsunquoterdnvaluea)
-   [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)
-   [**SyncUpdateProc**](/previous-versions/windows/desktop/legacy/ms677968(v=vs.85))

La plupart de ces fonctions nécessitent un handle lié au service d’annuaire. Les fonctions [**DsBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbinda) et [**DsBindWithCred**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithcreda) démarrent une session RPC avec un contrôleur de domaine particulier, puis lient un handle au service d’annuaire et retournent le descripteur. Lorsque le descripteur n’est plus nécessaire, utilisez la fonction [**DsUnBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsunbinda) pour mettre fin à la session RPC et annuler la liaison du descripteur.

La réplication se produit entre un serveur source et un serveur de destination. Un serveur source gère une liste de serveurs de destination vers laquelle il doit répliquer, et un serveur de destination gère une liste de serveurs source à partir desquels il reçoit la réplication. Utilisez la fonction [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda) pour ajouter à la liste des serveurs source sur un serveur de destination et utilisez la fonction [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela) pour supprimer les références de la liste serveur source sur un serveur de destination. La fonction [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya) peut être utilisée pour modifier une référence de serveur source existante sur un serveur de destination. Pour modifier la liste des serveurs de destination sur un serveur source, utilisez la fonction [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa) .

La réplication réelle est effectuée par les fonctions [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) et [**DsReplicaSyncAll**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasyncalla) . La fonction **DsReplicaSync** synchronise un serveur de destination spécifique avec un seul serveur source. Utilisez la fonction **DsReplicaSyncAll** pour synchroniser un serveur de destination avec tous les autres serveurs du site.

 

 