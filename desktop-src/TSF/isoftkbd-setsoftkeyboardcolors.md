---
title: Méthode ISoftKbd SetSoftKeyboardColors (Softkbdc. h)
description: La méthode ISoftKbd SetSoftKeyboardColors définit la couleur du clavier logiciel pour le type de couleur spécifié.
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- Infrastructure des services de texte de méthode SetSoftKeyboardColors
- SetSoftKeyboardColors méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b572d62895a4f5df503df3ed78bfcf931af331ded25596267f0dd5b4286a4c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118877370"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a>ISoftKbd :: SetSoftKeyboardColors, méthode

La méthode **ISoftKbd :: SetSoftKeyboardColors** définit la couleur du clavier logiciel pour le type de couleur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*colorType* \[ dans\]
</dt> <dd>

Valeur qui spécifie le type de couleur du clavier conditionnel. Les valeurs possibles sont définies pour l’énumération [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) .

</dd> <dt>

*Couleur* \[ dans\]
</dt> <dd>

Valeur [**COLORREF**](/windows/desktop/gdi/colorref) 32 bits spécifiant une couleur RVB.

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
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 Professional<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::GetSoftKeyboardColors**](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[**COLORREF**](/windows/desktop/gdi/colorref)
</dt> </dl>

 

