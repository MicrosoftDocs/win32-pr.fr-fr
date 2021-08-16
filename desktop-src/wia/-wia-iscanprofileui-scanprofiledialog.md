---
description: Affiche une boîte de dialogue qui permet aux utilisateurs de créer, de modifier et de supprimer des profils de numérisation.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'IScanProfileUI :: ScanProfileDialog, méthode (Scanprofileui. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: a2003471a151677b5f0fbd9ae88e9d3cf8d975525a9dbf8340c6fc1a9f2befc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965808"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a>IScanProfileUI :: ScanProfileDialog, méthode

Affiche une boîte de dialogue qui permet aux utilisateurs de créer, de modifier et de supprimer des profils de numérisation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Type : **HWND**

Handle de la fenêtre parente qui possède la boîte de dialogue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

La boîte de dialogue est modale. l’utilisateur ne peut pas basculer vers la fenêtre parente tant que la boîte de dialogue n’est pas fermée.

Les valeurs de l' `<ProfileName>` élément et de l' `<WiaItem>` élément peuvent être modifiées dans la boîte de dialogue. L' `<Default>` élément peut être ajouté ou supprimé. Aucune autre modification du profil d’analyse ne peut être effectuée dans la boîte de dialogue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Scanprofileui. h</dt> </dl>  |
| MIDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IScanProfileUI**](-wia-iscanprofileui.md)
</dt> <dt>

[Analyser le schéma de profil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




