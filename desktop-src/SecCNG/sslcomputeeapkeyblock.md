---
description: Calcule le bloc de clé utilisé par le protocole EAP (Extensible Authentication Protocol).
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: SslComputeEapKeyBlock, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: d46c1284b208975126067ff295507b51def9133b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013640"
---
# <a name="sslcomputeeapkeyblock-function"></a>SslComputeEapKeyBlock fonction)

La fonction **SslComputeEapKeyBlock** calcule le bloc de clé utilisé par le protocole EAP (Extensible Authentication Protocol).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hMasterKey* \[ dans\]
</dt> <dd>

Handle de l’objet de [*clé principale*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*pbRandoms* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient une concaténation des valeurs aléatoires \_ aléatoires du client et du serveur \_ de la session SSL.

</dd> <dt>

*cbRandoms* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon *pbRandoms* .

</dd> <dt>

*pbOutput* \[ out, facultatif\]
</dt> <dd>

Adresse d’une mémoire tampon qui reçoit l’objet BLOB de clé. Le paramètre *cbOutput* contient la taille de cette mémoire tampon. Si ce paramètre a la **valeur null**, cette fonction place la taille requise, en octets, dans la **valeur DWORD** pointée par le paramètre *pcbResult* .

</dd> <dt>

*cbOutput* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon *pbOutput* .

</dd> <dt>

*pcbResult* \[ à\]
</dt> <dd>

Pointeur vers une valeur **DWORD** qui spécifie la longueur, en octets, du hachage écrit dans la mémoire tampon *pbOutput* .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Définissez sur **\_ indicateur de \_ serveur \_ NCRYPT** pour indiquer qu’il s’agit d’un appel de serveur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.



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



 

