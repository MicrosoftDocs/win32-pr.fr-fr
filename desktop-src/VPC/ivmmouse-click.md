---
title: IVMMouse Click, méthode (VPCCOMInterfaces. h)
description: Simule un clic sur le bouton de la souris.
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- Cliquez sur méthode Virtual PC
- Cliquez sur méthode Virtual PC, interface IVMMouse
- IVMMouse interface Virtual PC, méthode click
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ea1b861db0a92ad92e689770182d225778aee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466830"
---
# <a name="ivmmouseclick-method"></a>IVMMouse :: Click, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simule un clic sur le bouton de la souris.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*buttonIndex* \[ dans\]
</dt> <dd>

Index du bouton sur lequel un clic a été effectué. Pour obtenir la liste des valeurs, consultez [**VMMouseButton**](vmmousebutton.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                        | Description                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                              | L'opération a réussi.<br/>                                                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>             | Le paramètre a la **valeur null**.<br/>                                                                                                             |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt> </dl>   | L’ordinateur virtuel auquel ce périphérique de souris est attaché n’est pas en cours d’exécution.<br/>                                                   |
| <dl> <dt>**Ordinateur virtuel \_ E \_ souris \_ non \_ active**</dt> <dt>0xA0040800</dt> </dl> | L’opération n’a pas pu aboutir car le périphérique de la souris n’est pas sous tension ou n’est pas actuellement actif sur la machine virtuelle.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>        | Une erreur inattendue s’est produite.<br/>                                                                                                      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse est défini en tant que ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

