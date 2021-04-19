---
description: Explique comment contre-signer un message à l’aide de CryptMsgCountersign.
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Contre-signature d’un message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02091d25e7ee22f986a26b8f07abff68ebb8c11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523275"
---
# <a name="countersigning-a-message"></a>Contre-signature d’un message

**Pour contre-signer un message signé à l’aide de CryptMsgCountersign**

1.  Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) pour obtenir un descripteur du message signé.
2.  Initialisez une structure d' [**\_ informations de \_ codage \_ CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) pour le signataire.
3.  Ajoutez la structure d’informations de codage du signataire CMSG à un tableau de contre- [**\_ signataires \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) (un seul contresigné est actuellement pris en charge).
4.  Appelez [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) pour ajouter la contre-signature ou les contre-signatures.

Si tous les appels de fonction ont été exécutés correctement, le message d’origine a désormais une contre- [*signature*](../secgloss/c-gly.md) incluse comme attribut non authentifié.

**Pour contre-signer un message signé à l’aide de CryptMsgCountersignEncoded**

1.  Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) pour obtenir un descripteur du message signé.
2.  Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) pour récupérer les informations de signataire encodées du message signé.
3.  Initialisez une structure d' [**\_ informations de \_ codage \_ CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) pour le signataire.
4.  Ajoutez la structure d’informations de codage du signataire CMSG à un tableau de contre- [**\_ signataires \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) (un seul contresigné est actuellement pris en charge).
5.  Appelez [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) pour créer l’attribut de contre-signature encodé.
6.  Appelez [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) pour ajouter l’attribut contre-signature au message d’origine en tant qu’attribut non authentifié.

Si tous les appels de fonction ont échoué, un attribut contre- [*signature*](../secgloss/c-gly.md) est ajouté au message d’origine.

 

 
