---
title: Chiffrement garanti
description: Le scénario de stratégie IPsec de chiffrement garanti requiert le chiffrement IPsec pour tout le trafic correspondant. Cette stratégie doit être spécifiée conjointement avec l’une des options de la stratégie mode de transport.
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381d029b3bebc6fc6e0a438c5123bb6703bc45dd457195fa7ff8fc7268bba16f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069149"
---
# <a name="guaranteed-encryption"></a>Chiffrement garanti

Le scénario de stratégie IPsec de chiffrement garanti requiert le chiffrement IPsec pour tout le trafic correspondant. Cette stratégie doit être spécifiée conjointement avec l’une des options de la stratégie mode de transport.

Le chiffrement garanti est généralement utilisé pour chiffrer le trafic sensible pour chaque application.

Un exemple de scénario de chiffrement garanti est le suivant : « sécuriser tout le trafic de données monodiffusion, sauf ICMP, à l’aide du mode de transport IPsec, activer la découverte de négociation et exiger un chiffrement garanti pour tout le trafic de monodiffusion correspondant au port local TCP 5555 ».

Pour implémenter cet exemple par programme, utilisez la configuration WFP suivante.

<dl>

**Stratégie de négociation de l’installation de la \_ couche FWPM \_ IKEEXT \_ V {4 \| 6}**  

1.  Ajoutez l’un des contextes de fournisseur de stratégie MM suivants, ou les deux.  
    -   Pour IKE, contexte d’un fournisseur de stratégie de type FWPM \_ IPSec \_ IKE \_ mm \_ Context.
    -   Pour AuthIP, contexte du fournisseur de stratégie de type FWPM \_ IPSec \_ AuthIP \_ mm \_ Context.

    > [!Note]  
    > Un module de génération de clés commun sera négocié et la stratégie MM correspondante sera appliquée. AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.

     

2.  Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.

    | Filter (propriété)        | Valeur                                            |
    |------------------------|--------------------------------------------------|
    | Conditions de filtrage   | Vide. Tout le trafic correspond au filtre.        |
    | **providerContextKey** | GUID du contexte du fournisseur MM ajouté à l’étape 1. |

        

**Au niveau de FWPM \_ Layer \_ IPSec \_ V {4 \| 6} Setup QM et em Negotiation Policy**  

1.  Ajoutez l’un des contextes de fournisseur de stratégie de mode de transport QM suivants, ou les deux, et définissez l’indicateur de sécurité de l' [**\_ indicateur de stratégie IPSec \_ \_ ND \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .  
    -   Pour IKE, contexte du fournisseur de stratégie de type **FWPM le \_ \_ \_ \_ \_ contexte de transport QM IPsec IKE**.
    -   Pour AuthIP, contexte du fournisseur de stratégie de **type \_ FWPM \_ IPSec \_ AuthIP \_ transport \_ Context**. Ce contexte peut éventuellement contenir la stratégie de négociation en mode étendu AuthIP (EM).

    > [!Note]  
    > Un module de génération de clés commun sera négocié et la stratégie de QM correspondante sera appliquée. AuthIP est le module de génération de clé préféré si IKE et AuthIP sont pris en charge.

     

2.  Pour chacun des contextes ajoutés à l’étape 1, ajoutez un filtre avec les propriétés suivantes.

    | Filter (propriété)        | Valeur                                            |
    |------------------------|--------------------------------------------------|
    | Conditions de filtrage   | Vide. Tout le trafic correspond au filtre.        |
    | **providerContextKey** | GUID du contexte du fournisseur QM ajouté à l’étape 1. |

        

**Au niveau de la \_ couche FWPM \_ \_ transport entrant \_ V {4 \| 6} configurer les règles de filtrage par paquet entrantes**  

1.  Ajoutez un filtre avec les propriétés suivantes. 

    | Filter (propriété)                                               | Valeur                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | \_Condition de \_ filtrage \_ de \_ type d’adresse locale IP de condition FWPM \_ | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **action. type**                                               | **fin de l’appel à l' \_ action fwp \_ \_**                                                              |
    | **action. calloutKey**                                         | **FWPM \_ de \_ \_ transport entrant IPSec \_ \_ V {4 \| 6}**                                              |
    | **rawContext**                                                | [**\_sécurité de \_ \_ connexion entrante IPSec de \_ \_ contexte FWPM \_**](filter-context-identifiers.md) |

        
2.  Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.

    | Filter (propriété)                                                   | Valeur                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                                |
    | **FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**             | **IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.<br/> |
    | **action. type**                                                   | **\_autorisation d’action fwp \_**                                                    |
    | **weight**                                                        | [**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**](filter-weight-identifiers.md)  |

        

**Au niveau \_ du \_ transport sortant de couche FWPM \_ \_ V {4 \| 6} configurer les règles de filtrage par paquet sortantes**  

