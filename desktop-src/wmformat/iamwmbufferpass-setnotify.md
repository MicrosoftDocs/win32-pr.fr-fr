---
title: Méthode IAMWMBufferPass SetNotify
description: La méthode SetNotify est utilisée par les applications pour fournir l’enregistreur ASF WM ou le filtre de lecteur ASF WM avec un pointeur vers l’interface IAMWMBufferPassCallback de l’application.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- Méthode SetNotify format Windows Media
- Méthode SetNotify format Windows Media, interface IAMWMBufferPass
- Interface IAMWMBufferPass Windows Media format, méthode SetNotify
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47e189a2654ed4c760fdfcd6ced5506cc90d5e7cc989a7f79979e6d95b0bbfb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847605"
---
# <a name="iamwmbufferpasssetnotify-method"></a>IAMWMBufferPass :: SetNotify, méthode

La méthode **SetNotify** est utilisée par les applications pour fournir l’enregistreur ASF WM ou le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) avec un pointeur vers l’interface [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) de l’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCallback* \[ dans\]
</dt> <dd>

Pointeur vers l’interface **IAMWMBufferPassCallback** de l’application.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d’échec, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Appelez cette méthode avant de placer le graphique de filtre dans l’état d’exécution.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 