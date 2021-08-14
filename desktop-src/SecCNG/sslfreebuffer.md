---
description: Utilisé pour libérer de la mémoire qui a été allouée par l’une des fonctions du fournisseur SSL (SSL (Secure Sockets Layer) Protocol).
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: SslFreeBuffer, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeBuffer
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6121802b8815a2e13fab0f4336420b763fe931a6e022fcce73080adfb01197c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906478"
---
# <a name="sslfreebuffer-function"></a>SslFreeBuffer fonction)

La fonction **SslFreeBuffer** est utilisée pour libérer de la mémoire qui a été allouée par l’une des fonctions du fournisseur SSL ( [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pvInput* \[ dans\]
</dt> <dd>

Pointeur vers la mémoire tampon à libérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt> </dl> | Le paramètre *pdwProviderCount* ou *PpProviderList* a la **valeur null**.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

