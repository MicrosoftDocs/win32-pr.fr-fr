---
title: Configuration IPsec
description: Windows la plateforme de filtrage (WFP) est la plateforme sous-jacente pour Windows pare-feu avec sécurité avancée.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34cf20fc8c95aafe3c387195b02468cec3ce884cc97287adde44a594305ee189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069012"
---
# <a name="ipsec-configuration"></a>Configuration IPsec

Windows la plateforme de filtrage (WFP) est la plateforme sous-jacente pour Windows pare-feu avec sécurité avancée. WFP est utilisé pour configurer les règles de filtrage réseau, qui incluent des règles qui régissent la sécurisation du trafic réseau avec IPsec. les développeurs d’applications peuvent configurer IPsec directement à l’aide de l’API WFP, afin de tirer parti d’un modèle de filtrage du trafic réseau plus granulaire que le modèle exposé via le composant logiciel enfichable MMC (Microsoft Management Console) pour Windows pare-feu avec fonctions avancées de sécurité.

## <a name="what-is-ipsec"></a>Qu’est-ce qu’IPsec ?

La sécurité du protocole Internet (IPsec) est un ensemble de protocoles de sécurité utilisés pour transférer des paquets IP de façon confidentielle sur Internet. IPsec est obligatoire pour toutes les implémentations IPv6 et facultatif pour IPv4.

Le trafic IP sécurisé comporte deux en-têtes IPsec facultatifs, qui identifient les types de protection par chiffrement appliqués au paquet IP et incluent des informations pour le décodage du paquet protégé.

L’en-tête ESP (Encapsulating Security Payload) est utilisé pour la confidentialité et la protection contre les modifications malveillantes en effectuant l’authentification et le chiffrement facultatif. Il peut être utilisé pour le trafic qui traverse les routeurs de traduction d’adresses réseau (NAT).

L’en-tête d’authentification (AH) est utilisé uniquement pour la protection contre les modifications malveillantes en effectuant l’authentification. Elle ne peut pas être utilisée pour le trafic qui traverse les routeurs NAT.

Pour plus d’informations sur IPsec, consultez également :

<dl>

[Informations techniques de référence sur IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))  
</dl>

## <a name="what-is-ike"></a>Qu’est-ce que IKE ?

protocole IKE (Internet Key Exchange) (IKE) est un protocole d’échange de clés qui fait partie de l’ensemble de protocoles IPsec. IKE est utilisé lors de la configuration d’une connexion sécurisée et effectue l’échange sécurisé de clés secrètes et d’autres paramètres liés à la protection sans l’intervention de l’utilisateur.

Pour plus d’informations sur IKE, voir aussi :

<dl>

[protocole IKE (Internet Key Exchange)](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))  
</dl>

## <a name="what-is-authip"></a>Présentation d’AuthIP

Protocole Authenticated IP (Authenticated Internet Protocol) (AuthIP) est un nouveau protocole d’échange de clés qui étend IKE comme suit.

<dl> Alors que IKE prend uniquement en charge les informations d’authentification de l’ordinateur, AuthIP prend également en charge :

-   Informations d’identification de l’utilisateur : NTLM, Kerberos, certificats.
-   Certificats d’intégrité de la protection d’accès réseau (NAP).
-   Informations d’identification anonymes, utilisées pour l’authentification facultative.
-   Combinaison d’informations d’identification ; par exemple, une combinaison d’informations d’identification Kerberos de l’ordinateur et de l’utilisateur.

  
AuthIP a un mécanisme de nouvelle tentative d’authentification qui vérifie toutes les méthodes d’authentification configurées avant l’échec de la connexion.  
AuthIP peut être utilisé avec des sockets sécurisés pour implémenter le trafic sécurisé IPsec basé sur les applications. Il offre :

-   Le chiffrement et l’authentification par socket. Pour plus d’informations, consultez [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) .
-   Emprunt d’identité du client. (IPsec emprunte l’identité du contexte de sécurité sous lequel le socket est créé.)
-   Validation du nom d’homologue entrante et sortante. Pour plus d’informations, consultez [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) .

  
</dl>

Pour plus d’informations sur AuthIP, consultez également :

<dl>

