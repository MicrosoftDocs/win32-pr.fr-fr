---
description: Le moteur de protocole Schannel effectue le protocole de transfert et l’authentification dans un processus sécurisé et le chiffrement/message en bloc passant dans le processus d’application.
ms.assetid: bcd49aaf-b0e3-4c31-be95-986b8ad843a8
title: Franchissement des limites de processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046bc6f53d609ec22ed37edd08d6967cc4ae73e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513201"
---
# <a name="crossing-process-boundaries"></a><span data-ttu-id="c3f06-103">Franchissement des limites de processus</span><span class="sxs-lookup"><span data-stu-id="c3f06-103">Crossing Process Boundaries</span></span>

<span data-ttu-id="c3f06-104">Le moteur de protocole [*Schannel*](../secgloss/s-gly.md) effectue le protocole de transfert et l’authentification dans un [*processus*](../secgloss/p-gly.md) sécurisé et le chiffrement/message en bloc passant dans le processus d’application.</span><span class="sxs-lookup"><span data-stu-id="c3f06-104">The [*Schannel*](../secgloss/s-gly.md) protocol engine performs the handshaking and authentication in a secure [*process*](../secgloss/p-gly.md) and the bulk encryption/message passing in the application process.</span></span> <span data-ttu-id="c3f06-105">Cela signifie que les [*clés de chiffrement en bloc*](../secgloss/b-gly.md) et les clés [*Mac*](../secgloss/m-gly.md) doivent être copiées d’un processus à un autre.</span><span class="sxs-lookup"><span data-stu-id="c3f06-105">This means that the [*bulk encryption keys*](../secgloss/b-gly.md) and [*MAC*](../secgloss/m-gly.md) keys must be copied from one process to another.</span></span> <span data-ttu-id="c3f06-106">Pour copier les clés d’un processus à un autre, utilisez les fonctions [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) et [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) comme suit :</span><span class="sxs-lookup"><span data-stu-id="c3f06-106">To copy the keys from one process to another, use the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) and [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) functions as follows:</span></span>

1.  <span data-ttu-id="c3f06-107">Le processus sécurisé exporte chaque clé dans un [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) à l’aide de [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), puis détruit la clé à l’aide de [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span><span class="sxs-lookup"><span data-stu-id="c3f06-107">The secure process exports each key into an [*OPAQUEKEYBLOB*](../secgloss/o-gly.md) using [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), then destroys the key using [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).</span></span> <span data-ttu-id="c3f06-108">Notez que si la clé est stockée dans le matériel, le CSP doit reconnaître cela et ne doit pas tenter de détruire la clé.</span><span class="sxs-lookup"><span data-stu-id="c3f06-108">Note that if the key is stored in hardware, the CSP must recognize this and must not attempt to destroy the key.</span></span>
2.  <span data-ttu-id="c3f06-109">Le processus sécurisé transmet le OPAQUEKEYBLOBs au processus d’application d’une manière allant au-delà de la portée de ce document.</span><span class="sxs-lookup"><span data-stu-id="c3f06-109">The secure process passes the OPAQUEKEYBLOBs to the application process in a manner beyond the scope of this document.</span></span>
3.  <span data-ttu-id="c3f06-110">Le processus d’application importe chaque OPAQUEKEYBLOB dans le CSP à l’aide de [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="c3f06-110">The application process imports each OPAQUEKEYBLOB back into the CSP using [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span> <span data-ttu-id="c3f06-111">À ce stade, la clé doit être exactement dans le même [*État*](../secgloss/s-gly.md) que lorsqu’elle a été exportée.</span><span class="sxs-lookup"><span data-stu-id="c3f06-111">At this point, the key must be in exactly the same [*state*](../secgloss/s-gly.md) as when it was exported.</span></span>

 

 
