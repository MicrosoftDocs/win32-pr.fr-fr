---
description: Permet d’indiquer qu’une erreur s’est produite avec la mémoire tampon source.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: 'IMFSourceBufferNotify :: OnError, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 8b5f48c3517eb62b0a70acb9cbb28a5ecf7c90cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516058"
---
# <a name="imfsourcebuffernotifyonerror-method"></a>IMFSourceBufferNotify :: OnError, méthode

Permet d’indiquer qu’une erreur s’est produite avec la mémoire tampon source.

## <a name="syntax"></a>Syntaxe


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RH* \[ dans\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFSourceBufferNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




