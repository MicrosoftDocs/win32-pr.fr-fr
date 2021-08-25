---
title: Méthode IConfigAsfWriter2 GetParam
description: La méthode GetParam récupère la valeur actuelle du paramètre de configuration de filtre spécifié.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- Méthode GetParam format Windows Media
- Méthode GetParam format Windows Media, interface IConfigAsfWriter2
- Interface IConfigAsfWriter2 Windows Media format, méthode GetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a411e4b1896174e25a1f671f3f42fd83c1376713f10e9e4cb2b2d2186b3d551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809139"
---
# <a name="iconfigasfwriter2getparam-method"></a>IConfigAsfWriter2 :: GetParam, méthode

La méthode **GetParam** récupère la valeur actuelle du paramètre de configuration de filtre spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwParam* \[ dans\]
</dt> <dd>

Spécifie le paramètre à récupérer. Il doit s’agir d’une valeur définie dans l’énumération [ \_ am \_ ASFWRITERCONFIG \_ param](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .

</dd> <dt>

*pdwParam1* \[ à\]
</dt> <dd>

Pointeur vers une variable qui récupère la valeur du paramètre spécifié dans *dwParam*.

</dd> <dt>

*pdwParam2* \[ à\]
</dt> <dd>

Non utilisé, doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d’échec, elle retourne un code d’erreur **HRESULT** .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2::SetParam**](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 