---
description: Définit une fonction de rappel à utiliser pendant la reconnaissance de ligne.
ms.assetid: 0b07ec80-328a-471b-b554-fa66f56a2871
title: SetLineRecoCallback fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineRecoCallback
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: b256a38d6d6ee6ecf43994c6619c369ea6ca2212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203424"
---
# <a name="setlinerecocallback-function"></a>SetLineRecoCallback fonction)

Définit une fonction de rappel à utiliser pendant la reconnaissance de ligne.

Cette fonction d’assistance n’est pas destinée à être utilisée par le code d’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI SetLineRecoCallback(
  _In_ INT_PTR        hDivider,
       GetLineRecoDef pfn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDivider* \[ dans\]
</dt> <dd>

Handle de l’objet [**InkDivider**](inkdivider-class.md) .

</dd> <dt>

*PFN* 
</dt> <dd>

Pointeur vers une fonction qui est appelée lorsque la reconnaissance se produit sur le [**InkDivider**](inkdivider-class.md) passé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction peut retourner l’une de ces valeurs.



| Code de retour                                                                                  | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La fonction a réussi.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Le paramètre *pDivider* n’est pas valide.<br/> |



 

## <a name="remarks"></a>Notes

Voici la syntaxe de la fonction de rappel.

``` syntax
public delegate void GetLineRecoDef(
        int cStrokes, 
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.I4, SizeParamIndex = 0)]int [] aStrokeIds, 
        float degrees, 
        Point point, 
        [MarshalAs(UnmanagedType.BStr)] out string lineString, 
        out int cSegment, 
        out int[] strokeIdOrdered, 
        out int[] segmentStrokes,
        [MarshalAs(UnmanagedType.LPArray, ArraySubType = UnmanagedType.BStr)] out string [] aSegmentString
    );
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Bibliothèque<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




