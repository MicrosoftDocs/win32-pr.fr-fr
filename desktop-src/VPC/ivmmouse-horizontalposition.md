---
title: IVMMouse, propriété HorizontalPosition (VPCCOMInterfaces. h)
description: Coordonnée x absolue de la souris.
ms.assetid: 8cf2a247-b6db-49f6-8e19-c862004f26cd
keywords:
- Propriété HorizontalPosition Virtual PC
- Propriété HorizontalPosition Virtual PC, IVMMouse, interface
- IVMMouse interface Virtual PC, propriété HorizontalPosition
topic_type:
- apiref
api_name:
- IVMMouse.HorizontalPosition
- IVMMouse.get_HorizontalPosition
- IVMMouse.put_HorizontalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2cb3fde1caff23845c653024d9c5e2859b0b7b5df8502dbaea167d3e969a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007149"
---
# <a name="ivmmousehorizontalposition-property"></a>IVMMouse :: HorizontalPosition, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère la coordonnée x absolue de la souris.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_HorizontalPosition(
  [in]          long position
);

HRESULT get_HorizontalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a>Valeur de la propriété

Coordonnée x indiquant la nouvelle position de la souris. Lorsque vous utilisez des coordonnées absolues, cette valeur spécifie la nouvelle coordonnée x de la souris. Lorsque vous utilisez des coordonnées relatives, cette valeur spécifie le nombre de pixels que la souris doit déplacer dans la direction x.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                       | Signification                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'opération a réussi.<br/>                                                                                                                |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                            | Le paramètre a la **valeur null**.<br/>                                                                                                                   |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt> </dl>               | L’ordinateur virtuel auquel ce périphérique de souris est attaché n’est pas en cours d’exécution.<br/>                                                         |
| <dl> <dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt> </dl> | Les composants d’intégration doivent être installés pour récupérer la position de la souris ou définir la position de la souris lors de l’utilisation de coordonnées absolues.<br/>       |
| <dl> <dt>Ordinateur virtuel \_ E \_ utilisant \_ des \_ coordonnées relatives</dt> <dt>0xA0040802</dt> </dl>   | Le périphérique souris est actuellement configuré pour utiliser des coordonnées de souris relatives.<br/>                                                                         |
| <dl> <dt>Ordinateur virtuel \_ E \_ souris \_ non \_ active</dt> <dt>0xA0040800</dt> </dl>             | Les coordonnées absolues ne peuvent pas être récupérées si le périphérique de la souris n’est pas sous tension ou s’il n’est pas actuellement actif sur l’ordinateur virtuel.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                    | Une erreur inattendue s’est produite.<br/>                                                                                                            |



## <a name="remarks"></a>Remarques

Impossible de récupérer cette propriété lors de l’utilisation de coordonnées relatives.

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

 

