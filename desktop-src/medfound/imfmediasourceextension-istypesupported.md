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
ms.openlocfilehash: 4c2784dc4e97f96ae28ba56544a7f425de8ce742
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106523108"
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
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                      |
| MIDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




