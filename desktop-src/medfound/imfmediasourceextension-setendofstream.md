---
description: Indique que la fin du flux multimédia a été atteinte.
ms.assetid: 6d6bffcc-aa3c-4825-9268-00dcd2a347e6
title: 'IMFMediaSourceExtension :: SetEndOfStream, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetEndOfStream
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 9018d76ce13bf441ea98134eb751f9e472f6bca8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523107"
---
# <a name="imfmediasourceextensionsetendofstream-method"></a>IMFMediaSourceExtension :: SetEndOfStream, méthode

Indique que la fin du flux multimédia a été atteinte.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetEndOfStream(
  [in] MF_MSE_ERROR error
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*erreur* \[ dans\]
</dt> <dd>

Utilisé pour transmettre les informations d’erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> <dt>

[**\_erreur de MSE MF \_**](mf-mse-error.md)
</dt> </dl>

 

 




