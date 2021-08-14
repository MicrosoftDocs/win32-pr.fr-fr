---
description: Obtient une valeur qui indique si le type MIME spécifié est pris en charge par la source du média.
ms.assetid: 894ef7d2-d008-42e1-8a61-26f35a8877be
title: 'IMFMediaSourceExtension :: IsTypeSupported, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: e2292ab717914e29a7741fed997b0f8b8b16e152e2fa889dd7ecb04bbb98aaea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974338"
---
# <a name="imfmediasourceextensionistypesupported-method"></a>IMFMediaSourceExtension :: IsTypeSupported, méthode

Obtient une valeur qui indique si le type MIME spécifié est pris en charge par la source du média.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsTypeSupported(
  [in] BSTR type
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*type* \[ dans\]
</dt> <dd>

Type de média pour lequel vérifier la prise en charge.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**true** si le type de média est pris en charge ; Sinon, **false**.

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

 

 




