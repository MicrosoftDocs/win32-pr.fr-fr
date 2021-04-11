---
description: Ouvre un handle vers le fournisseur de protocole SSL (SSL (Secure Sockets Layer) Protocol) spécifié.
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: SslOpenProvider, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenProvider
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8a9ea6c97662d94fffef0c87a227d5e2ae052606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201355"
---
# <a name="sslopenprovider-function"></a>SslOpenProvider fonction)

La fonction **SslOpenProvider** ouvre un handle pour le fournisseur de protocole SSL ( [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ) spécifié.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslOpenProvider(
  _Out_ NCRYPT_PROV_HANDLE *phSslProvider,
  _In_  LPCWSTR            pszProviderName,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phSslProvider* \[ à\]
</dt> <dd>

Adresse d’un **handle NCRYPT \_ Prov \_** dans lequel écrire le descripteur du fournisseur.

Lorsque vous avez fini d’utiliser le descripteur, vous devez le libérer en appelant la fonction [**SslFreeObject**](sslfreeobject.md) .

</dd> <dt>

*pszProviderName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode qui contient le nom du fournisseur. Si la valeur de ce paramètre est **null**, un descripteur **du \_ \_ fournisseur MS Schannel** est retourné.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à une utilisation ultérieure et doit être défini à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | L’un des handles fournis n’est pas valide.<br/>                      |
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | Le paramètre *phSslProvider* ou *PpProviderList* a la **valeur null**.<br/> |
| <dl> <dt>**État \_ AUCUNE \_ mémoire**</dt> <dt>0xC0000017L</dt> </dl>      | La mémoire disponible est insuffisante pour allouer les tampons nécessaires.<br/>  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

