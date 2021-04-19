---
title: Méthode IDWriteInlineObject GetOverhangMetrics
description: IDWriteTextLayout appelle cette fonction de rappel pour récupérer les étendues visibles (en DIP) de l’objet Inline. Dans le cas d’une image bitmap simple, sans remplissage ni dépassement, tous les surblocages sont simplement des zéros.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Écriture directe de la méthode GetOverhangMetrics
- Méthode GetOverhangMetrics Write directe, interface IDWriteInlineObject
- Écriture directe de l’interface IDWriteInlineObject, méthode GetOverhangMetrics
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0960f28394c5b55c3377136451a5c13748edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538132"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a>IDWriteInlineObject :: GetOverhangMetrics, méthode

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) appelle cette fonction de rappel pour récupérer les étendues visibles (en DIP) de l’objet Inline. Dans le cas d’une image bitmap simple, sans remplissage ni dépassement, tous les surblocages sont simplement des zéros.

Les surblocages doivent être retournés par rapport à la taille signalée de l’objet (consultez mesures de l' [**\_ \_ objet \_ inline DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) et ne doivent pas être ajustées à la ligne de base.

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

Dépassement des étendues visibles (en DIP) à l’extérieur de l’objet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

