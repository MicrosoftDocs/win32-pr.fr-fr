---
description: Spécifie le type de bus d’e/s utilisé par la carte graphique.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: Énumération D3DBUSTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBUSTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cece215946406bedcca2cbfdd2b64bfdb5df00208b2d84cf2aa90fdb89b516bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828379"
---
# <a name="d3dbustype-enumeration"></a>Énumération D3DBUSTYPE

Spécifie le type de bus d’e/s utilisé par la carte graphique.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  D3DBUSTYPE_OTHER                                             = 0x00000000,
  D3DBUSTYPE_PCI                                               = 0x00000001,
  D3DBUSTYPE_PCIX                                              = 0x00000002,
  D3DBUSTYPE_PCIEXPRESS                                        = 0x00000003,
  D3DBUSTYPE_AGP                                               = 0x00000004,
  D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET                        = 0x00010000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP           = 0x00020000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET         = 0x00030000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR                 = 0x00040000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE  = 0x00050000,
  D3DBUSIMPL_MODIFIER_NON_STANDARD                             = 0x80000000
} D3DBUSTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ autre**
</dt> <dd>

Indique un type de bus autre que les types répertoriés ici.

</dd> <dt>

<span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE \_ PCI**
</dt> <dd>

Bus PCI.

</dd> <dt>

<span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ PCIx**
</dt> <dd>

Bus PCI-X.

</dd> <dt>

<span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ PCIEXPRESS**
</dt> <dd>

Bus PCI Express.

</dd> <dt>

<span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**
</dt> <dd>

Bus AGP (Accelerated Graphics Port).

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**\_Modificateur D3DBUSIMPL \_ à l’intérieur \_ du \_ Chipset**
</dt> <dd>

L’implémentation de la carte graphique se trouve dans le pont nord d’un chipset de carte mère. Cet indicateur implique que les données ne sont jamais placées sur un bus d’expansion (comme PCI ou AGP) lorsqu’elles sont transférées de la mémoire principale vers la carte graphique.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**\_Le modificateur D3DBUSIMPL \_ effectue \_ le suivi de la \_ carte mère \_ \_ \_ sur la puce**
</dt> <dd>

Indique que la carte graphique est connectée au pont nord d’un chipset de carte mère par des pistes sur la carte mère et que toutes les puces de la carte graphique sont soudées à la carte mère. Cet indicateur implique que les données ne sont jamais placées sur un bus d’expansion (comme PCI ou AGP) lorsqu’elles sont transférées de la mémoire principale vers la carte graphique.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**\_Le modificateur D3DBUSIMPL \_ effectue \_ le suivi de la \_ \_ carte mère \_ au \_ Socket**
</dt> <dd>

La carte graphique est connectée au pont nord d’un chipset de carte mère par des pistes sur la carte mère, et toutes les puces de la carte graphique sont connectées via des sockets à la carte mère.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**\_ \_ Connecteur de carte fille de MODIFICATeur D3DBUSIMPL \_ \_**
</dt> <dd>

La carte graphique est connectée à la carte mère via un connecteur en fille.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**\_ \_ \_ Connecteur de carte fille de modificateur D3DBUSIMPL \_ \_ dans \_ \_ NUAE**
</dt> <dd>

La carte graphique est connectée à la carte mère via un connecteur à fille et la carte graphique est à l’intérieur d’un boîtier qui n’est pas accessible par l’utilisateur.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**\_Modificateur D3DBUSIMPL \_ non \_ standard**
</dt> <dd>

L’un des indicateurs modificateur de \_ modificateur D3DBUSIMPL \_ \_ xxx est défini.

</dd> </dl>

## <a name="remarks"></a>Remarques

Jusqu’à trois indicateurs peuvent être définis. Les indicateurs dans la plage 0x00 à 0x04 (**D3DBUSTYPE \_ xxx**) fournissent le type de bus de base. Les indicateurs dans la plage 0x10000 à 0x50000 **( \_ modificateur D3DBUSIMPL \_ xxx**) modifient la description de base. Le pilote définit un indicateur de type bus et peut définir zéro ou un indicateur de modificateur. Si le pilote définit un indicateur de modificateur, il définit également l’indicateur **D3DBUSIMPL \_ modificateur \_ non \_ standard** . Les indicateurs sont combinés avec une **opération or** au niveau du bit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>D3d9types. h (inclure d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations de vidéos Direct3D](direct3d-video-enumerations.md)
</dt> </dl>

 

 




