---
title: Fonctions du service d’annuaire (AD DS)
description: Les fonctions de service d’annuaire fournissent un utilitaire permettant de localiser un contrôleur de domaine (DC) dans un domaine Windows NT ou Windows 2000.
ms.assetid: 7b519c81-5a6c-470a-a525-1894efd53305
ms.tgt_platform: multiple
keywords:
- Fonctions du service d’annuaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b071128806926e07cf61d62e53b823d8e7e1ac
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2019
ms.locfileid: "104030695"
---
# <a name="directory-service-functions-ad-ds"></a>Fonctions du service d’annuaire (AD DS)

Les fonctions de service d’annuaire fournissent un utilitaire permettant de localiser un contrôleur de domaine (DC) dans un domaine Windows NT ou Windows 2000. L’architecture interagit avec les clients ainsi que les serveurs dans toutes les versions de Windows NT et Windows 2000. Les fonctions suivantes permettent aux développeurs de travailler avec le contrôleur de domaine et l’appartenance à un domaine dans le service d’annuaire :

-   [**DsAddressToSiteNames**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesa)
-   [**DsAddressToSiteNamesEx**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsaddresstositenamesexa)
-   [**DsDeregisterDnsHostRecords**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsderegisterdnshostrecordsa)
-   [**DsEnumerateDomainTrusts**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsenumeratedomaintrustsa)
-   [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)
-   [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea)
-   [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)
-   [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)
-   [**DsGetDcSiteCoverage**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcsitecoveragea)
-   [**DsGetForestTrustInformationW**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetforesttrustinformationw)
-   [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea)
-   [**DsMergeForestTrustInformationW**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsmergeforesttrustinformationw)
-   [**DsRoleFreeMemory**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolefreememory)
-   [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation)
-   [**DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea)

Le localisateur de contrôleur de réseau, [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea), est implémenté par le service Netlogon. Chaque contrôleur de domaine enregistre son nom DNS sur le serveur DNS et son nom NetBIOS à l’aide d’un mécanisme spécifique au transport, par exemple dans WINS. Le localisateur de contrôleur de périphérique recherche le nom, puis envoie un datagramme à, ou ping, au contrôleur de périphérique qui a enregistré le nom. Pour les noms de domaine NetBIOS, le datagramme est un message mailslot. Pour les noms de domaine DNS, le datagramme est une recherche UDP LDAP. Chacun de ces DC répond, indiquant qu’il est en cours de fonctionnement. Le premier contrôleur de périphérique à répondre est retourné à l’appelant.

Le contrôleur de périphérique retourné est mis en cache, de sorte que les appelants suivants n’ont pas besoin de répéter l’algorithme précédent et d’inciter tous les appelants à utiliser ce même contrôleur de périphérique. Cela garantit qu’un seul client dispose d’une vue cohérente du contenu du contrôleur de contenu.

Lors de la recherche d’un contrôleur de domaine par nom de domaine DNS, le localisateur de contrôleur de domaine tente de trouver un contrôleur de domaine dans le site « le plus proche ». Chaque contrôleur de domaine inscrit des enregistrements DNS supplémentaires indiquant le site dans lequel se trouve le contrôleur de domaine et les sites inclus dans le contrôleur de domaine. Le localisateur de contrôleur de domaine recherche d’abord cet enregistrement DNS spécifique au site avant de Rechercher l’enregistrement DNS qui n’est pas spécifique à un site, préférant donc un contrôleur de domaine de ce site. Lorsque le localisateur de contrôleur de domaine envoie un datagramme au contrôleur de domaine, le contrôleur de domaine recherche l’adresse IP du client dans le conteneur Configuration/sites/sous-réseau du service d’annuaire pour trouver un objet de sous-réseau. La propriété **siteObject** de l’objet sous-réseau définit le nom du site qui contient le client. Le contrôleur de site répond au test ping avec le nom du site qui contient le client, ainsi qu’un indicateur indiquant si ce contrôleur de site couvre ce site. Si le contrôleur de site n’inclut pas ce site et que le localisateur de contrôleur de site n’a pas encore trouvé de contrôleur de périphérique dans ce site, le localisateur de contrôleur de site tente à nouveau de trouver un contrôleur de site dans le site.

Pour rechercher le nom du site contenant le client, utilisez la fonction [**DsGetSiteName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetsitenamea) . Les noms des objets dans le conteneur Configuration/sites/sous-réseau doivent être des noms de sous-réseaux valides. La fonction [**DsValidateSubnetName**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsvalidatesubnetnamea) indique si un nom de sous-réseau spécifié est valide.

 

 