[AuthIP dans Windows Vista](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a>Qu’est-ce qu’une stratégie IPsec ?

Une stratégie IPsec est un ensemble de règles qui déterminent le type de trafic IP qui doit être sécurisé à l’aide d’IPsec et comment sécuriser ce trafic. Une seule stratégie IPsec est active sur un ordinateur à la fois.

Pour en savoir plus sur l’implémentation des stratégies IPsec, ouvrez le composant logiciel enfichable MMC stratégie de sécurité locale (secpol. msc), appuyez sur F1 pour afficher l’aide, puis sélectionnez création et utilisation des stratégies IPsec dans la table des matières.

Pour plus d’informations sur les stratégies IPsec, voir aussi :

<dl>

[Vue d’ensemble des concepts de la stratégie IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))  
[Description d’une stratégie IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a>Comment utiliser WFP pour configurer des stratégies IPsec

l’implémentation Microsoft d’IPsec utilise Windows plate-forme de filtrage pour configurer des stratégies IPsec. Les stratégies IPsec sont implémentées en ajoutant des filtres dans différentes couches WFP comme suit.

-   Au niveau de la \_ couche FWPM \_ \_ couches IKEEXT V {4 \| 6}, ajoutez des filtres qui spécifient les stratégies de négociation utilisées par les modules de génération de clé (IKE/AuthIP) pendant les échanges en mode principal (mm). Les méthodes d’authentification et les algorithmes de chiffrement sont spécifiés au niveau de ces couches.
-   Au niveau des \_ couches FWPM Layer \_ IPSec \_ V {4 \| 6}, ajoutez des filtres qui spécifient les stratégies de négociation utilisées par les modules de génération de clés en mode rapide (QM) et les échanges en mode étendu (EM). Les en-têtes IPsec (AH/ESP) et les algorithmes de chiffrement sont spécifiés au niveau de ces couches.

    Une stratégie de négociation est spécifiée comme un contexte de fournisseur de stratégie associé au filtre. Le module de génération de clés énumère les contextes du fournisseur de stratégie en fonction des caractéristiques du trafic et obtient la stratégie à utiliser pour la négociation de sécurité.

    > [!Note]  
    > L’API WFP peut être utilisée pour spécifier les associations de sécurité (SAP) directement et par conséquent pour ignorer la stratégie de négociation du module de génération de clés.

     

-   Au niveau des \_ \_ \_ couches FWPM transport entrant \_ v {4 \| 6} et \_ transport sortant de couche FWPM \_ \_ \_ v {4 \| 6}, ajoutez des filtres qui appellent des légendes et déterminent le flux de trafic à sécuriser.
-   Au niveau des \_ couches FWPM d’authentification ALE de la couche \_ ALE \_ \_ \_ , accepter les \_ couches {4 \| 6} ajoutez des filtres qui implémentent le filtrage d’identité et la stratégie par application.

Le diagramme suivant illustre l’interaction des différents composants de WFP, en ce qui concerne le fonctionnement d’IPsec.![configuration IPSec à l’aide de la plateforme de filtrage Windows](images/ipsec-configuration.jpg)

Une fois IPsec configuré, il s’intègre à WFP et étend les fonctionnalités de filtrage de WFP en fournissant des informations à utiliser comme conditions de filtrage au niveau des couches d’autorisation d’application de la couche application (ALE). Par exemple, IPsec fournit l’identité de l’utilisateur distant et de l’ordinateur distant, que WFP expose au niveau de la connexion ALE et accepte les couches d’autorisation. Ces informations peuvent être utilisées pour une autorisation d’identité à distance fine par une implémentation de pare-feu basée sur WFP.

Voici un exemple de stratégie d’isolation qui peut être implémentée à l’aide d’IPsec :

-   \_Couches FWPM \_ IKEEXT \_ V {4 \| 6} couche-authentification Kerberos.
-   \_Couches FWPM \_ IPSec \_ V {4 \| 6} couches – Ah/SHA-1.
-   \_Couche FWPM \_ transport entrant \_ \_ v {4 \| 6} et couche FWPM \_ \_ transport sortant \_ \_ v {4 \| 6} couches-détection de négociation pour tout le trafic réseau.
-   FWPM \_ \_ de l’authentification ALE de la couche ALE \_ \_ \_ \_ -accepter les couches V {4 \| 6}-IPSec requis pour tout le trafic réseau.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Couches WFP**
</dt> <dt>

[**Filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[Couches ALE](ale-layers.md)
</dt> <dt>

**Scénarios de stratégie IPsec implémentés à l’aide de l’API WFP :**
</dt> <dt>

[mode de transport](regular-transport-mode.md)
</dt> <dt>

[Mode de transport de la découverte de négociation](negotiation-discovery-transport-mode.md)
</dt> <dt>

[Mode de transport de la découverte de négociation en mode limite](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[Tunnel Mode](tunnel-mode.md)
</dt> <dt>

[Chiffrement garanti](guaranteed-encryption.md)
</dt> <dt>

[Autorisation d’identité distante](remote-identity-authorization.md)
</dt> <dt>

[SAs IPsec manuelle](manual-ipsec-sas.md)
</dt> <dt>

[Exemptions IKE/AuthIP](ike-exemptions.md)
</dt> <dt>

**Solutions IPsec :**
</dt> <dt>

[Isolation de serveur et de domaine](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))
</dt> </dl>

 

 