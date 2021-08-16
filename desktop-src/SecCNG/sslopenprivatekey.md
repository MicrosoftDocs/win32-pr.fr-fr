---
description: Ouvre un handle vers une clé privée.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: SslOpenPrivateKey, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: bab1451ada84576ee33623dfdaa7d8dcad189e6d4ef8050b0b79fafaba11b49c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905648"
---
# <a name="sslopenprivatekey-function"></a>SslOpenPrivateKey fonction)

La fonction **SslOpenPrivateKey** ouvre un handle vers une [*clé privée*](/windows/desktop/SecGloss/p-gly).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*phPrivateKey* \[ à\]
</dt> <dd>

Adresse d’une mémoire tampon dans laquelle écrire le descripteur de la clé privée.

Lorsque vous avez fini d’utiliser la clé, vous devez libérer *phPrivateKey* en appelant la fonction [**SslFreeObject**](sslfreeobject.md) .

</dd> <dt>

*pCertContext* \[ dans\]
</dt> <dd>

Adresse du certificat à partir duquel obtenir la clé privée.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt> </dl>         | La mémoire disponible est insuffisante pour allouer les tampons nécessaires.<br/> |
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | Le descripteur *hSslProvider* n’est pas valide.<br/>                       |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | Le paramètre *phPrivateKey* ou *PCertContext* a la **valeur null**.<br/>   |



 

## <a name="remarks"></a>Remarques

La clé privée obtenue fait partie d’une [*paire de clés publique/privée*](/windows/desktop/SecGloss/p-gly) au sein d’un [*certificat*](/windows/desktop/SecGloss/c-gly). Cette fonction extrait simplement la clé privée du certificat spécifié par le paramètre *pCertContext* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

