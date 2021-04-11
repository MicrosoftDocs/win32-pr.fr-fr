---
description: Les données d’appel sont une mémoire tampon de taille variable qui peut être utilisée pour accumuler des informations sur une session de communication. Ces informations deviennent disponibles pour toutes les applications qui possèdent ou surveillent la session.
ms.assetid: 8b7a674f-ba78-4830-bb20-7fa74e202a1a
title: Données d’appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedfd44a46518a58f3a3aeaec59326648669cb49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318881"
---
# <a name="call-data"></a>Données d’appel

Les données d’appel sont une mémoire tampon de taille variable qui peut être utilisée pour accumuler des informations sur une session de communication. Ces informations deviennent disponibles pour toutes les applications qui possèdent ou surveillent la session.

Par exemple, le gestionnaire initial d’une session entrante peut demander et entrer des informations de compte client dans un tampon de données d’appel, et les gestionnaires suivants n’ont pas besoin de répéter la demande.

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.

**TAPI 2. x :** Consultez [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetCallData**](/windows/win32/api/tapi/nf-tapi-linesetcalldata) (**DwCallDataSize** et **dwCallDataOffset** membres de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)), [**ligne \_ CALLINFO**](./line-callinfo.md) message (*dwParam1* défini sur LINECALLINFOSTATE \_ CALLDATA).

**TAPI 3. x :** Consultez [**ITCallInfo ::p ut \_ CallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfobuffer) (**CIM \_ CALLDATABUFFER** membre de [**CALLINFO \_ buffer**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer)); [**ITCallInfoChangeEvent :: obtient \_ Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) retourne le **membre \_ CALLDATA CIC** de [**la \_ cause CALLINFOCHANGE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause).

 

 
