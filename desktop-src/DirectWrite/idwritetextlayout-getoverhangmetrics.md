---
title: Méthode IDWriteTextLayout GetOverhangMetrics
description: Retourne les surblocages (en DIP) de la disposition et de tous les objets qu’elle contient, y compris les glyphes de texte et les objets insérés.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Écriture directe de la méthode GetOverhangMetrics
- Méthode GetOverhangMetrics Write directe, interface IDWriteTextLayout
- Écriture directe de l’interface IDWriteTextLayout, méthode GetOverhangMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3591df5dc02fdc63215ff2276202df62347ed21aef23991b4ddcadef094281
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649744"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a>IDWriteTextLayout :: GetOverhangMetrics, méthode

Retourne les surblocages (en DIP) de la disposition et de tous les objets qu’elle contient, y compris les glyphes de texte et les objets insérés.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*surblocages* \[ à\]
</dt> <dd>

Type : **[ **\_ \_ métriques de dépassement DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***

Dépassements d’étendues visibles (en DIP) en dehors de la disposition.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Les traits de soulignement et les strikethroughs ne contribuent pas à la détermination de la boîte noire, car ils sont réellement dessinés par le convertisseur, ce qui est autorisé à les dessiner dans n’importe quel ensemble de styles.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

