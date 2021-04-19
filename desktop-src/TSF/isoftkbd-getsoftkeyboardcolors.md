---
title: Méthode ISoftKbd GetSoftKeyboardColors (Softkbdc. h)
description: La méthode ISoftKbd GetSoftKeyboardColors récupère la couleur de clavier programmable correspondant au type de couleur fourni.
ms.assetid: d59d249c-a1c4-4d6a-add6-632be55a7549
keywords:
- Infrastructure des services de texte de méthode GetSoftKeyboardColors
- GetSoftKeyboardColors méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode GetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8f184dc04ddcbef18a9279000b1a68acd35bd3
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2021
ms.locfileid: "106523089"
---
# <a name="isoftkbdgetsoftkeyboardcolors-method"></a>ISoftKbd :: GetSoftKeyboardColors, méthode

La méthode **ISoftKbd :: GetSoftKeyboardColors** récupère la couleur de clavier programmable correspondant au type de couleur fourni.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSoftKeyboardColors(
  [in]  COLORTYPE colorType,
  [out] COLORREF  *lpColor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*colorType* \[ dans\]
</dt> <dd>

Valeur qui spécifie le type de couleur à récupérer pour le clavier conditionnel. Les valeurs possibles sont définies pour l’énumération [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) .

</dd> <dt>

*lpColor* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle cette méthode récupère une valeur [**COLORREF**](/windows/desktop/gdi/colorref) 32 bits spécifiant une couleur RVB.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L’un des paramètres n’est pas valide.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::SetSoftKeyboardColors**](/windows/desktop/TSF/isoftkbd-setsoftkeyboardcolors)
</dt> <dt>

[**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

