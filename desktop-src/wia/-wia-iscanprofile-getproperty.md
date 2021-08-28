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
ms.openlocfilehash: ef09115c7131df21697540fa941f8bd863650bc029601088b4a0f8c80e9b1a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814079"
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

Type : **propid \***

Pointeur vers un tableau des numéros d’identification des propriétés à définir. Chaque valeur du tableau est une [constante de propriété WIA](-wia-wia-property-constants.md).

</dd> <dt>

*pvar* \[ à\]
</dt> <dd>

Type : **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\***

Pointeur vers un tableau de valeurs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Retourne \_ la valeur false si l’une des valeurs de propriété n’est pas disponible ; sinon, retourne s \_ OK ou un code d’erreur com standard.

## <a name="remarks"></a>Remarques

Le type de chaque valeur doit être du même type que celui qui a été défini avec l’appel à [**IScanProfile :: SetProperty**](-wia-iscanprofile-setproperty.md).

Chaque valeur du tableau que *PID* pointe vers est l’une des [constantes de propriété WIA](-wia-wia-property-constants.md). Vous pouvez étendre ce système d’identification. Consultez [définition des propriétés personnalisées](-wia-defining-custom-properties.md).

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

 

 
