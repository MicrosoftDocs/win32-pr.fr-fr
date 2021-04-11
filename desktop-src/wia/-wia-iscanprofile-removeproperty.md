---
description: Supprime une liste spécifiée de propriétés enfants dans le <Properties> élément d’un profil de numérisation.
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'IScanProfile :: RemoveProperty, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113910"
---
# <a name="iscanprofileremoveproperty-method"></a>IScanProfile :: RemoveProperty, méthode

Supprime une liste spécifiée de propriétés enfants dans l' `<Properties>` élément d’un profil de numérisation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nombre* \[ dans\]
</dt> <dd>

Type : **ULong**

Nombre d’entrées dans le tableau sur lequel *PID* pointe.

</dd> <dt>

*PID* \[ dans\]
</dt> <dd>

Type : **propid \** _

Pointeur vers un tableau de numéros d’identification des propriétés à supprimer. Chaque est une [constante de propriété WIA](-wia-wia-property-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Chaque valeur du tableau que *PID* pointe vers est l’une des [constantes de propriété WIA](-wia-wia-property-constants.md). Vous pouvez étendre ce système d’identification. Consultez [définition des propriétés personnalisées](-wia-defining-custom-properties.md).

Les modifications apportées à un profil ne sont pas enregistrées sur le disque tant que l’application n’a pas appelé la méthode [**IScanProfile :: Save**](-wia-iscanprofile-save.md) .

Si deux applications créent des objets de profil d’analyse à partir du même fichier XML, et que chaque application écrit des modifications dans son objet, seules les modifications apportées par l’application qui appelle [**IScanProfile :: Save**](-wia-iscanprofile-save.md) Last sont enregistrées sur le disque.

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

 

 




