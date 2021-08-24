---
description: Définit un pointeur vers une fonction de rappel facultative qui calcule le pourcentage de calculs de l’harmonique sphérique (SH) terminé et donne à l’appelant la possibilité d’abandonner le simulateur.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'ID3DXPRTEngine :: SetCallBack, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1ed2570c45380ce4faa0be42ddb9231d6420940dd9a6d669d6f2540154dc644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847358"
---
# <a name="id3dxprtenginesetcallback-method"></a>ID3DXPRTEngine :: SetCallBack, méthode

Définit un pointeur vers une fonction de rappel facultative qui calcule le pourcentage de calculs de l’harmonique sphérique (SH) terminé et donne à l’appelant la possibilité d’abandonner le simulateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PCB* \[ dans\]
</dt> <dd>

Type : **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Pointeur vers la fonction de rappel [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) qui calcule le pourcentage de calculs SH terminés. La fonction de rappel doit être implémentée pour retourner \_ OK pour continuer à exécuter le simulateur. Toute autre valeur abandonne le simulateur.

</dd> <dt>

*Fréquence* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Fréquence des appels de rappel. L’inverse de la fréquence est approximativement le nombre de fois où la fonction de rappel sera appelée.

</dd> <dt>

*lpUserContext* \[ dans\]
</dt> <dd>

Type : **[ **LPVOID**](../winprog/windows-data-types.md)**

Pointeur vers une valeur définie par l’utilisateur qui est passée à la fonction de rappel. Généralement utilisé par une application pour passer un pointeur vers une structure de données qui fournit des informations de contexte pour la fonction de rappel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est \_ OK.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
