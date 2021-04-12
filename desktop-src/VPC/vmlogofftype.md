---
title: Énumération VMLogoffType (VPCCOMInterfaces. h)
description: Indique comment arrêter un ordinateur virtuel.
ms.assetid: 3a2965e3-2637-4677-b487-98d2b508672c
keywords:
- Virtual PC de l’énumération VMLogoffType
topic_type:
- apiref
api_name:
- VMLogoffType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2311736115390d807058bbfc54c24e7f9e9654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032816"
---
# <a name="vmlogofftype-enumeration"></a>Énumération VMLogoffType

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Indique comment arrêter un ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  vmLogoff_Normal    = 0,
  vmLogoff_Forced    = 1,
  vmLogoff_External  = 2
} VMLogoffType;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff \_ normal**
</dt> <dd>

La fermeture de session dans la machine virtuelle invitée était normale.

</dd> <dt>

<span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff \_ forcé**
</dt> <dd>

La fermeture de session de la machine virtuelle invitée a été forcée.

</dd> <dt>

<span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff \_ externe**
</dt> <dd>

La déconnexion de la machine virtuelle invitée a été effectuée à l’aide de la méthode [**IVMGuestOS :: Logoff**](ivmguestos-logoff.md) .

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

[**IVMVirtualMachine::ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

