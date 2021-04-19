---
description: L’interface IH323LineEx est implémentée par le MSP H323 et n’est disponible que sur les objets d’adresse H. 323. Cette interface expose des méthodes qui permettent la création et la manipulation de terminaux qui peuvent communiquer entre des clients H323 et SDP.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: Interface IH323LineEx (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41888b16f645a3af1eefd9df61623cb28684bfdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535290"
---
# <a name="ih323lineex-interface"></a>Interface IH323LineEx

\[**IH323LineEx** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **IH323LineEx** est implémentée par le [MSP H323](h323-msp.md) et n’est disponible que sur les objets d’adresse H. 323. Cette interface expose des méthodes qui permettent la création et la manipulation de terminaux qui peuvent communiquer entre des clients H323 et SDP.

> [!Note]  
> Toutes les méthodes dans cette interface doivent être appelées uniquement après l’inscription des appels entrants sur cette adresse.

 

## <a name="members"></a>Membres

L’interface **IH323LineEx** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IH323LineEx** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IH323LineEx** possède ces méthodes.



| Méthode                                                                                 | Description                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**SetAlias**](ih323lineex-setalias.md)                                               | Configure un alias H. 323 par défaut pour l’adresse.<br/>             |
| [**SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md) | Configure la pondération des préférences pour les fonctionnalités par défaut.<br/> |
| [**SetExternalT120Address**](ih323lineex-setexternalt120address.md)                   | Configure une adresse T. 120 externe pour l’échange de données.<br/>       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MSP H323](h323-msp.md)
</dt> </dl>

 

