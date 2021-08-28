---
description: PNRP utilise la fonction WSALookupServiceEnd pour effectuer les opérations suivantes.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP et WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9d91dea87b5a8c41cb5f689d89464bf7fd7e0179b1cad71943c14d107842b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553379"
---
# <a name="pnrp-and-wsalookupserviceend"></a>PNRP et WSALookupServiceEnd

PNRP utilise la fonction [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) pour effectuer les opérations suivantes :

-   Terminer une requête lancée lors d’un appel précédent à [ **WSALookupServiceBegin**](winsock-nsp-reference-links.md)
-   Débloquer un appel à [**WSALookupServiceNext**](winsock-nsp-reference-links.md) pour arrêter la recherche

Un appel à [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) met fin à une requête et nettoie le contexte. Le handle obtenu à partir d’un appel à **WSALookupServiceBegin** doit être passé en tant que paramètre à **WSALookupServiceEnd**.

Pour plus d’informations sur PNRP et la fonction [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) , consultez [PNRP et WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[PNRP et WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[Codes d’erreur du NSP PNRP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSALookupServiceNext**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



