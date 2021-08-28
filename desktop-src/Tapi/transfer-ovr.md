---
description: L’opération de transfert permet à une application d’envoyer une session de communication actuellement connectée à une autre adresse.
ms.assetid: b1027f09-74e1-4da8-b718-bb55a56dda1d
title: Transférer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bb527ad8e0a26ba5e4da341eb15509e8af05e7950d82de92be839e70370c79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514539"
---
# <a name="transfer"></a>Transférer

L’opération de transfert permet à une application d’envoyer une session de communication actuellement connectée à une autre adresse.

L’interface TAPI fournit deux mécanismes pour transférer une session active vers une autre adresse. Le *transfert aveugle* permet de transférer une session existante vers une adresse de destination spécifiée en une seule phase. La *consultation du transfert* requiert l’existence d’une session de consultation en plus de la session active à configurer pour le transfert, puis l’achèvement du transfert. Le choix entre ces deux types est souvent basé sur les fonctionnalités du fournisseur de services, car certains fournisseurs de services ne prennent pas en charge le transfert aveugle. Dans certains cas, les besoins de l’application peuvent faire passer la méthode préférée au transfert consultatif, même si le transfert des aveugles est possible.

L’opération de transfert aveugle est fondamentalement identique sous TAPI 2 et TAPI 3, mais le transfert consultatif suit des modèles légèrement différents.

**TAPI 2. x :** Le transfert consultatif commence par l’appel de [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), qui place l’appel existant sur la suspension de la consultation et identifie cet appel comme la cible de la demande de transfert-achèvement suivante. La fonction **lineSetupTransfer** alloue également un appel de consultation qui peut être utilisé pour établir l’appel de consultation avec le tiers vers lequel l’appel sera transféré. L’application peut composer l’extension du tiers de destination lors de l’appel de consultation (à l’aide de [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial)), ou elle peut supprimer et désallouer l’appel de consultation et activer à la place un appel détenu existant (à l’aide de [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold)), s’il est pris en charge par le commutateur. Alors que l’appel initial est en attente de consultation et que l’appel de consultation est actif, l’application peut basculer entre ces appels à l’aide de [**lineSwapHold**](/windows/win32/api/tapi/nf-tapi-lineswaphold).

**TAPI 2. x :** Les applications effectuent le transfert consultatif à l’aide de [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer). Les deux appels sont rétablis à l’état *inactif* .

Les applications peuvent utiliser la fonctionnalité « transfert en une étape » de nombreux PBX (une seule pression pour établir un transfert de consultation) en définissant le paramètre *lpCallParams* sur le membre **LINECALLPARAMFLAGS \_ ONESTEPTRANSFER** des [ \_ constantes LINECALLPARAMFLAGS](./linecallparamflags--constants.md) lors de l’appel de [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer).

**TAPI 3. x :** Le transfert consultatif commence avec l’utilisation de [**ITAddress :: createCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) pour créer un appel de consultation vers la nouvelle adresse de destination. [**ITBasicCallControl :: Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer) est ensuite appelé sur l’objet d’appel d’origine à l’aide d’un pointeur vers le nouvel objet d’appel de consultation en tant que paramètre. L’appel de [**ITBasicCallControl :: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) sur l’objet d’appel de consultation termine ensuite le transfert.

L’application doit libérer des ressources de session après la réussite d’une opération de transfert.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.

**TAPI 2. x :** Consultez [**lineBlindTransfer**](/windows/win32/api/tapi/nf-tapi-lineblindtransfer), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer).

**TAPI 3. x :** Consultez [**ITBasicCallControl :: BlindTransfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-blindtransfer), [**ITAddress :: createCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall), [**ITBasicCallControl :: Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer), [**ITBasicCallControl :: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish).

 

 
