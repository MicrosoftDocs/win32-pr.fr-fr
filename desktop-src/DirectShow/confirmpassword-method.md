---
description: La méthode DVDAdm. ConfirmPassword teste si le mot de passe spécifié correspond au mot de passe enregistré précédemment.
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: Méthode ConfirmPassword (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526111"
---
# <a name="confirmpassword-method"></a>Méthode ConfirmPassword

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `DVDAdm.ConfirmPassword` méthode teste si le mot de passe spécifié correspond au mot de passe enregistré précédemment.

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Spécifie le nom de l’utilisateur sous la forme d’une chaîne.

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Spécifie le nouveau mot de passe sous forme de chaîne.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la valeur true si le mot de passe spécifié correspond au mot de passe existant, false dans le cas contraire.

## <a name="remarks"></a>Notes

Actuellement, le paramètre *sUserName* est ignoré sur cette et toutes les méthodes associées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Segment. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ChangePassword**](changepassword-method.md)
</dt> <dt>

[Objet MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 




