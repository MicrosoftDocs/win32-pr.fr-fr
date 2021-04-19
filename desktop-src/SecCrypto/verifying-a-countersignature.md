---
description: Explique comment vérifier une contre-signature à l’aide de CryptMsgVerifyCountersignatureEncoded.
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: Vérification d’une contre-signature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711e15388144fbf674cbb0c42ff41883edbb5af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524926"
---
# <a name="verifying-a-countersignature"></a><span data-ttu-id="b6c9f-103">Vérification d’une contre-signature</span><span class="sxs-lookup"><span data-stu-id="b6c9f-103">Verifying a Countersignature</span></span>

<span data-ttu-id="b6c9f-104">**Pour vérifier une contre-signature**</span><span class="sxs-lookup"><span data-stu-id="b6c9f-104">**To verify a countersignature**</span></span>

1.  <span data-ttu-id="b6c9f-105">Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) pour obtenir un descripteur du message signé.</span><span class="sxs-lookup"><span data-stu-id="b6c9f-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="b6c9f-106">Obtient un pointeur vers le certificat du contresignéeur ( [**\_ informations de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).</span><span class="sxs-lookup"><span data-stu-id="b6c9f-106">Get a pointer to the countersigner's certificate ( [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).</span></span>
3.  <span data-ttu-id="b6c9f-107">Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) pour récupérer les informations de signataire à partir du message.</span><span class="sxs-lookup"><span data-stu-id="b6c9f-107">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the signer information from the message.</span></span>
4.  <span data-ttu-id="b6c9f-108">Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) pour récupérer la contre- [*signature*](../secgloss/c-gly.md) du message.</span><span class="sxs-lookup"><span data-stu-id="b6c9f-108">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the [*countersignature*](../secgloss/c-gly.md) from the message.</span></span>
5.  <span data-ttu-id="b6c9f-109">Appelez [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) pour vérifier la contre-signature.</span><span class="sxs-lookup"><span data-stu-id="b6c9f-109">Call [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) to verify the countersignature.</span></span>

<span data-ttu-id="b6c9f-110">Si l’appel de fonction [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) a échoué, la contre- [*signature*](../secgloss/c-gly.md) est vérifiée.</span><span class="sxs-lookup"><span data-stu-id="b6c9f-110">If the [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) function call succeeds, the [*countersignature*](../secgloss/c-gly.md) is verified.</span></span>

 

 
