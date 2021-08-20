---
title: Méthode IVMVirtualPCEvents OnEventLogged (VPCCOMInterfaces. h)
description: reçoit une notification indiquant que Windows Virtual PC enregistre un événement.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- Méthode OnEventLogged Virtual PC
- Méthode OnEventLogged Virtual PC, interface IVMVirtualPCEvents
- IVMVirtualPCEvents interface Virtual PC, méthode OnEventLogged
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4994f37cd0e6f83162171fbbdacbf2247a8d472cd49b5750aa2d1b735e4b554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998519"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a>IVMVirtualPCEvents :: OnEventLogged, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

reçoit une notification indiquant que Windows Virtual PC enregistre un événement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*logMessageID* \[ dans\]
</dt> <dd>

Identificateur du message du journal des événements qui a été enregistré.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

cette méthode est appelée quand Windows Virtual PC enregistre un message dans le journal des événements Windows. Le programme client doit implémenter cette méthode d’interface pour recevoir la notification de l’événement **vmVirtualPCEvent \_ EventLogged** provenant de [**IVMVirtualPC**](ivmvirtualpc.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualPCEvents est défini comme efed1ef1-3c09-41f7-a9c2-7e29fa286c9d<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualPCEvents**](ivmvirtualpcevents.md)
</dt> </dl>

 

