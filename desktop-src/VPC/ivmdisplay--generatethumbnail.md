---
title: IVMDisplay _GenerateThumbnail, méthode (VPCCOMInterfaces. h)
description: Récupère un tableau de pixels représentant une image miniature de l’écran de l’ordinateur virtuel. | IVMDisplay _GenerateThumbnail, méthode (VPCCOMInterfaces. h)
ms.assetid: c97bb0ff-55cd-491f-a706-0ba15c9a6b54
keywords:
- Méthode _GenerateThumbnail Virtual PC
- _GenerateThumbnail méthode Virtual PC, interface IVMDisplay
- IVMDisplay interface Virtual PC, méthode _GenerateThumbnail
topic_type:
- apiref
api_name:
- IVMDisplay._GenerateThumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4084549de96330761bca4f4ec6da65ca150c96e5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106539834"
---
# <a name="ivmdisplay_generatethumbnail-method"></a>IVMDisplay :: \_ GenerateThumbnail, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère un tableau de pixels représentant une image miniature de l’écran de l’ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT _GenerateThumbnail(
  [out] unsigned long thumbnailImage[3072]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*thumbnailimage* \[ à\]
</dt> <dd>

Tableau de pixels représentant une image miniature de l’écran de la machine virtuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                 | Description                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>        |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



 

## <a name="remarks"></a>Notes

Cette interface retourne plus efficacement la miniature que la propriété [**thumbnail**](ivmdisplay-thumbnail.md) , mais elle n’est pas utilisable à partir de scripts de clients. La miniature est toujours de 64 pixels de large de 48 pixels de haut. Chaque pixel est 32 bits, où les 8 bits de poids fort représentent la valeur bleue du pixel, les 8 bits suivants représentent la valeur verte du pixel, et les 8 bits suivants représentent la valeur rouge du pixel. Les 64 premiers éléments du tableau sont la première ligne de la miniature, les 64 suivants sont la deuxième ligne, et ainsi de suite. Cette méthode retourne un tableau statique de pixels, qui est plus efficace que le retour d’un **SAFEARRAY** de valeurs **Variant** , mais n’est pas compatible avec les clients de script.

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

 

