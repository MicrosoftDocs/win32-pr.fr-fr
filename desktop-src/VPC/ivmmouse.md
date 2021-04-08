---
title: Interface IVMMouse (VPCCOMInterfaces. h)
description: Contrôle le périphérique de la souris au sein d’une machine virtuelle.
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- Virtual PC de l’interface IVMMouse
- IVMMouse interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMMouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7041b8a28b924ffedc8ff23edd2b04afdaa78be2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844149"
---
# <a name="ivmmouse-interface"></a>Interface IVMMouse

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Contrôle l’appareil de la souris au sein d’une machine virtuelle. La **IVMMouse** d’un ordinateur virtuel peut être récupérée à l’aide de la propriété [**IVMVirtualMachine :: Mouse**](ivmvirtualmachine-mouse.md) . Les coordonnées du périphérique de la souris peuvent être représentées soit en coordonnées absolues, soit en coordonnées Delta. Utilisez la propriété [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) pour faire la distinction entre les deux méthodes de représentation de coordonnées. Notez que la récupération de la position actuelle du curseur et l’utilisation de coordonnées absolues sont prises en charge uniquement si les composants d’intégration sont installés sur le système d’exploitation invité.

## <a name="members"></a>Membres

L’interface **IVMMouse** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMMouse** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMMouse** possède ces méthodes.



| Méthode                                  | Description                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [**Cliquez sur**](ivmmouse-click.md)         | Simule un clic sur le bouton de la souris.<br/>                                         |
| [**GetButton**](ivmmouse-getbutton.md) | Récupère l’état actuel (vers le haut ou vers le haut) du bouton spécifié de la souris.<br/> |
| [**SetButton**](ivmmouse-setbutton.md) | Définit l’état actuel (vers le haut ou vers le haut) du bouton spécifié de la souris.<br/>      |



 

### <a name="properties"></a>Propriétés

L’interface **IVMMouse** possède les propriétés suivantes.



| Propriété                                                                         | Type d’accès           | Description                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [**HorizontalPosition**](ivmmouse-horizontalposition.md)<br/>             | Lecture/écriture<br/> | Coordonnée x absolue de la souris.<br/>                                         |
| [**ScrollWheelPosition**](ivmmouse-scrollwheelposition.md)<br/>           | Écriture seule<br/> | Coordonnée z de la souris (relative uniquement).<br/>                                  |
| [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md)<br/> | Lecture/écriture<br/> | Indique si les coordonnées de la souris représentent des coordonnées absolues ou relatives.<br/> |
| [**VerticalPosition**](ivmmouse-verticalposition.md)<br/>                 | Lecture/écriture<br/> | Coordonnée y absolue de la souris.<br/>                                         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse est défini en tant que ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



 