1.  Ajoutez un filtre avec les propriétés suivantes.

    | Filter (propriété)                                                   | Valeur                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                                               |
    | **action. type**                                                   | **fin de l’appel à l' \_ action fwp \_ \_**                                                     |
    | **action. calloutKey**                                             | **FWPM \_ de \_ \_ transport sortant IPSec \_ \_ V {4 \| 6}**                                    |
    | **rawContext**                                                    | [**\_détection de \_ \_ négociation sortante \_ IPSec \_ du contexte FWPM**](filter-context-identifiers.md) |

        
2.  Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.

    | Filter (propriété)                                                   | Valeur                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                                |
    | **FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**             | **IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.<br/> |
    | **action. type**                                                   | **\_autorisation d’action fwp \_**                                                    |
    | **weight**                                                        | **\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**                                   |

        

**Au niveau de FWPM \_ \_ , l’authentification ALE de la couche ALE \_ \_ recv \_ accepte \_ \| les règles de filtrage par connexion entrantes V {4 6}**  

1.  Ajoutez un filtre avec les propriétés suivantes. Ce filtre n’autorise que les tentatives de connexion entrante s’ils sont sécurisés par IPsec. 

    | Filter (propriété)                                                   | Valeur                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                  |
    | **action. type**                                                   | **fin de l’appel à l' \_ action fwp \_ \_**                        |
    | **action. calloutKey**                                             | **\_Appel FWPM \_ IPSec \_ entrant \_ initiate \_ Secure \_ V {4 \| 6}** |

        
2.  Exempter le trafic ICMP d’IPsec en ajoutant un filtre avec les propriétés suivantes.

    | Filter (propriété)                                                   | Valeur                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                                |
    | **FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**             | **IPPROTO \_ ICMP {V6}** ces constantes sont définies dans Winsock2. h.<br/> |
    | **action. type**                                                   | **\_autorisation d’action fwp \_**                                                    |
    | **weight**                                                        | **\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**                                   |

        
3.  Ajoutez un filtre avec les propriétés suivantes. Ce filtre autorise uniquement les connexions entrantes vers le port TCP 5555 s’ils sont chiffrés.

    | Filter (propriété)                                                   | Valeur                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                                                           |
    | **FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**             | **IPPROTO \_ TCP** cette constante est définie dans Winsock2. h.<br/>                                    |
    | **FWPM \_ Condition de filtrage de \_ \_ \_ port local IP de condition**          | 5555                                                                                                  |
    | **action. type**                                                   | **fin de l’appel à l' \_ action fwp \_ \_**                                                                 |
    | **action. calloutKey**                                             | **\_Appel FWPM \_ IPSec \_ entrant \_ initiate \_ Secure \_ V {4 \| 6}**                                          |
    | **rawContext**                                                    | [**la \_ connexion du jeu ale du contexte FWPM \_ \_ nécessite le \_ \_ \_ \_ chiffrement IPSec**](filter-context-identifiers.md) |

        

**Au niveau de FWPM \_ couche \_ ALE \_ auth \_ Connect connexion \_ V {4 \| 6} configurer les règles de filtrage par connexion sortantes**

-   Ajoutez un filtre avec les propriétés suivantes. Ce filtre autorise uniquement les connexions sortantes à partir du port TCP 5555 s’ils sont chiffrés.

    | Filter (propriété)                                                   | Valeur                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condition de filtrage du \_ \_ \_ \_ type d’adresse locale IP de condition** | NlatUnicast                                                                                           |
    | **FWPM \_ Condition de filtrage de \_ \_ protocole IP de condition**             | **IPPROTO \_ TCP** cette constante est définie dans Winsock2. h.<br/>                                    |
    | **FWPM \_ Condition de filtrage de \_ \_ \_ port local IP de condition**          | 5555                                                                                                  |
    | **action. type**                                                   | **fin de l’appel à l' \_ action fwp \_ \_**                                                                 |
    | **action. calloutKey**                                             | **FWPM \_ de \_ \_ connexion ALE ALE IPSec \_ \_ V {4 \| 6}**                                                       |
    | **rawContext**                                                    | [**la \_ connexion du jeu ale du contexte FWPM \_ \_ nécessite le \_ \_ \_ \_ chiffrement IPSec**](filter-context-identifiers.md) |

      

  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de code : utilisation du mode de transport](using-transport-mode.md)
</dt> <dt>

[Couches ALE](ale-layers.md)
</dt> <dt>

[**Identificateurs de légende intégrés**](built-in-callout-identifiers.md)
</dt> <dt>

[Conditions de filtrage](filtering-conditions.md)
</dt> <dt>

[**Filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**\_type de \_ contexte du fournisseur FWPM \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

