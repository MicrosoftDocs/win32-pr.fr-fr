---
description: Définit la valeur du secret utilisé pour dériver la clé de session de chiffrement utilisée pour chiffrer et déchiffrer les données.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: EncryptedData. SetSecret, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c8d30355b022a593ca17519e3ccfa876a5b07b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540998"
---
# <a name="encrypteddatasetsecret-method"></a>EncryptedData. SetSecret, méthode

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt les services d’appel de code non managé (PInvoke) pour appeler les fonctions de l’API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) et [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) pour chiffrer et déchiffrer les messages. Pour plus d’informations sur PInvoke, consultez Didacticiel sur l’appel de code non [managé](https://msdn.microsoft.com/library/aa288468.aspx). Le [.net et CryptoAPI via p/Invoke : part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) et [.net et CryptoAPI via p/Invoke : partie 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sous-sections de l' [extension du chiffrement .net avec CAPICOM et P/Invoke](/previous-versions/ms867087(v=msdn.10)) peuvent également s’avérer utiles.\]

La méthode **SetSecret** définit la valeur du secret utilisé pour dériver la [*clé de session*](../secgloss/s-gly.md) de chiffrement utilisée pour chiffrer et déchiffrer les données.

## <a name="syntax"></a>Syntaxe


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newVal* \[ dans\]
</dt> <dd>

Chaîne qui contient un secret utilisé pour créer une clé de chiffrement de session.

</dd> <dt>

*SecretType* \[ dans, facultatif\]
</dt> <dd>

Valeur de l’énumération de [**\_ \_ type secret CAPICOM**](capicom-secret-type.md) qui indique le type de secret utilisé pour générer la clé de session. La valeur par défaut est CAPICOM \_ secret secret \_ . Ce paramètre peut avoir la valeur suivante.



| Valeur                                                                                                                                                                                        | Signification                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <dt>**\_ \_ mot de passe secret de CAPICOM**</dt> </dl> | La clé de chiffrement doit être dérivée d’un mot de passe.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le secret est utilisé pour créer la clé de session pour le chiffrement ou le déchiffrement. La même clé secrète doit être utilisée pour les deux opérations. Si le secret utilisé pour chiffrer les données est perdu, les données chiffrées ne peuvent pas être déchiffrées.

Si c’est approprié pour votre application, envisagez d’utiliser [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) ou [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) pour protéger la clé secrète avant et après l’utilisation. Effacez la mémoire associée à la clé secrète lorsque vous avez terminé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> <dt>

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 
