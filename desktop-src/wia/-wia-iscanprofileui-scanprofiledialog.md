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
ms.openlocfilehash: bc8707378f1debc322fea258ceb8aad0c6400ea0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219980"
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

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

La boîte de dialogue est modale. l’utilisateur ne peut pas basculer vers la fenêtre parente tant que la boîte de dialogue n’est pas fermée.

Les valeurs de l' `<ProfileName>` élément et de l' `<WiaItem>` élément peuvent être modifiées dans la boîte de dialogue. L' `<Default>` élément peut être ajouté ou supprimé. Aucune autre modification du profil d’analyse ne peut être effectuée dans la boîte de dialogue.

## <a name="requirements"></a>Spécifications



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

 

 




