---
description: Définit la durée de la source du média en unités de 100 nanosecondes.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: 'IMFMediaSourceExtension :: SetDuration, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414254"
---
# <a name="imfmediasourceextensionsetduration-method"></a>IMFMediaSourceExtension :: SetDuration, méthode

Définit la durée de la source du média en unités de 100 nanosecondes.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*durée* \[ dans\]
</dt> <dd>

Durée de la source du média en unités de 100 nanosecondes.

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

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




