---
title: Méthode ISoftKbd CreateSoftKeyboardWindow (Softkbdc. h)
description: La méthode ISoftKbd CreateSoftKeyboardWindow crée une fenêtre de clavier temporaire.
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- Infrastructure des services de texte de méthode CreateSoftKeyboardWindow
- CreateSoftKeyboardWindow méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode CreateSoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ed6f9f91f335945d40dd0b995226a400965ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508994"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a>ISoftKbd :: CreateSoftKeyboardWindow, méthode

La méthode **ISoftKbd :: CreateSoftKeyboardWindow** crée une fenêtre de clavier temporaire.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateSoftKeyboardWindow(
  [in] HWND          hOwner,
  [in] TITLEBAR_TYPE Titlebar_type,
  [in] INT           xPos,
  [in] INT           yPos,
  [in] INT           width,
  [in] INT           height
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hOwner* \[ dans\]
</dt> <dd>

Handle de la fenêtre qui contient le clavier conditionnel.

</dd> <dt>

*\_ Type de TitleBar* \[ dans\]
</dt> <dd>

Type de barre de titre de la fenêtre du clavier conditionnel. Les types possibles sont définis par l’énumération de [**\_ type TITLEBAR**](titlebar-type.md) .

</dd> <dt>

*xpos* \[ dans\]
</dt> <dd>

Position x du coin supérieur gauche de la fenêtre de clavier temporaire.

</dd> <dt>

*Posy* \[ dans\]
</dt> <dd>

Position y du coin supérieur gauche de la fenêtre de clavier temporaire.

</dd> <dt>

*largeur* \[ dans\]
</dt> <dd>

Largeur de la fenêtre de clavier temporaire.

</dd> <dt>

*hauteur* \[ dans\]
</dt> <dd>

Hauteur de la fenêtre du clavier conditionnel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                        | Description                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | La méthode a réussi.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Un ou plusieurs paramètres ne sont pas valides.<br/> |



 

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

[**ISoftKbd::CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[**ISoftKbd ::D estroySoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[**ISoftKbd::ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[**TYPE de TITLEBAR \_**](titlebar-type.md)
</dt> </dl>

 

 





