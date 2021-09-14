---
description: Retourne un tableau de fournisseurs de protocoles SSL (SSL (Secure Sockets Layer) Protocole) installés.
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: SslEnumProtocolProviders, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 94c8648950af20a97bcc34b614aee0d0f716b043
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013621"
---
# <a name="sslenumprotocolproviders-function"></a>SslEnumProtocolProviders fonction)

La fonction **SslEnumProtocolProviders** retourne un tableau de fournisseurs de protocole SSL ( [*SSL (Secure Sockets Layer) protocole*](/windows/desktop/SecGloss/s-gly) ) installés.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdwProviderCount* \[ à\]
</dt> <dd>

Pointeur vers une valeur **DWORD** pour recevoir le nombre de fournisseurs de protocole retourné.

</dd> <dt>

*ppProviderList* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit le tableau de structures [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NPD \_ \_Indicateurs INcorrects**</dt> <dt>0x80090009L</dt> </dl>         | Le paramètre *dwFlags* n’est pas égal à zéro.<br/>                              |
| <dl> <dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt> </dl>         | La mémoire disponible est insuffisante pour allouer les tampons nécessaires.<br/>     |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | Le paramètre *pdwProviderCount* ou *PpProviderList* a la **valeur null**.<br/> |



 

## <a name="remarks"></a>Notes

Lorsque vous avez fini d’utiliser le tableau de structures [**NCryptProviderName**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) , appelez la fonction [**SslFreeBuffer**](sslfreebuffer.md) pour libérer le tableau.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

