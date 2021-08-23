---
title: IVMMouse ScrollWheelPosition, propriété (VPCCOMInterfaces. h)
description: Ajuste la coordonnée z de la souris (relative uniquement).
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- ScrollWheelPosition propriété Virtual PC
- ScrollWheelPosition, propriété Virtual PC, IVMMouse, interface
- IVMMouse interface Virtual PC, propriété ScrollWheelPosition
topic_type:
- apiref
api_name:
- IVMMouse.ScrollWheelPosition
- IVMMouse.put_ScrollWheelPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334190707cd43e63ce2244f410180b11bf6eb5018ff1482f073903adfb4b7878
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510649"
---
# <a name="ivmmousescrollwheelposition-property"></a>IVMMouse :: ScrollWheelPosition, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ajuste la coordonnée z de la souris (relative uniquement).

Cette propriété est en écriture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a>Valeur de la propriété

Coordonnée z qui indique le nombre de pixels que la souris doit déplacer le long de l’axe z.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                     | Signification                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                        | L'opération a réussi.<br/>                                                                |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt> </dl>             | L’ordinateur virtuel auquel ce périphérique de souris est attaché n’est pas en cours d’exécution.<br/>         |
| <dl> <dt>Ordinateur virtuel \_ E \_ souris \_ non \_ active</dt> <dt>0xA0040800</dt> </dl>           | Le périphérique de la souris n’a pas été mis sous tension ou n’est pas actuellement actif sur la machine virtuelle.<br/> |
| <dl> <dt>Ordinateur virtuel \_ E \_ utilisant \_ des \_ coordonnées absolues</dt> <dt>0xA0040801</dt> </dl> | La position de la roulette de défilement ne peut pas être définie lorsque le périphérique de la souris utilise des coordonnées absolues.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                  | Une erreur inattendue s’est produite.<br/>                                                            |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse est défini en tant que ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

