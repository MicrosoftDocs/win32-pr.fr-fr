---
description: L’application doit inventorier les ressources de communication disponibles, puis notifier à l’interface TAPI les ressources qu’elle utilisera et son mode d’utilisation.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Inventaire des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13436479877f63255ce6132a5907f97a511efea16dd5e21db41b0e41000beb8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773419"
---
# <a name="resource-inventory"></a>Inventaire des ressources

L’application doit inventorier les ressources de communication disponibles, puis notifier à l’interface TAPI les ressources qu’elle utilisera et son mode d’utilisation. Pour plus d’informations sur les types de ressources et capacités auxquelles une application peut accéder, consultez contrôle de l' [appareil](device-control.md) .

**TAPI 2. x :** Les applications obtiennent le nombre de lignes disponibles lorsque [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) retourne. Ils peuvent ensuite effectuer des [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) sur chaque ligne, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) pour chaque adresse et [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) pour chaque ligne qui sera utilisée.

**TAPI 3. x :** Les applications utilisent [**ITTAPI :: EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) ou [**ITTAPI :: obtenir des \_ adresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) pour découvrir les adresses disponibles. [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) et [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) fournissent des informations sur les types de communication possibles pour chaque adresse. Si elle est implémentée par le fournisseur de services, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) permet à une application d’accéder à des informations et des contrôles supplémentaires.

 

 
