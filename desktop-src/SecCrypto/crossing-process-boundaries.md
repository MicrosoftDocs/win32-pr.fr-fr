---
description: Le moteur de protocole Schannel effectue le protocole de transfert et l’authentification dans un processus sécurisé et le chiffrement/message en bloc passant dans le processus d’application.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Franchissement des limites de processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0f8ba4c2d7a0a80ad97e62487421b5b4a0a6f8deda9d8edb550c2d8fcddab15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768871"
---
# <a name="crossing-process-boundaries"></a>Franchissement des limites de processus

Le moteur de protocole [*Schannel*](../secgloss/s-gly.md) effectue le protocole de transfert et l’authentification dans un [*processus*](../secgloss/p-gly.md) sécurisé et le chiffrement/message en bloc passant dans le processus d’application. Cela signifie que les [*clés de chiffrement en bloc*](../secgloss/b-gly.md) et les clés [*Mac*](../secgloss/m-gly.md) doivent être copiées d’un processus à un autre. Pour copier les clés d’un processus à un autre, utilisez les fonctions [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) et [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) comme suit :

1.  Le processus sécurisé exporte chaque clé dans un [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) à l’aide de [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), puis détruit la clé à l’aide de [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey). Notez que si la clé est stockée dans le matériel, le CSP doit reconnaître cela et ne doit pas tenter de détruire la clé.
2.  Le processus sécurisé transmet le OPAQUEKEYBLOBs au processus d’application d’une manière allant au-delà de la portée de ce document.
3.  Le processus d’application importe chaque OPAQUEKEYBLOB dans le CSP à l’aide de [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey). À ce stade, la clé doit être exactement dans le même [*État*](../secgloss/s-gly.md) que lorsqu’elle a été exportée.

 

 
