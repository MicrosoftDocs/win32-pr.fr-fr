---
description: Le type d’adresse de l’appareil décrit les formes d’adressage autorisées sur une adresse, par exemple un numéro de téléphone ou une adresse IP.
ms.assetid: b474dfca-c4a6-4aab-a4dd-5aec7be3e02a
title: Type d'adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9438c200c9b09dd4f78342ea18d412eaaf23b646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521051"
---
# <a name="address-type"></a>Type d'adresse

Le type d’adresse de l’appareil décrit les formes d’adressage autorisées sur une adresse, par exemple un numéro de téléphone ou une adresse IP. Un appareil donné va comprendre un ou plusieurs types d’adresses. Pour obtenir la liste des types d’adresses pris en charge par TAPI, consultez [ \_ constantes LINEADDRESSTYPE](lineaddresstype--constants.md). La [traduction d’adresses](initiate-a-session-ovr.md) peut être utilisée pour convertir une adresse d’un type en un autre.

Pour obtenir des informations générales sur les adresses, consultez [adresse](address-ovr.md) sous [catégories d’appareils](device-categories.md).

Le [type d’adresse d’une session](address-type-for-a-session-ovr.md) est un sous-ensemble des types d’adresse d’appareil.

**TAPI 2. x :** Consultez [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) et le membre **dwAddressType** de [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).

**TAPI 3. x :** Consultez [**ITAddressCapabilities :: obtenir \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), avec *AddressCap* défini sur la [**\_ fonctionnalité d’adresse**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)de **\_ ADDRESSTYPES AC** .

 

 
