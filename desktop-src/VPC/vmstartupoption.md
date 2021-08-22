---
title: Énumération VMStartupOption (VPCCOMInterfaces. h)
description: Spécifie l’option de démarrage.
ms.assetid: ac4de9a7-7fc7-4361-89dd-e7da8f5dbb92
keywords:
- Virtual PC de l’énumération VMStartupOption
topic_type:
- apiref
api_name:
- VMStartupOption
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f9799f4eb797c76be9c37b458551f99e0067977f42422c4b4181cee66c92527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998459"
---
# <a name="vmstartupoption-enumeration"></a>Énumération VMStartupOption

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Spécifie l’option de démarrage.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  vmStartupOption_Normal                      = 0,
  vmStartupOption_FixParentTimestampMismatch  = 1
} VMStartupOption;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmStartupOption \_ normal**
</dt> <dd>

Démarrez normalement.

</dd> <dt>

<span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**vmStartupOption \_ FixParentTimestampMismatch**
</dt> <dd>

Corrigez l’incompatibilité d’horodatage parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine :: Startup2**](ivmvirtualmachine-startup2.md)
</dt> </dl>

 

