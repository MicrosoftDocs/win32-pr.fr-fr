---
description: Constantes prédéfinies pour les protocoles de chiffrement. Ces valeurs sont définies dans wincrypt. h.
ms.assetid: 61dc0eff-2033-464a-a558-1798a92d48a2
title: Indicateurs de protocole (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25804763e407ff2a12e5657878e343f483d353e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952621"
---
# <a name="protocol-flags"></a>Indicateurs de protocole

Les éléments suivants sont des constantes prédéfinies pour les protocoles de chiffrement. Ces valeurs sont définies dans wincrypt. h.



| Constante/valeur                                                                                                                                                                                                                            | Description                                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="CRYPT_FLAG_IPSEC"></span><span id="crypt_flag_ipsec"></span><dl> <dt>**Crypt \_ BALIser \_ IPSec**</dt> <dt>0x0010</dt> </dl>       | Protocole IPsec (Internet Protocol Security).<br/>               |
| <span id="CRYPT_FLAG_PCT1"></span><span id="crypt_flag_pct1"></span><dl> <dt>**Crypt \_ INDICATEUR \_ PCT1**</dt> <dt>0x0001</dt> </dl>          | Protocole PCT (Private communications transport) version 1.<br/> |
| <span id="CRYPT_FLAG_SIGNING"></span><span id="crypt_flag_signing"></span><dl> <dt>**Crypt \_ SIGNALER la \_ signature**</dt> <dt>0x0020</dt> </dl> | Protocole de signature.<br/>                                          |
| <span id="CRYPT_FLAG_SSL2"></span><span id="crypt_flag_ssl2"></span><dl> <dt>**Crypt \_ INDICATEUR \_ SSL2**</dt> <dt>0x0002</dt> </dl>          | Protocole SSL (Secure Sockets Layer) version 2.<br/>             |
| <span id="CRYPT_FLAG_SSL3"></span><span id="crypt_flag_ssl3"></span><dl> <dt>**Crypt \_ SIGNALER \_ SSL3**</dt> <dt>0x0004</dt> </dl>          | Protocole SSL version 3.<br/>                                    |
| <span id="CRYPT_FLAG_TLS1"></span><span id="crypt_flag_tls1"></span><dl> <dt>**Crypt \_ INDICATEUR \_ TLS1**</dt> <dt>0x0008</dt> </dl>          | Protocole TLS (Transport Layer Security) version 1.<br/>         |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PROV \_ ENUMALGS \_ ex**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex)
</dt> </dl>

 

 




