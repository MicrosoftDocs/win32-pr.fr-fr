---
title: Énumération VMMouseButton (VPCCOMInterfaces. h)
description: Spécifie le bouton de la souris.
ms.assetid: d09e63cb-9dc5-424f-b130-c0b0dd07fe11
keywords:
- Virtual PC de l’énumération VMMouseButton
topic_type:
- apiref
api_name:
- VMMouseButton
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18744af5a4f8068b9bb371cb15e06c365561f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466370"
---
# <a name="vmmousebutton-enumeration"></a>Énumération VMMouseButton

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Spécifie le bouton de la souris.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  vmMouseButton_Left    = 1,
  vmMouseButton_Right   = 2,
  vmMouseButton_Center  = 3
} VMMouseButton;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton \_ gauche**
</dt> <dd>

Bouton gauche de la souris.

</dd> <dt>

<span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton \_ droit**
</dt> <dd>

Bouton droit de la souris.

</dd> <dt>

<span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**\_Centre vmMouseButton**
</dt> <dd>

Bouton central de la souris.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

