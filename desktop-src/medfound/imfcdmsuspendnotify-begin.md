---
description: Indique que le processus de suspension démarre et que les ressources doivent être mises dans un état cohérent.
ms.assetid: 5cf3d249-3d8b-4596-9d8b-e7b95a270eff
title: 'IMFCdmSuspendNotify :: Begin, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFCdmSuspendNotify.Begin
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 84453a6c846e88a9d6e6c32c5253d97d36e89c7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749661"
---
# <a name="imfcdmsuspendnotifybegin-method"></a>IMFCdmSuspendNotify :: Begin, méthode

Indique que le processus de suspension démarre et que les ressources doivent être mises dans un état cohérent.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Begin();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

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

[**IMFCdmSuspendNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify)
</dt> </dl>

 

 




