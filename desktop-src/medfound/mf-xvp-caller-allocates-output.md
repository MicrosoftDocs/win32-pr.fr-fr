---
description: Spécifie si l’appelant doit allouer les textures utilisées pour la sortie.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: Attribut MF_XVP_CALLER_ALLOCATES_OUTPUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31da89bec9c9573d9d968077e51d413e1861bca28cb606667d402fab5a408f96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599969"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a>L' \_ appelant MF XVP \_ \_ alloue l' \_ attribut de sortie

Spécifie si l’appelant doit allouer les textures utilisées pour la sortie.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Remarques

Si cet attribut a la **valeur true**, le processeur vidéo s’attend à ce que la texture de sortie soit allouée par l’appelant, même en mode d’accélération vidéo DirectX (DXVA). Si cet attribut a la **valeur false**, le processeur vidéo alloue les textures de sortie en mode DXVA, et échoue si l’appelant a fourni des textures de sortie.

Pour définir cet attribut :

1.  Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le processeur vidéo.
2.  Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Définissez l’attribut avant le début de la diffusion en continu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




