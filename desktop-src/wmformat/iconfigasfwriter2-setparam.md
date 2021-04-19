---
title: Méthode IConfigAsfWriter2 SetParam
description: La méthode SetParam définit la valeur du paramètre de configuration de filtre spécifié.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- Méthode SetParam format Windows Media
- Méthode SetParam format Windows Media, interface IConfigAsfWriter2
- Interface IConfigAsfWriter2 Windows Media format, méthode SetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f123bf11c8297f3a7ce0d4b0047874d8d7b31b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511301"
---
# <a name="iconfigasfwriter2setparam-method"></a>IConfigAsfWriter2 :: SetParam, méthode

La méthode **setParam** définit la valeur du paramètre de configuration de filtre spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwParam* \[ dans\]
</dt> <dd>

Spécifie le paramètre à définir. Il doit s’agir d’une valeur définie dans l’énumération [ \_ am \_ ASFWRITERCONFIG \_ param](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .

</dd> <dt>

*dwParam1* \[ dans\]
</dt> <dd>

Spécifie la valeur à assigner au paramètre *dwParam* .

</dd> <dt>

*dwParam2* \[ dans\]
</dt> <dd>

Non utilisé ; doit être égal à 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d’échec, elle retourne un code d’erreur **HRESULT** .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> <dt>

[**IConfigAsfWriter2 :: GetParam**](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 