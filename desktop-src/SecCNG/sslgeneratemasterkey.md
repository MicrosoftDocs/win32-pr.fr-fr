---
description: Calcule la clé de secret principal du protocole SSL (Secure Sockets Layer) (SSL).
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: SslGenerateMasterKey, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ae8b357743cabf652721d3666c177990568718e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233393"
---
# <a name="sslgeneratemasterkey-function"></a>SslGenerateMasterKey fonction)

La fonction **SslGenerateMasterKey** calcule la clé de secret principal du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslGenerateMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  NCRYPT_KEY_HANDLE  hPublicKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
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

*hPublicKey* \[ dans\]
</dt> <dd>

Handle de la [*clé publique*](/windows/desktop/SecGloss/p-gly) utilisée dans l’échange.

</dd> <dt>

*phMasterKey* \[ à\]
</dt> <dd>

Pointeur vers le handle de la [*clé principale*](/windows/desktop/SecGloss/m-gly)générée.

</dd> <dt>

*dwProtocol* \[ dans\]
</dt> <dd>

L’une des valeurs d' [**identificateur de protocole du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*dwCipherSuite* \[ dans\]
</dt> <dd>

L’une des valeurs d’identificateur de la [**suite de chiffrement du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*pParameterList* \[ dans\]
</dt> <dd>

Pointeur vers un tableau de mémoires tampons [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) qui contiennent des informations utilisées dans le cadre de l’opération d’échange de clés. L’ensemble précis de mémoires tampons dépend du protocole et de la suite de chiffrement utilisés. Au minimum, la liste contient des mémoires tampons qui contiennent les valeurs aléatoires fournies par le client et le serveur.

</dd> <dt>

*pbOutput* \[ à\]
</dt> <dd>

Adresse d’une mémoire tampon qui reçoit le secret de prémaster chiffré avec la clé publique du serveur. Le paramètre *cbOutput* contient la taille de cette mémoire tampon. Si ce paramètre a la **valeur null**, cette fonction retourne la taille requise, en octets, dans la **valeur DWORD** pointée par le paramètre *pcbResult* .

> [!Note]  
> Ce tampon est utilisé lors de l’exécution d’un échange de clés RSA.

 

</dd> <dt>

*cbOutput* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon *pbOutput* .

</dd> <dt>

*pcbResult* \[ à\]
</dt> <dd>

Pointeur vers une valeur **DWORD** dans laquelle placer le nombre d’octets écrits dans la mémoire tampon *pbOutput* .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Spécifie si cette fonction est utilisée pour l’échange de clés côté client ou côté serveur.



| Valeur                                                                                                                                                                                                                                                      | Signification                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Indicateur client SSL**</dt> <dt>0x00000001</dt> </dl> | Spécifie un échange de clés côté client.<br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <dt>**NCRYPT \_ \_ \_ Indicateur de serveur SSL**</dt> <dt>0x00000002</dt> </dl> | Spécifie un échange de clés côté serveur.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt> </dl>         | La mémoire disponible est insuffisante pour allouer les tampons nécessaires.<br/> |
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | L’un des handles fournis n’est pas valide.<br/>                     |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | Le paramètre *phMasterKey* ou *hPublicKey* n’est pas valide.<br/>     |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

