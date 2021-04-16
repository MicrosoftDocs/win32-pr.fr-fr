---
description: Spécifie si l’appelant doit allouer les textures utilisées pour la sortie.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: Attribut MF_XVP_CALLER_ALLOCATES_OUTPUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527394"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a>L' \_ appelant MF XVP \_ \_ alloue l' \_ attribut de sortie

Spécifie si l’appelant doit allouer les textures utilisées pour la sortie.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Si cet attribut a la **valeur true**, le processeur vidéo s’attend à ce que la texture de sortie soit allouée par l’appelant, même en mode d’accélération vidéo DirectX (DXVA). Si cet attribut a la **valeur false**, le processeur vidéo alloue les textures de sortie en mode DXVA, et échoue si l’appelant a fourni des textures de sortie.

Pour définir cet attribut :

1.  Appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sur le processeur vidéo.
2.  Appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Définissez l’attribut avant le début de la diffusion en continu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




