---
description: Ajoute un IMFSourceBuffer à la collection de mémoires tampons associée au IMFMediaSourceExtension.
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
title: 'IMFMediaSourceExtension :: AddSourceBuffer, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.AddSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: b49a7c4fb0cb9e45ab0c2823d92ceb6e4076dfcaef4d2e8450f1f3d07f474279
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942029"
---
# <a name="imfmediasourceextensionaddsourcebuffer-method"></a>IMFMediaSourceExtension :: AddSourceBuffer, méthode

Ajoute un [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) à la collection de mémoires tampons associée au [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddSourceBuffer(
  [in]  BSTR                  type,
  [in]  IMFSourceBufferNotify *pNotify,
  [out] IMFSourceBuffer       **ppSourceBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*type* \[ dans\]
</dt> <dd></dd> <dt>

*pNotify* \[ dans\]
</dt> <dd></dd> <dt>

*ppSourceBuffer* \[ à\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




