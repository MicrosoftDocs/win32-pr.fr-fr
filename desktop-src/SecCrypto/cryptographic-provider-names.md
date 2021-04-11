---
description: Utilisé avec les fonctions CryptAcquireContext et CryptSetProvider.
ms.assetid: 97e9a708-83b5-48b3-9d16-f7b54367dc4e
title: Noms des fournisseurs de services de chiffrement (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58a5cbe497e56144a9948dab96be0c03dd5a99f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951090"
---
# <a name="cryptographic-provider-names"></a>Noms des fournisseurs de services de chiffrement

Les noms des [*fournisseurs de services de chiffrement*](../secgloss/c-gly.md) (CSP) suivants sont définis dans wincrypt. h. Ces constantes sont utilisées avec les fonctions [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) et [**CryptSetProvider**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera) .



| Constante/valeur                                                                                                                                                                                                                                                                                          | Description                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MS_DEF_DH_SCHANNEL_PROV"></span><span id="ms_def_dh_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ DH \_ Schannel \_ Prov**</dt> ( <dt>fournisseur de services de chiffrement Microsoft DH SChannel)</dt> </dl>      | Le [fournisseur de services de chiffrement Microsoft DSS et Diffie-Hellman/Schannel](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md).<br/>                                         |
| <span id="MS_DEF_DSS_DH_PROV"></span><span id="ms_def_dss_dh_prov"></span><dl> <dt>**MS \_ DEF \_ DSS \_ DH \_ Prov**</dt> <dt>« Microsoft Base DSS et Diffie-Hellman fournisseur de services de chiffrement »</dt> </dl>     | [Microsoft Base DSS et Diffie-Hellman fournisseur de services de chiffrement](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                                 |
| <span id="MS_DEF_DSS_PROV"></span><span id="ms_def_dss_prov"></span><dl> <dt>**MS \_ DEF \_ DSS \_ Prov**</dt> ( <dt>fournisseur de services de chiffrement DSS de base Microsoft)</dt> </dl>                                  | [Fournisseur de services de chiffrement DSS Microsoft](microsoft-dss-cryptographic-provider.md).<br/>                                                                                                 |
| <span id="MS_DEF_PROV"></span><span id="ms_def_prov"></span><dl> <dt>**MS \_ DEF \_ Prov**</dt> <dt>« Microsoft base Cryptographic Provider v 1.0 »</dt> </dl>                                              | [Fournisseur de services de chiffrement de base Microsoft](microsoft-base-cryptographic-provider.md).<br/>                                                                                               |
| <span id="MS_DEF_RSA_SCHANNEL_PROV"></span><span id="ms_def_rsa_schannel_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ Schannel \_ Prov**</dt> ( <dt>fournisseur de services de chiffrement Microsoft RSA SChannel)</dt> </dl>  | [Fournisseur de services de chiffrement Microsoft RSA/SChannel](microsoft-rsa-schannel-cryptographic-provider.md).<br/>                                                                               |
| <span id="MS_DEF_RSA_SIG_PROV"></span><span id="ms_def_rsa_sig_prov"></span><dl> <dt>**MS \_ DEF \_ RSA \_ SIG \_ Prov**</dt> <dt>"fournisseur de chiffrement Microsoft RSA signature"</dt> </dl>                | Le [fournisseur de chiffrement de signature Microsoft RSA](microsoft-rsa-signature-cryptographic-provider.md) n’est pas pris en charge.<br/>                                                            |
| <span id="MS_ENH_DSS_DH_PROV"></span><span id="ms_enh_dss_dh_prov"></span><dl> <dt>**MS \_ ENH \_ DSS \_ DH \_ Prov**</dt> <dt>« Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider »</dt> </dl> | Le [fournisseur de services de chiffrement DSS et Diffie-Hellman Microsoft Enhanced](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md).<br/>                                         |
| <span id="MS_ENH_RSA_AES_PROV"></span><span id="ms_enh_rsa_aes_prov"></span><dl> <dt>**MS \_ ENH \_ RSA \_ AES \_ Prov**</dt> <dt>« Microsoft Enhanced RSA and AES Cryptographic Provider »</dt> </dl>         | [Fournisseur de services de chiffrement AES Microsoft](microsoft-aes-cryptographic-provider.md).<br/> * * Windows XP : * * « Microsoft Enhanced RSA and AES Cryptographic Provider (prototype) »<br/> |
| <span id="MS_ENHANCED_PROV"></span><span id="ms_enhanced_prov"></span><dl> <dt>**MS \_ \_Proven Premium**</dt> <dt>« Microsoft Enhanced Cryptographic Provider v 1.0 »</dt> </dl>                           | [Fournisseur de services de chiffrement amélioré Microsoft](microsoft-enhanced-cryptographic-provider.md).<br/>                                                                                       |
| <span id="MS_SCARD_PROV"></span><span id="ms_scard_prov"></span><dl> <dt>**MS \_ \_**</dt> <dt>« Fournisseur de chiffrement de carte à puce Microsoft de base »</dt> </dl>                                         | [Fournisseur de services de chiffrement de carte à puce de base Microsoft](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider).<br/>                                                    |
| <span id="MS_STRONG_PROV"></span><span id="ms_strong_prov"></span><dl> <dt>**MS \_ FORT \_ prove**</dt> ( <dt>fournisseur de chiffrement fort Microsoft)</dt> </dl>                                        | [Fournisseur de services de chiffrement renforcé Microsoft](microsoft-strong-cryptographic-provider.md).<br/>                                                                                           |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



 

 
