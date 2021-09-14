---
description: Fournit des propriétés et des méthodes pour chiffrer et déchiffrer des données à l’aide d’une clé de session dérivée d’un secret.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: Objet EncryptedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 123e0973343e4990dd2d49cfb321d739085358f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416428"
---
# <a name="encrypteddata-object"></a>Objet EncryptedData

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt les services d’appel de code non managé (PInvoke) pour appeler les fonctions de l’API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) et [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) pour chiffrer et déchiffrer les messages. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

L’objet **EncryptedData** fournit des propriétés et des méthodes pour chiffrer et déchiffrer des données à l’aide d’une [*clé de session*](../secgloss/s-gly.md) dérivée d’un secret.

> [!Note]  
> CAPICOM ne prend pas en charge le \# type de contenu PKCS 7 EncryptedData, mais utilise une structure ASN non standard pour **EncryptedData**. Par conséquent, seul CAPICOM peut déchiffrer un objet CAPICOM **EncryptedData** .

 

## <a name="members"></a>Membres

L’objet **EncryptedData** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **EncryptedData** possède ces méthodes.



| Méthode                                       | Description                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [**Crypté**](encrypteddata-decrypt.md)     | Déchiffre le contenu chiffré à l’aide de la clé secrète.<br/>                                 |
| [**Codage**](encrypteddata-encrypt.md)     | Chiffre le contenu à l’aide du secret et de l’algorithme de chiffrement actuels.<br/>      |
| [**SetSecret**](encrypteddata-setsecret.md) | Définit le secret à partir duquel la clé de session de chiffrement/déchiffrement est dérivée.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **EncryptedData** a ces propriétés.



| Propriété                                                | Type d’accès           | Description                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithme**](encrypteddata-algorithm.md)<br/> | Lecture seule<br/>  | Algorithme utilisé pour le chiffrement/déchiffrement.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Humidité**](encrypteddata-content.md)<br/>     | Lecture/écriture<br/> | Contenu à chiffrer ou à déchiffrer. La définition de cette propriété doit être effectuée avant l’appel de la méthode [**Encrypt**](encrypteddata-encrypt.md) . <br/> Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée et tout contenu chiffré dans l’objet est perdu.<br/> Il s’agit de la propriété par défaut.<br/> |



 

## <a name="remarks"></a>Notes

L’objet **EncryptedData** peut être créé et il est sécurisé pour les scripts. Le ProgID de l’objet **EncryptedData** est CAPICOM. EncryptedData. 1.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> </dl>

 

 
