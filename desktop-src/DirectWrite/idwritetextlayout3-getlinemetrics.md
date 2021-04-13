---
title: Méthode IDWriteTextLayout3 GetLineMetrics
description: Récupère les propriétés de chaque ligne.
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- Écriture directe de la méthode GetLineMetrics
- Méthode GetLineMetrics Write directe, interface IDWriteTextLayout3
- Écriture directe de l’interface IDWriteTextLayout3, méthode GetLineMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465842"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a>IDWriteTextLayout3 :: GetLineMetrics, méthode

Récupère les propriétés de chaque ligne.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lineMetrics* \[ à\]
</dt> <dd>

Tableau à remplir avec les informations de ligne.

</dd> <dt>

*maxLineCount* 
</dt> <dd>

Taille maximale du tableau lineMetrics.

</dd> <dt>

*actualLineCount* \[ à\]
</dt> <dd>

Taille réelle du tableau lineMetrics nécessaire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Si maxLineCount n’est pas assez grand \_ \_ , E \_ mémoire tampon insuffisante, qui est équivalente à HRESULT \_ de \_ Win32 (erreur de \_ mémoire tampon insuffisante \_ ), est retourné et actualLineCount est défini sur le nombre de lignes nécessaires.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                                 |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/> |
| Bibliothèque<br/>                  | <dl> <dt>DWrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





