---
title: Exemptions IKE/AuthIP
description: protocole IKE (Internet Key Exchange) (IKE) et protocole Authenticated IP (Authenticated Internet Protocol) (AuthIP), afin de fonctionner, doivent exempter le trafic réseau du filtrage IPsec.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2963c804c6bd63f191563566bcc99dcf9f0f4a74bb2c844a402adc856dbad3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069059"
---
# <a name="ikeauthip-exemptions"></a>Exemptions IKE/AuthIP

les modules de génération de clés ipsec (Internet Protocol security), protocole IKE (Internet Key Exchange) (IKE) et protocole Authenticated IP (Authenticated Internet Protocol) (AuthIP), afin de fonctionner, doivent exempter le trafic réseau du filtrage IPsec.

dans Windows plate-forme de filtrage (WFP), le moteur de filtrage de Base ajoute automatiquement des filtres d’exemption ike et authip lorsque le filtre de stratégie en mode principal ike ou authip (MM) est ajouté et les supprime lorsque le dernier filtre de stratégie ike ou authip MM est supprimé. De cette façon, les fournisseurs de stratégie n’ont pas à gérer individuellement les exemptions de filtrage IKE et AuthIP.

Un filtre de stratégie IKE MM est un filtre dans la couche de moteur [**FWPM \_ \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) qui fait référence à un contexte de fournisseur de type [**FWPM \_ IPSec \_ IKE \_ mm \_ Context**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Un filtre de stratégie AuthIP MM est un filtre dans la couche de moteur [**FWPM \_ \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) qui fait référence à un contexte de fournisseur de type [**FWPM \_ IPSec \_ AuthIP \_ mm \_ Context**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Un filtre d’exemption IKE ou AuthIP est un filtre dans la couche FWPM couche du moteur [**\_ \_ \_ transport entrant \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) ou transport sortant de la couche **FWPM \_ \_ \_ \_ v {4 \| 6}** pondéré automatiquement dans la plage de poids [**FWPM les \_ \_ \_ \_ exemptions IKE**](filter-weight-identifiers.md) .

Les exemptions IKE et AuthIP implémentées par BFE sont les suivantes.

| Version de l’adresse IP      | Port                        | Exemption                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPv4<br/> | UDP : 500 UDP : 4500<br/> | Autorisez le trafic IKE et AuthIP au niveau de la couche de transport entrante et au niveau de la couche de transport sortante. <br/> Autorisez le trafic IKE et AuthIP aux couches de réception/acceptation et de connexion ALE, mais limitez-les au système local.<br/> |
| IPv6<br/> | UDP : 500<br/>          | Autorisez le trafic IKE et AuthIP au niveau de la couche de transport entrante et au niveau de la couche de transport sortante. <br/> Autorisez le trafic IKE et AuthIP aux couches de réception/acceptation et de connexion ALE, mais limitez-les au système local.<br/> |



 

Les filtres d’exemption IKE et AuthIP sont ouverts à toutes les adresses. Pour implémenter un pare-feu avec un contrôle plus granulaire, les fournisseurs de stratégie doivent ajouter des filtres dans une plage de poids supérieure à celle des [**\_ \_ \_ \_ exemptions IKE**](filter-weight-identifiers.md)de la plage de poids de FWPM.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration IPsec](ipsec-configuration.md)
</dt> <dt>

[Affectation de poids de filtre](filter-weight-assignment.md)
</dt> </dl>

 

 





