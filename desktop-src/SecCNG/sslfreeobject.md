---
description: Libère un objet de clé, de hachage ou de fournisseur.
ms.assetid: 73fa0a08-4654-4515-bdb2-9951936b689a
title: SslFreeObject, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeObject
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7415ac31147f08bec038da5af57e8a4bc0cc4d2d3f39cb3b8391f42dfcff21b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906488"
---
# <a name="sslfreeobject-function"></a>SslFreeObject fonction)

La fonction **SslFreeObject** libère un objet de clé, de hachage ou de fournisseur.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslFreeObject(
  _In_ NCRYPT_HANDLE hObject,
  _In_ DWORD         dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hObject* \[ dans\]
</dt> <dd>

Handle de l’objet à libérer.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé à un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                       | Description                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl>    | Un descripteur interne n’est pas valide.<br/>  |
| <dl> <dt>**État \_ \_Handle 0XC0000008L non valide**</dt> <dt></dt> </dl> | Le handle fourni n’est pas valide.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




