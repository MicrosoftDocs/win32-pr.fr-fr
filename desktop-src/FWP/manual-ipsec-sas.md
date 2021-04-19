---
title: SA manuelle
description: Le scénario de stratégie IPsec d’association de sécurité manuelle permet aux appelants de contourner les modules de génération de clé IPsec intégrés (IKE et AuthIP) en spécifiant directement les associations de sécurité IPsec pour sécuriser tout le trafic réseau.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beeef4486e3a07dea2e83d924c2354a3dabca241
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314572"
---
# <a name="manual-sa"></a>SA manuelle

Le scénario de stratégie IPsec d’association de sécurité manuelle permet aux appelants de contourner les modules de génération de clé IPsec intégrés (IKE et AuthIP) en spécifiant directement les associations de sécurité IPsec pour sécuriser tout le trafic réseau.

Un exemple de scénario d’association de sécurité manuelle possible est « ajouter une paire SA IPsec pour sécuriser le trafic de données de monodiffusion entre les adresses IP 1.1.1.1 & 2.2.2.2, sauf ICMP, à l’aide du mode de transport IPsec ».

> [!Note]  
> Les étapes suivantes doivent être exécutées sur les deux ordinateurs avec des adresses IP définies correctement.

 

Pour implémenter cet exemple par programme, utilisez la configuration WFP suivante.

<dl>

**Au niveau de la \_ couche FWPM \_ \_ transport entrant \_ V {4 \| 6} configurer les règles de filtrage par paquet entrantes**  

1.  Ajoutez un filtre avec les propriétés suivantes. 

    | Filter (propriété)                                                   | Valeur                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **\_ \_ \_ adresse locale IP de condition FWPM \_**                           | Adresse locale appropriée (1.1.1.1 ou 2.2.2.2).           |
    | **\_ \_ \_ adresse distante IP de la condition FWPM \_**                          | Adresse distante appropriée (1.1.1.1 ou 2.2.2.2).          |
    | **action. type**                                                   | **fin de l’appel à l' \_ action fwp \_ \_**                         |
    | **action. calloutKey**                                             | **FWPM \_ de \_ \_ transport entrant IPSec \_ \_ V {4 \| 6}**         |

        
2.  Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes. 

    | Filter (propriété)                                                   | Valeur                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                                |
    | **FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**             | **IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.<br/> |
    | **action. type**                                                   | **\_autorisation d’action fwp \_**                                                    |
    | **weight**                                                        | [**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**](filter-weight-identifiers.md)  |

        

**Au niveau \_ du \_ transport sortant de couche FWPM \_ \_ V {4 \| 6} configurer les règles de filtrage par paquet sortantes**  

1.  Ajoutez un filtre avec les propriétés suivantes. 

    | Filter (propriété)                                                   | Valeur                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                            |
    | **FWPM \_ Condition de filtrage d' \_ \_ \_ adresse locale de condition IP**       | Adresse locale appropriée (1.1.1.1 ou 2.2.2.2).    |
    | **FWPM \_ Condition de filtrage d' \_ \_ \_ adresse distante IP de condition**      | Adresse distante appropriée (1.1.1.1 ou 2.2.2.2).   |
    | **action. type**                                                   | **fin de l’appel à l' \_ action fwp \_ \_**                  |
    | **action. calloutKey**                                             | **FWPM \_ de \_ \_ transport sortant IPSec \_ \_ V {4 \| 6}** |

        
2.  Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes. 

    | Filter (propriété)                                                   | Valeur                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                                |
    | **FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**             | **IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.<br/> |
    | **action. type**                                                   | **\_autorisation d’action fwp \_**                                                    |
    | **weight**                                                        | **\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**                                   |

        

**Configurer des associations de sécurité entrantes et sortantes**

1.  Appelez [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)avec le paramètre *outboundTraffic* contenant les adresses IP sous la forme 1.1.1.1 & 2.2.2.2 et **ipsecFilterId** comme LUID du filtre de la légende IPSec de la couche de transport sortant ajoutée ci-dessus.
2.  Appelez [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0), avec le paramètre *ID* contenant l’ID de contexte renvoyé par [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), et le paramètre *getSpi* contenant les adresses IP sous la forme 1.1.1.1 & 2.2.2.2 et **ipsecFilterId** comme LUID du filtre de la légende IPSec de la couche transport entrante ajoutée ci-dessus. La valeur SPI renvoyée est destinée à être utilisée comme le SPI entrant de l’administrateur système par l’ordinateur local et comme le SPI sortant de l’administrateur système par la machine distante correspondante. Les deux ordinateurs doivent utiliser des moyens hors bande pour échanger les valeurs SPI.
3.  Appelez [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), avec le paramètre *ID* contenant l’ID de contexte renvoyé par [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), et le paramètre *inboundBundle* décrivant les propriétés du bundle de l’Association de sécurité entrante (par exemple, le SPI entrant sa, le type de transformation, les types d’algorithmes, les clés, etc.).
4.  Appelez [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), avec le paramètre *ID* contenant l’ID de contexte renvoyé par [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0), et le paramètre *outboundBundle* décrivant les propriétés du bundle de la sa sortante (par exemple, le SPI sortant sa, le type de transformation, les types d’algorithmes, les clés, etc.).

  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de code : génération manuelle de la clé SA](manual-sa-keying.md)
</dt> <dt>

[**Identificateurs de légende intégrés**](built-in-callout-identifiers.md)
</dt> <dt>

[**Filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

