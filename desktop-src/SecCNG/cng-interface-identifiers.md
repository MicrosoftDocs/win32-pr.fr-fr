---
description: Les identificateurs suivants sont utilisés pour identifier une interface de chiffrement CNG.
ms.assetid: 509c89ff-0c73-4e57-9c39-400522f2086e
title: Identificateurs d’interface CNG (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4f75de82e198e0471b48175a080012b9b40eed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106530827"
---
# <a name="cng-interface-identifiers"></a>Identificateurs d’interface CNG

Les identificateurs suivants sont utilisés pour identifier une interface de chiffrement CNG. Dans CNG, une interface identifie le type de comportement de chiffrement pris en charge par un fournisseur. Par exemple, un fournisseur peut être un générateur de nombres aléatoires ou un fournisseur de hachage.



| Constante/valeur                                                                                                                                                                                                                                                                                             | Description                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_CIPHER_INTERFACE"></span><span id="bcrypt_cipher_interface"></span><dl> <dt>**BCRYPT \_ \_Interface de chiffrement**</dt> <dt>0x00000001</dt> </dl>                                               | Interface de chiffrement symétrique.<br/>                                                                                                                                        |
| <span id="BCRYPT_HASH_INTERFACE"></span><span id="bcrypt_hash_interface"></span><dl> <dt>**BCRYPT \_ \_Interface de hachage**</dt> <dt>0x00000002</dt> </dl>                                                     | Interface de hachage.<br/>                                                                                                                                                    |
| <span id="BCRYPT_ASYMMETRIC_ENCRYPTION_INTERFACE"></span><span id="bcrypt_asymmetric_encryption_interface"></span><dl> <dt>**BCRYPT \_ 0x00000003 de l' \_ \_ interface de CHIFFREment asymétrique**</dt> <dt></dt> </dl> | Interface de chiffrement asymétrique.<br/>                                                                                                                                   |
| <span id="BCRYPT_SECRET_AGREEMENT_INTERFACE"></span><span id="bcrypt_secret_agreement_interface"></span><dl> <dt>**BCRYPT \_ \_ \_ Interface de l’accord secret**</dt> <dt>0x00000004</dt> </dl>                | Interface d’accord secret.<br/>                                                                                                                                        |
| <span id="BCRYPT_SIGNATURE_INTERFACE"></span><span id="bcrypt_signature_interface"></span><dl> <dt>**BCRYPT \_ De l' \_ interface de signature**</dt> <dt>0x00000005</dt> </dl>                                      | Interface de signature.<br/>                                                                                                                                               |
| <span id="BCRYPT_RNG_INTERFACE"></span><span id="bcrypt_rng_interface"></span><dl> <dt>**BCRYPT \_ \_Interface RNG**</dt> <dt>0x00000006</dt> </dl>                                                        | Interface du générateur de nombres aléatoires.<br/>                                                                                                                                 |
| <span id="NCRYPT_KEY_STORAGE_INTERFACE"></span><span id="ncrypt_key_storage_interface"></span><dl> <dt>**NCRYPT \_ \_ \_ Interface de stockage de clés**</dt> <dt>0x00010001</dt> </dl>                               | Interface de stockage de clés.<br/>                                                                                                                                             |
| <span id="NCRYPT_SCHANNEL_INTERFACE"></span><span id="ncrypt_schannel_interface"></span><dl> <dt>**NCRYPT \_ \_Interface Schannel**</dt> <dt>0x00010002</dt> </dl>                                         | Interface de signature Schannel.<br/>                                                                                                                                      |
| <span id="NCRYPT_SCHANNEL_SIGNATURE_INTERFACE"></span><span id="ncrypt_schannel_signature_interface"></span><dl> <dt>**NCRYPT \_ \_ \_ Interface de signature Schannel**</dt> <dt>0x00010003</dt> </dl>          | Interface de la suite de chiffrement Schannel.<br/> **Windows server 2008, Windows Vista, Windows server 2003, Windows XP et windows 2000 :** Cette valeur n’est pas prise en charge.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                                                                |
| En-tête<br/>                   | <dl> <dt>Bcrypt. h ; </dt> <dt>Ncrypt. h</dt> </dl> |



 

 




