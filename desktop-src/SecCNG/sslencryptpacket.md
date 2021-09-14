---
description: Chiffre un paquet SSL (Single SSL (Secure Sockets Layer) Protocol).
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: SslEncryptPacket, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEncryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e839b37e839fd09d5df5f9902474b7ce7c4c74a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013624"
---
# <a name="sslencryptpacket-function"></a>SslEncryptPacket fonction)

La fonction **SslEncryptPacket** chiffre un paquet SSL (Single [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslEncryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwContentType,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole SSL.

</dd> <dt>

*HKEY* \[ in, out\]
</dt> <dd>

Handle de la clé utilisée pour chiffrer le paquet.

</dd> <dt>

*pbInput* \[ dans\]
</dt> <dd>

Pointeur vers la mémoire tampon qui contient le paquet à chiffrer.

</dd> <dt>

*cbInput* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon *pbInput* .

</dd> <dt>

*pbOutput* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon destinée à recevoir le paquet chiffré.

</dd> <dt>

*cbOutput* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon *pbOutput* .

</dd> <dt>

*pcbResult* \[ à\]
</dt> <dd>

Nombre d’octets écrits dans la mémoire tampon *pbOutput* .

</dd> <dt>

 N \[ dans\]
</dt> <dd>

Numéro de séquence qui correspond à ce paquet.

</dd> <dt>

*dwContentType* \[ dans\]
</dt> <dd>

Type de contenu qui correspond à ce paquet, qui spécifie le protocole de niveau supérieur utilisé pour traiter le paquet délimité.



| Valeur                                                                                                                                                                                                                                           | Signification                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <dt>**CT \_ MODIFIER \_ la \_ spécification de chiffrement**</dt> <dt>20</dt> </dl> | Indique une modification de la stratégie de chiffrement.<br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <dt>**CT \_ ALERTE**</dt> <dt>21</dt> </dl>                                          | Indique que le paquet délimité contient une alerte.<br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <dt>**CT \_ NÉGOCIATION**</dt> <dt>22</dt> </dl>                              | Indique que le paquet délimité fait partie du protocole de négociation.<br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <dt>**CT \_ APPLICATIONDATA**</dt> <dt>23</dt> </dl>            | Indique que le paquet contient des données d’application.<br/>                  |



 

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                    | Description                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl> | L’un des handles fournis n’est pas valide.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

