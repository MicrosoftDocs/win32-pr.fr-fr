---
description: Après l’attribution d’adresses, l’interface TAPI assigne des identificateurs d’adresse aux adresses.
ms.assetid: 19394db1-4408-4ba6-be48-b408c1fa0f30
title: Identificateurs d’adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80ee463271a4d7fe9e4dcec086b08c37326551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512946"
---
# <a name="address-identifiers"></a>Identificateurs d’adresse

Après l’attribution d’adresses, l’interface TAPI assigne des identificateurs d’adresse aux adresses. Un *identificateur d’adresse* est un nombre compris entre 0 et le nombre d’adresses sur la ligne moins un. Un identificateur d’adresse est un nombre permanent attribué à un appareil donné et reste constant même entre les mises à niveau du système d’exploitation. La combinaison de l' [identificateur d’appareil](device-identifier-ovr.md) et de l’identificateur d’adresse identifie de façon unique une adresse donnée.

**TAPI 2. x :** Les applications obtiennent un identificateur d’adresse (et un identificateur de périphérique) lors d’un appel à [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) ou [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), dans la structure [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) ou dans un appel à [**lineGetAddressID**](/windows/win32/api/tapi/nf-tapi-linegetaddressid).

**TAPI 3. x :** Le [**ITAddressCapabilities :: obtenir \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) appelé *AddressCap* défini sur la [**\_ fonctionnalité d’adresse**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability) de **\_ ADDRESSID AC** est retourné avec le paramètre *plCapability* défini sur l’ID d’adresse actuel.

 

 
