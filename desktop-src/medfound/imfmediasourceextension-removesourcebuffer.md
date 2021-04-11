---
description: Supprime la mémoire tampon source spécifiée de la collection de mémoires tampons sources gérée par l’objet IMFMediaSourceExtension.
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: 'IMFMediaSourceExtension :: RemoveSourceBuffer, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 2a093401058895f31b29843778a18a040e722c33
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321582"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a>IMFMediaSourceExtension :: RemoveSourceBuffer, méthode

Supprime la mémoire tampon source spécifiée de la collection de mémoires tampons sources gérée par l’objet [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSourceBuffer* \[ dans\]
</dt> <dd>

Mémoire tampon à supprimer.

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
</dt> </dl>

 

 




