---
description: Enregistre les modifications apportées à un profil sur le disque.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: 'IScanProfile :: Save, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 6d4787380344a7bf8adb70f4cb5a3eaacdea403a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527087"
---
# <a name="iscanprofilesave-method"></a>IScanProfile :: Save, méthode

Enregistre les modifications apportées à un profil sur le disque.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Save();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Un profil de numérisation enregistré est un fichier XML stocké dans% USERPROFILE% \\ Application Data \\ \\ Center \\ UserScanProfiles.

Si plusieurs processus écrivent dans l’objet [**IScanProfile**](-wia-iscanprofile.md) , celui qui appelle **IScanProfile :: Save** Last est le seul processus dont les modifications sont enregistrées.

La méthode **IScanProfile :: Save** valide le profil avant l’enregistrement. Le profil est toujours considéré comme valide, sauf si la catégorie de l’élément d’acquisition d’images Windows (WIA) 2,0 associé au profil est le \_ chargeur de catégorie WIA ou WIA de la catégorie WIA \_ \_ \_ . Si la catégorie est WIA \_ de catégorie à \_ plat ou WIA \_ \_ , les propriétés suivantes doivent être valides pour l’élément, si les propriétés sont contenues dans le profil :

\_luminosité des adresses IP WIA \_

\_contraste des adresses IP WIA \_

type de données WIA de la \_ Loi WIA \_

\_XRES IPS \_ WIA

FORMAT WIA de la \_ Loi WIA \_

En outre, si la catégorie est WIA \_ (alimentation de catégorie WIA \_ ), la \_ propriété de taille de page IPS WIA \_ \_ doit être valide, si elle est présente dans le profil. Pour plus d’informations sur ces propriétés, consultez [**constantes de propriété d’élément de scanneur WIA**](-wia-wiaitempropscanneritem.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| MIDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Analyser le schéma de profil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




