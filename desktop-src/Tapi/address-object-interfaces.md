---
description: Les objets Address sont des entités qui peuvent émettre ou recevoir des appels. Les méthodes et interfaces associées permettent à une application d’extraire et de définir des informations relatives à une adresse, par exemple si l’adresse est prise en charge par l’ID d’appelant.
ms.assetid: 6e347e4c-aec3-4bbd-95f3-a68e6e136e11
title: Interfaces d’objet Address
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef19db02123e10e839906a00931ef246d19d2c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538690"
---
# <a name="address-object-interfaces"></a>Interfaces d’objet Address

Les [objets Address](address-object.md) sont des entités qui peuvent émettre ou recevoir des appels. Les méthodes et interfaces associées permettent à une application d’extraire et de définir des informations relatives à une adresse, par exemple si l’adresse est prise en charge par l’ID d’appelant.

Les interfaces [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent), [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo), [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard), [**ITForwardInformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation), [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)et [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress) ne sont pas directement exposées sur l’objet Address, mais sont étroitement liées et sont répertoriées ici pour des raisons de commodité de référence.



| Interface                                                            | Description                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)                                       | Agit comme une interface de base pour l’objet Address.                                                                                                  |
| [**ITAddress2**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2)                                     | Dérive de [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress); fournit des méthodes supplémentaires qui prennent en charge les appareils téléphoniques.                                            |
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)               | Obtient des informations sur les fonctionnalités d’une adresse.                                                                                          |
| [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent)                             | Fournit des informations concernant les événements d’adresse.                                                                                                 |
| [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation)                 | Effectue la traduction d’adresses.                                                                                                                   |
| [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo)         | Obtient les informations de traduction d’adresse.                                                                                                           |
| [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)                               | Fournit des méthodes pour récupérer des informations de carte d’appel.                                                                                          |
| [**ITForwardInformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation)                 | Fournit des méthodes pour configurer et implémenter le transfert d’appel.                                                                               |
| [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol)   | Prend en charge les applications héritées qui requièrent un accès direct à un appareil et à sa configuration.                                                      |
| [**ITLegacyAddressMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2) | Étend [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol) en autorisant la configuration de paramètres liés aux appareils de ligne. |
| [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)                             | Obtient des informations relatives à l’emplacement du tiers appelant.                                                                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                             | Obtient des informations sur les fonctionnalités de support multimédia d’une adresse.                                                                            |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                       | Obtient des informations sur les terminaux disponibles et fournit une méthode pour créer des terminaux supplémentaires.                                                   |
| [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress)                                 | Énumère [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress).                                                                                                      |
| [**IEnumCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard)                         | Énumère [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard).                                                                                              |



 

Si l’adresse est une adresse [MSP Wave](wave-msp.md) , l’interface [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport) est également exposée sur l’objet Address.

 

 
