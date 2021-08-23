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
ms.openlocfilehash: bd86df70eed27fb192e65b23ea567beb1f4b42001dd3df5e5381045387dc1490
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874659"
---
# <a name="encrypteddatacontent-property"></a>EncryptedData. Content, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt les services d’appel de code non managé (PInvoke) pour appeler les fonctions de l’API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) et [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) pour chiffrer et déchiffrer les messages. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

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
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 
