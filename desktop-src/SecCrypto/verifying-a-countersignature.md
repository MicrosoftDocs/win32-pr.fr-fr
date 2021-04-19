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
# <a name="verifying-a-countersignature"></a>Vérification d’une contre-signature

**Pour vérifier une contre-signature**

1.  Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) pour obtenir un descripteur du message signé.
2.  Obtient un pointeur vers le certificat du contresignéeur ( [**\_ informations de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).
3.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) pour récupérer les informations de signataire à partir du message.
4.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) pour récupérer la contre- [*signature*](../secgloss/c-gly.md) du message.
5.  Appelez [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) pour vérifier la contre-signature.

Si l’appel de fonction [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) a échoué, la contre- [*signature*](../secgloss/c-gly.md) est vérifiée.

 

 
