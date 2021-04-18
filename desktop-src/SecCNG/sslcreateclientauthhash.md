---
description: Récupère un handle vers le hachage de négociation utilisé pour l’authentification du client.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: SslCreateClientAuthHash, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4ac83d6d8aeea8429812d80b7bf66de7c87062a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533844"
---
# <a name="sslcreateclientauthhash-function"></a>SslCreateClientAuthHash fonction)

La fonction **SslCreateClientAuthHash** récupère un handle vers le [*hachage*](/windows/desktop/SecGloss/h-gly) de négociation utilisé pour l’authentification du client.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslCreateClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  LPCWSTR            pszHashAlgId,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*phHandshakeHash* \[ à\]
</dt> <dd>

Pointeur vers une variable **de \_ \_ handle de hachage NCRYPT** pour recevoir le descripteur de hachage.

</dd> <dt>

*dwProtocol* \[ dans\]
</dt> <dd>

L’une des valeurs d' [**identificateur de protocole du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ dans\]
</dt> <dd>

L’une des valeurs d’identificateur de la [**suite de chiffrement du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pszHashAlgId* \[ dans\]
</dt> <dd>

L’un des valeurs des [**identificateurs d’algorithme CNG**](cng-algorithm-identifiers.md) .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé pour une utilisation ultérieure et doit être défini à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | Le paramètre *hSslProvider* contient un pointeur qui n’est pas valide.<br/>                |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | Le paramètre *phHandshakeHash* a la valeur **null**.<br/>                               |
| <dl> <dt>**NPD \_ 0x80090029L non \_ pris en charge**</dt> <dt></dt> </dl>     | La fonction sélectionnée n’est pas prise en charge dans la version spécifiée de l’interface.<br/> |
| <dl> <dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt> </dl>         | Mémoire insuffisante pour allouer des tampons.<br/>                                          |
| <dl> <dt>**NPD \_ \_Indicateurs INcorrects**</dt> <dt>0x80090009L</dt> </dl>         | Le paramètre *dwFlags* doit avoir la valeur zéro.<br/>                                      |



 

## <a name="remarks"></a>Notes

La fonction **SslCreateClientAuthHash** est appelée pour les conversations TLS ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) 1,2 ou ultérieures pour créer des objets de hachage utilisés pour hacher les messages de négociation. Elle est appelée une fois pour chaque [*algorithme de hachage*](/windows/desktop/SecGloss/h-gly) possible qui peut être utilisé dans la signature d’authentification du client.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

