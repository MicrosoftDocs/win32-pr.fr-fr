---
description: Obtient une valeur qui indique si le système de clés spécifié prend en charge le type de média spécifié.
ms.assetid: 6f4f50db-e491-46c2-a8b2-1b8e51033b5b
title: 'IMFMediaEngineClassFactoryEx :: IsTypeSupported, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineClassFactoryEx.IsTypeSupported
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 92bf3d64d36c043e9e33b897294ff74a3fda0445
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106537160"
---
# <a name="imfmediaengineclassfactoryexistypesupported-method"></a>IMFMediaEngineClassFactoryEx :: IsTypeSupported, méthode

Obtient une valeur qui indique si le système de clés spécifié prend en charge le type de média spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsTypeSupported(
   BSTR type,
   BSTR keySystem,
   BOOL *isSupported
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*type* 
</dt> <dd>

Type MIME pour lequel vérifier la prise en charge.

</dd> <dt>

*Système* 
</dt> <dd>

Système de clé pour lequel vérifier la prise en charge.

</dd> <dt>

*isSupported* 
</dt> <dd>

**true** si le type est pris en charge par *keysystem*; Sinon, **false.**

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

[**IMFMediaEngineClassFactoryEx**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex)
</dt> </dl>

 

 




