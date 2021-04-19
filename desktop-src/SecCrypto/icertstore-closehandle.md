---
description: Ferme un handle HCERTSTORE acquis par le biais de la propriété StoreHandle.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: 'ICertStore :: CloseHandle, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bb1e9ab032b76b8ef02de786d1fc39af0b0d54b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540722"
---
# <a name="icertstoreclosehandle-method"></a>ICertStore :: CloseHandle, méthode

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]

La méthode **CloseHandle** ferme un handle HCERTSTORE acquis par le biais de la propriété [**StoreHandle**](icertstore-storehandle.md) .

## <a name="syntax"></a>Syntaxe


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hCertStore* \[ dans\]
</dt> <dd>

Handle HCERTSTORE à fermer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un **HRESULT**. La valeur **S \_ OK** indique la réussite de l’opération. Toute autre valeur indique que l’opération a échoué.

## <a name="remarks"></a>Notes

Cette méthode ne libère pas le handle HCERTSTORE contenu dans un objet de [**magasin**](store.md) . Elle doit être utilisée uniquement pour libérer un handle HCERTSTORE acquis par le biais de la propriété [**StoreHandle**](icertstore-storehandle.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




