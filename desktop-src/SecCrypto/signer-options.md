---
description: Définit ou récupère l’option de certificat du signataire.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Signer. options, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c22cf7b9d9ebe7e98e534d62b0a2771391c6cacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529912"
---
# <a name="signeroptions-property"></a>Signer. options, propriété

\[La propriété **options** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **options** définit ou récupère l’option de certificat du signataire.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a>Valeur de la propriété

La valeur du [**\_ certificat CAPICOM \_ inclut \_**](capicom-certificate-include-option.md) l’énumération d’option qui spécifie l’option de certificat du signataire. La valeur par défaut est le \_ certificat CAPICOM \_ \_ chaîne \_ , à l’exception de la \_ racine. Le tableau suivant répertorie les valeurs possibles.



| Value                                                                                                                                                                                                                                                             | Signification                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**le certificat CAPICOM \_ \_ inclut une \_ chaîne \_ à l’exception \_ de la racine**</dt> </dl> | Enregistre tous les certificats de la chaîne à l’exception de l’entité racine.<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**le certificat CAPICOM \_ \_ inclut une \_ \_ chaîne entière**</dt> </dl>                    | Enregistre la totalité de la chaîne de certificats.<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**le certificat CAPICOM \_ \_ inclut \_ uniquement l' \_ entité \_ end**</dt> </dl>       | Enregistre uniquement le certificat d’entité finale.<br/>                                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Signataire**](signer.md)
</dt> </dl>

 

 
