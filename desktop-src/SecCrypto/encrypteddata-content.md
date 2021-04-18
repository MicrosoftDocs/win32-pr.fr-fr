---
description: Définit ou récupère le contenu à chiffrer ou à déchiffrer.
ms.assetid: fdab0f19-c69e-443b-b4b3-079d23028921
title: EncryptedData. Content, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4b873d40ed04270defe04fd59f0ce00a0f84040a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525964"
---
# <a name="encrypteddatacontent-property"></a>EncryptedData. Content, propriété

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt les services d’appel de code non managé (PInvoke) pour appeler les fonctions de l’API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) et [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) pour chiffrer et déchiffrer les messages. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

La propriété de **contenu** définit ou récupère le contenu à chiffrer ou à déchiffrer. Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
EncryptedData.Content As String
```



## <a name="property-value"></a>Valeur de la propriété

Contenu à chiffrer ou à déchiffrer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 
