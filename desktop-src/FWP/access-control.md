---
title: Access Control (plateforme de filtrage Windows)
description: Dans la plateforme de filtrage Windows (WFP), le service de moteur de filtrage de base (BFE) implémente le modèle de contrôle d’accès Windows standard basé sur les jetons d’accès et les descripteurs de sécurité.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0df63b6fe92b18614a7ccf205ccf826927664ee
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104321370"
---
# <a name="access-control-windows-filtering-platform"></a>Access Control (plateforme de filtrage Windows)

Dans la plateforme de filtrage Windows (WFP), le service de moteur de filtrage de base (BFE) implémente le [modèle de contrôle d’accès Windows](/windows/desktop/SecAuthZ/access-control-model) standard basé sur les jetons d’accès et les descripteurs de sécurité.

## <a name="access-control-model"></a>Modèle de Access Control

Des descripteurs de sécurité peuvent être spécifiés lors de l’ajout de nouveaux objets WFP, tels que des filtres et des sous-couches. Les descripteurs de sécurité sont gérés à l’aide des fonctions de gestion WFP **Fwpm \* GetSecurityInfo0** et **Fwpm \* SetSecurityInfo0**, où * *\** _ correspond au nom de l’objet WFP. Ces fonctions sont sémantiquement identiques aux fonctions Windows [_ *GetSecurityInfo* *](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) et [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

> [!Note]  
> Les fonctions **Fwpm \* SetSecurityInfo0** ne peuvent pas être appelées à partir d’une transaction explicite.

 

> [!Note]  
> Les **fonctions \* SetSecurityInfo0 Fwpm** peuvent uniquement être appelées à partir d’une session dynamique s’ils sont utilisés pour gérer un objet dynamique créé au cours de la même session.

 

Le descripteur de sécurité par défaut pour le moteur de filtre (l’objet moteur racine dans le diagramme ci-dessous) est le suivant.

-   Accordez des droits d’accès **génériques \_ tous** (GA) au groupe Administrateurs intégré.
-   Octroie des droits d’accès génériques **\_ en** **\_ écriture** générique ( **EG \_** ) aux opérateurs de configuration de réseau.
-   Accordez des droits d’accès **GRGWGX** aux identificateurs de sécurité de service (SSID) suivants : mpssvc (pare-feu Windows), NapAgent (agent de protection d’accès réseau), policyagent (agent de stratégie IPSec), RPCSS (appel de procédure distante) et WdiServiceHost (hôte de service de diagnostic).
-   Accordez la classification **FWPM \_ ACTRL \_ Open** et **FWPM \_ ACTRL \_** à tout le monde. (Il s’agit de droits d’accès spécifiques à WFP, décrits dans le tableau ci-dessous.)

Les descripteurs de sécurité par défaut restants sont dérivés de l’héritage.

Certains contrôles d’accès, par exemple, pour les appels de fonction **Fwpm \* Add0**, **Fwpm \* CreateEnumHandle0**, **Fwpm \* SubscribeChanges0** , ne peuvent pas être effectués au niveau de l’objet individuel. Pour ces fonctions, il existe des objets conteneurs pour chaque type d’objet. Pour les types d’objet standard (par exemple, fournisseurs, légendes, filtres), les fonctions **Fwpm \* GetSecurityInfo0** et **Fwpm \* SetSecurityInfo0** existantes sont surchargées, de sorte qu’un paramètre **GUID** null identifie le conteneur associé. Pour les autres types d’objets (par exemple, les événements réseau et les associations de sécurité IPsec), il existe des fonctions explicites pour la gestion des informations de sécurité du conteneur.

BFE prend en charge l’héritage automatique des entrées de contrôle d’accès (DACL) de liste de Access Control discrétionnaire. BFE ne prend pas en charge les ACE du système Access Control List (SACL). Les objets héritent des ACE de leur conteneur. Les conteneurs héritent des ACE du moteur de filtre. Les chemins de propagation sont indiqués dans le diagramme ci-dessous.

![Diagramme qui affiche les chemins d’accès de propagation de l’ACE, commençant par’Engine'.](images/access-control.jpg)

Pour les types d’objet standard, BFE applique tous les droits d’accès génériques et standard. De plus, WFP définit les droits d’accès spécifiques suivants.



| Droit d’accès à WFP                                                                                                                        | Description                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ Add**<br/>                                       | Obligatoire pour ajouter un objet à un conteneur.<br/>                                                                                                                     |
| <span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ Ajouter un \_ lien**<br/>                       | Requis pour créer une association à un objet. Par exemple, pour ajouter un filtre qui fait référence à une légende, l’appelant doit disposer d’un lien ajouter un \_ accès à la légende.<br/> |
| <span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Read \_ TXN**<br/>    | Requis pour commencer une transaction de lecture explicite.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Write \_ TXN**<br/> | Requis pour commencer une transaction d’écriture explicite.<br/>                                                                                                              |
| <span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_classification FWPM ACTRL \_**<br/>                        | Requis pour classer par rapport à une couche en mode utilisateur.<br/>                                                                                                               |
| <span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL, \_ énumération**<br/>                                    | Requis pour énumérer les objets dans un conteneur. Toutefois, l’énumérateur retourne uniquement les objets auxquels l’appelant a \_ \_ accès en lecture FWPM ACTRL.<br/>              |
| <span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ Open**<br/>                                    | Requis pour ouvrir une session avec BFE.<br/>                                                                                                                          |
| <span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ lecture**<br/>                                    | Requis pour lire les propriétés d’un objet.<br/>                                                                                                                      |
| <span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**\_statistiques de \_ lecture FWPM ACTRL \_**<br/>                 | Requis pour lire les statistiques.<br/>                                                                                                                                  |
| <span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**abonnement à FWPM \_ ACTRL \_**<br/>                     | Requis pour s’abonner aux notifications. Les abonnés reçoivent uniquement des notifications pour les objets auxquels ils disposent d’un \_ \_ accès en lecture FWPM ACTRL.<br/>                 |
| <span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ Write**<br/>                                 | Requis pour définir les options du moteur.<br/>                                                                                                                               |



 

BFE ignore toutes les vérifications d’accès pour les appelants en mode noyau.

Pour empêcher les administrateurs de se verrouiller eux-mêmes, les membres du groupe Administrateurs intégré bénéficient toujours de l’autorisation **FWPM \_ ACTRL \_ Open** sur l’objet moteur. Ainsi, un administrateur peut récupérer l’accès en suivant les étapes ci-dessous.

-   Activez le privilège **se \_ prendre possession du \_ \_ nom** .
-   Appelez [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). L’appel a lieu car l’appelant est membre des administrateurs intégrés.
-   Prendre possession de l’objet moteur. Cela est dû au fait que l’appelant a le privilège **se \_ prendre \_ possession du \_ nom** .
-   Mettez à jour la liste DACL. Cela est dû au fait que le propriétaire a toujours un accès en écriture à la **\_ DAC**

Dans la mesure où BFE prend en charge son propre audit personnalisé, il ne génère pas d’audits d’accès aux objets génériques. Par conséquent, la liste SACL est ignorée.

## <a name="wfp-required-access-rights"></a>Droits d’accès requis pour WFP

Le tableau ci-dessous montre les droits d’accès requis par les fonctions WFP pour accéder à différents objets de plateforme de filtrage. Les **\* *fonctions FwpmFilter _ sont répertoriées comme exemple pour accéder aux objets standard. Toutes les autres fonctions qui accèdent aux objets standard suivent le* \*** modèle d’accès aux fonctions _ FwpmFilter.



Fonction

Objet vérifié

Accès obligatoire

[**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

Moteur

**FWPM \_ ACTRL \_ Open**

[**FwpmEngineGetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

Moteur

**FWPM \_ ACTRL \_ lecture**

[**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

Moteur

**FWPM \_ ACTRL \_ Write**

[**FwpmSessionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

Moteur

**FWPM \_ ACTRL, \_ énumération**

[**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

Moteur

**FWPM \_ ACTRL \_ Begin \_ Read \_ TXN**  &  **FWPM \_ ACTRL \_ Begin \_ Write \_ TXN**

[**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Fournisseur de conteneurs<br/> Couche<br/> Sub-Layer<br/> Légende<br/> Contexte du fournisseur<br/>

**FWPM \_ ACTRL \_ ADDFWPM \_ ACTRL \_ Ajouter un \_ lien**<br/> **FWPM \_ ACTRL \_ Ajouter un \_ lien**<br/> **FWPM \_ ACTRL \_ Ajouter un \_ lien**<br/> **FWPM \_ ACTRL \_ Ajouter un \_ lien**<br/> **FWPM \_ ACTRL \_ Ajouter un \_ lien**<br/>

[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)<br/>

Filtrer

**DELETE**

[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)<br/>

Filtrer

**FWPM \_ ACTRL \_ lecture**

[**FwpmFilterCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

Filtre de conteneur<br/>

**FWPM \_ ACTRL \_ ENUMFWPM \_ ACTRL \_ lecture**<br/>

[**FwpmFilterSubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

Conteneur

**abonnement à FWPM \_ ACTRL \_**

[**FwpmFilterSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

Conteneur

**FWPM \_ ACTRL \_ lecture**

[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

BD IPsec SA

**\_statistiques de \_ lecture FWPM ACTRL \_**

[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)<br/> [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

BD IPsec SA

**FWPM \_ ACTRL \_ Add**

[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)<br/>

BD IPsec SA

**DELETE**

[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

BD IPsec SA

**FWPM \_ ACTRL \_ lecture**

[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)<br/>

BD IPsec SA

**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ lecture**

[**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

BD IKE SA

**\_statistiques de \_ lecture FWPM ACTRL \_**

[**IkeextSaDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

BD IKE SA

**DELETE**

[**IkeextSaGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

BD IKE SA

**FWPM \_ ACTRL \_ lecture**

[**IkeextSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

BD IKE SA

**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ lecture**

[**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

Conteneur

**FWPM \_ ACTRL, \_ énumération**

[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)<br/>

Aucune vérification d’accès supplémentaire au-delà de celles pour les filtres individuels et les contextes de fournisseur



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Droits d’accès standard**](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Modèle de contrôle d’accès Windows](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[**Identificateurs des droits d’accès à la plateforme de filtrage Windows**](access-right-identifiers.md)
</dt> </dl>

 

