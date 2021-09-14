---
title: Méthode IDWriteTextLayout2 GetMetrics
description: Récupère les métriques globales de la chaîne mise en forme.
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
keywords:
- Écriture directe de la méthode GetMetrics
- Méthode GetMetrics Write directe, interface IDWriteTextLayout2
- Écriture directe de l’interface IDWriteTextLayout2, méthode GetMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout2.GetMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e393dfabb632641125d915e85f275977b20f0326
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119782"
---
# <a name="idwritetextlayout2getmetrics-method"></a>IDWriteTextLayout2 :: GetMetrics, méthode

Récupère les métriques globales de la chaîne mise en forme.

## <a name="syntax"></a>Syntaxe


```C++
virtual HRESULT GetMetrics(
  [out] DWRITE_TEXT_METRICS1 * textMetrics
) = 0;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

 *textMetrics* \[ à\]
</dt> <dd>

Tapez : **[ **DWRITE \_ Text \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1)\***

Lorsque cette méthode est retournée, contient les distances mesurées du texte et du contenu associé après avoir été mis en forme.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                          |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





