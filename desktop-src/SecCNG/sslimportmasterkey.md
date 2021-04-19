---
description: Effectue une opération d’échange de clés SSL (Server-Side SSL (Secure Sockets Layer) Protocol).
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: SslImportMasterKey, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e21c4cd0f6e51662124e02881b82c905dba68c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534257"
---
# <a name="sslimportmasterkey-function"></a>SslImportMasterKey fonction)

La fonction **SslImportMasterKey** effectue une opération d’échange de clés SSL (Server-Side [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslImportMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  PBYTE              pbEncryptedKey,
  _In_  DWORD              cbEncryptedKey,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole SSL.

</dd> <dt>

*hPrivateKey* \[ dans\]
</dt> <dd>

Handle de la [*clé privée*](/windows/desktop/SecGloss/p-gly) utilisée dans l’échange.

</dd> <dt>

*phMasterKey* \[ à\]
</dt> <dd>

Pointeur vers le handle pour recevoir la [*clé principale*](/windows/desktop/SecGloss/m-gly).

</dd> <dt>

*dwProtocol* \[ dans\]
</dt> <dd>

L’une des valeurs d' [**identificateur de protocole du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ dans\]
</dt> <dd>

L’un des valeurs d' [**identificateurs de la suite de chiffrement du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pParameterList* \[ dans\]
</dt> <dd>

Pointeur vers un tableau de mémoires tampons [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) qui contiennent des informations utilisées dans le cadre de l’opération d’échange de clés. L’ensemble précis de mémoires tampons dépend du protocole et de la suite de chiffrement utilisés. Au minimum, la liste contient des mémoires tampons qui contiennent les valeurs aléatoires fournies par le client et le serveur.

</dd> <dt>

*pbEncryptedKey* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient la clé secrète de prémaster chiffrée chiffrée avec la [*clé publique*](/windows/desktop/SecGloss/p-gly) du serveur.

</dd> <dt>

*cbEncryptedKey* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon *pbEncryptedKey* .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Définissez ce paramètre sur **l' \_ \_ \_ indicateur de serveur SSL NCRYPT** pour indiquer qu’il s’agit d’un appel de serveur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt> </dl>         | La mémoire disponible est insuffisante pour allouer les tampons nécessaires.<br/> |
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | L’un des handles fournis n’est pas valide.<br/>                     |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | Le paramètre *phMasterKey* a la **valeur null**.<br/>                      |



 

## <a name="remarks"></a>Notes

Cette fonction déchiffre le secret de prémaster, calcule le secret principal SSL et retourne un handle vers cet objet à l’appelant. Cette clé principale peut ensuite être utilisée pour dériver la clé de session SSL et terminer le protocole de transfert SSL.

> [!Note]  
> Cette fonction est utilisée lorsque l’algorithme d’échange de clés [*RSA*](/windows/desktop/SecGloss/r-gly) est utilisé. Lorsque [*DH*](/windows/desktop/SecGloss/d-gly) est utilisé, le code serveur appelle [**SslGenerateMasterKey**](sslgeneratemasterkey.md) à la place.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

