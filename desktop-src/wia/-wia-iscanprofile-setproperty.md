---
description: Définit la valeur des propriétés enfants spécifiées dans le <Properties> élément d’un profil de numérisation.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'IScanProfile :: SetProperty, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: ba4c7aff5139f1230179299d80065f1b933a6cf2d01d4ca03c045ccbe142c3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441425"
---
# <a name="iscanprofilesetproperty-method"></a>IScanProfile :: SetProperty, méthode

Définit la valeur des propriétés enfants spécifiées dans l' `<Properties>` élément d’un profil de numérisation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nombre* \[ dans\]
</dt> <dd>

Type : **ULong**

Nombre d’entrées dans les tableaux qui sont pointés par *PID* et *pvar*.

</dd> <dt>

*PID* \[ dans\]
</dt> <dd>

Type : **propid \***

Pointeur vers un tableau de numéros d’identification des propriétés à définir. Chaque valeur du tableau est une [constante de propriété WIA](-wia-wia-property-constants.md).

</dd> <dt>

*pvar* \[ dans\]
</dt> <dd>

Type : **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\***

Pointeur vers un tableau de valeurs à assigner aux propriétés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Chaque valeur du tableau que *PID* pointe vers est l’une des [constantes de propriété WIA](-wia-wia-property-constants.md). Vous pouvez étendre ce système d’identification. Consultez [définition des propriétés personnalisées](-wia-defining-custom-properties.md).

Les modifications apportées à un profil ne sont pas enregistrées sur le disque tant que l’application n’a pas appelé la méthode [**IScanProfile :: Save**](-wia-iscanprofile-save.md) .

Si deux applications créent des objets de profil d’analyse à partir du même fichier XML, et que chaque application écrit des modifications dans son objet, seules les modifications apportées par l’application qui appelle [**IScanProfile :: Save**](-wia-iscanprofile-save.md) Last sont enregistrées sur le disque.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| MIDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Analyser le schéma de profil](-wia-scan-profile-schema.md)
</dt> <dt>

[Constantes de propriété WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Définition des propriétés personnalisées](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
