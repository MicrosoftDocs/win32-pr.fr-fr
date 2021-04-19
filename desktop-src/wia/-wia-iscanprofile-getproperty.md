---
description: Obtient la valeur des propriétés enfants spécifiées dans le <Properties> élément d’un profil de numérisation.
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: 'IScanProfile :: GetProperty, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 48137e61d88d580ac556220b4e47b949d9e2c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524911"
---
# <a name="iscanprofilegetproperty-method"></a>IScanProfile :: GetProperty, méthode

Obtient la valeur des propriétés enfants spécifiées dans l' `<Properties>` élément d’un profil de numérisation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
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

Type : **propid \** _

Pointeur vers un tableau des numéros d’identification des propriétés à définir. Chaque valeur du tableau est une [constante de propriété WIA](-wia-wia-property-constants.md).

</dd> <dt>

_pvar * \[ out\]
</dt> <dd>

Tapez : **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _

Pointeur vers un tableau de valeurs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Retourne \_ la valeur false si l’une des valeurs de propriété n’est pas disponible ; sinon, retourne s \_ OK ou un code d’erreur com standard.

## <a name="remarks"></a>Notes

Le type de chaque valeur doit être du même type que celui qui a été défini avec l’appel à [**IScanProfile :: SetProperty**](-wia-iscanprofile-setproperty.md).

Chaque valeur du tableau que *PID* pointe vers est l’une des [constantes de propriété WIA](-wia-wia-property-constants.md). Vous pouvez étendre ce système d’identification. Consultez [définition des propriétés personnalisées](-wia-defining-custom-properties.md).

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

**Méthodologique**
</dt> <dt>

[Analyser le schéma de profil](-wia-scan-profile-schema.md)
</dt> <dt>

[Constantes de propriété WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Définition des propriétés personnalisées](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
