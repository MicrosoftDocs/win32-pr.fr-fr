---
title: Propriété Width de IVMDisplay (VPCCOMInterfaces. h)
description: Largeur de l’affichage de la machine virtuelle, en pixels.
ms.assetid: a0062d75-dbb3-41ff-8112-87c1a31b088e
keywords:
- Propriété Width de Virtual PC
- Propriété de largeur Virtual PC, interface IVMDisplay
- IVMDisplay interface Virtual PC, propriété Width
topic_type:
- apiref
api_name:
- IVMDisplay.Width
- IVMDisplay.get_Width
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db106804f81f52b669b90920699761061d97fb3412dd58b761f7da1701ec53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654219"
---
# <a name="ivmdisplaywidth-property"></a>IVMDisplay :: Width, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère, en pixels, la largeur de l’affichage de la machine virtuelle (de la machine virtuelle).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Width(
  [out, retval] long *displayPixelWidth
);
```



## <a name="property-value"></a>Valeur de la propriété

Largeur, en pixels.

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
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay est défini en tant que 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

