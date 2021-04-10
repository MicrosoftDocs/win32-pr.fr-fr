---
title: Interface IVMDisplay (VPCCOMInterfaces. h)
description: Contrôle les paramètres d’affichage d’un ordinateur virtuel. L’interface IVMDisplay pour un ordinateur virtuel peut être récupérée à l’aide de la propriété d’affichage IVMVirtualMachine.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- Virtual PC de l’interface IVMDisplay
- IVMDisplay interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMDisplay
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0f410e49682d2fa9f5f8511d96e3b9ce9a1094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942507"
---
# <a name="ivmdisplay-interface"></a>Interface IVMDisplay

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Contrôle les paramètres d’affichage d’un ordinateur virtuel. L’interface **IVMDisplay** pour un ordinateur virtuel peut être récupérée à l’aide de la propriété [**IVMVirtualMachine ::D**](ivmvirtualmachine-display.md) .

## <a name="members"></a>Membres

L’interface **IVMDisplay** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMDisplay** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMDisplay** possède ces méthodes.



| Méthode                                                       | Description                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) | Récupère un tableau de pixels représentant une image miniature de l’écran de l’ordinateur virtuel.<br/> |
| [**SetDimensions**](ivmdisplay-setdimensions.md)            | Définit, en pixels, la hauteur et la largeur de l’affichage de l’ordinateur virtuel.<br/>                       |



 

### <a name="properties"></a>Propriétés

L’interface **IVMDisplay** possède les propriétés suivantes.



| Propriété                                             | Type d’accès          | Description                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**CanResize**](ivmdisplay-canresize.md)<br/> | Lecture seule<br/> | Indique si l’invité autorise les modifications de résolution.<br/>                             |
| [**Height**](ivmdisplay-height.md)<br/>       | Lecture seule<br/> | Hauteur de l’affichage de l’ordinateur virtuel, en pixels.<br/>                            |
| [**Thumbnail**](ivmdisplay-thumbnail.md)<br/> | Lecture seule<br/> | Tableau de pixels représentant une image miniature de l’écran de la machine virtuelle.<br/> |
| [**VideoMode**](ivmdisplay-videomode.md)<br/> | Lecture seule<br/> | Mode vidéo actuel (texte, VGA, SVGA, etc.).<br/>                               |
| [**Width**](ivmdisplay-width.md)<br/>         | Lecture seule<br/> | Largeur de l’affichage de l’ordinateur virtuel, en pixels.<br/>                             |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay est défini en tant que 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



 

