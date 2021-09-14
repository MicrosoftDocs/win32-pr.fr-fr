---
description: Explique comment vérifier une contre-signature à l’aide de CryptMsgVerifyCountersignatureEncoded.
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: Vérification d’une contre-signature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711e15388144fbf674cbb0c42ff41883edbb5af0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416353"
---
# <a name="verifying-a-countersignature"></a>Vérification d’une contre-signature

**Pour vérifier une contre-signature**

1.  Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) pour obtenir un descripteur du message signé.
2.  Obtient un pointeur vers le certificat du contresignéeur ( [**\_ informations de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).
3.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) pour récupérer les informations de signataire à partir du message.
4.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) pour récupérer la contre- [*signature*](../secgloss/c-gly.md) du message.
5.  Appelez [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) pour vérifier la contre-signature.

Si l’appel de fonction [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) a échoué, la contre- [*signature*](../secgloss/c-gly.md) est vérifiée.

 

 
