---
description: Obtient l’objet de clés multimédia associé au moteur multimédia ou null s’il n’y a pas d’objet de clés multimédia.
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: 'IMFMediaEngineEME :: get_Keys, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530821"
---
# <a name="imfmediaengineemeget_keys-method"></a>IMFMediaEngineEME :: méthode d’extraction de \_ clés

Obtient l’objet de clés multimédia associé au moteur multimédia ou **null** s’il n’y a pas d’objet de clés multimédia.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*clés* 
</dt> <dd>

L’objet de clés multimédia associé au moteur multimédia ou **null** s’il n’existe pas d’objet de clés multimédia.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaEngineEME**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 




