---
title: IVMDisplay VideoMode, propriété (VPCCOMInterfaces. h)
description: Récupère le mode vidéo actuel.
ms.assetid: e5a090c2-f7e6-4b85-8729-64d2ff68fcf3
keywords:
- VideoMode propriété Virtual PC
- VideoMode, propriété Virtual PC, IVMDisplay, interface
- IVMDisplay interface Virtual PC, propriété VideoMode
topic_type:
- apiref
api_name:
- IVMDisplay.VideoMode
- IVMDisplay.get_VideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0164a658766cb8973a7c1ac403756ee888abab1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942081"
---
# <a name="ivmdisplayvideomode-property"></a>IVMDisplay :: VideoMode, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère le mode vidéo actuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_VideoMode(
  [out, retval] VMDisplayVideoMode *videoMode
);
```



## <a name="property-value"></a>Valeur de la propriété

Mode vidéo actuel du système d’exploitation invité. Pour obtenir la liste des valeurs, consultez [**VMDisplayVideoMode**](vmdisplayvideomode.md).

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                         | Signification                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | L'opération a réussi.<br/>                                 |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>              | Le paramètre a la **valeur null**.<br/>                                    |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt> </dl> | L’ordinateur virtuel doit être en cours d’exécution pour cette opération.<br/>       |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>      | L’ordinateur virtuel n’est pas valide ou n’est pas en cours d’exécution.<br/> |
| <dl> <dt>Ordinateur virtuel \_ E \_ aucun \_ </dt> <dt>0xA0040850</dt> d’affichage </dl>      | Impossible de trouver un affichage valide pour la machine virtuelle.<br/>     |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>      | Une erreur inattendue s’est produite.<br/>                             |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay est défini en tant que 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

