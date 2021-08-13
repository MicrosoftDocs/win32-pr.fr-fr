---
title: IVMDisplay, propriété de la miniature (VPCCOMInterfaces. h)
description: Récupère un tableau de pixels représentant une image miniature de l’écran de l’ordinateur virtuel. | IVMDisplay, propriété de la miniature (VPCCOMInterfaces. h)
ms.assetid: e7b57f16-eec1-4461-acfb-742976eff14a
keywords:
- Propriété de miniature Virtual PC
- Propriété de miniature Virtual PC, interface IVMDisplay
- IVMDisplay interface Virtual PC, propriété thumbnail
topic_type:
- apiref
api_name:
- IVMDisplay.Thumbnail
- IVMDisplay.get_Thumbnail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a558a551972bb76558dcd60223d8ddc29783aeaa23e6dbe9263f34642c1c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473329"
---
# <a name="ivmdisplaythumbnail-property"></a>IVMDisplay :: Thumbnail, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère un tableau de pixels représentant une image miniature de l’écran de l’ordinateur virtuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Thumbnail(
  [out, retval] VARIANT *thumbnailImage
);
```



## <a name="property-value"></a>Valeur de la propriété

Variante de type VT de \_ tableau \| VT \_ contenant des entrées de type VT \_ UI4, une pour chaque pixel de la miniature.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>        |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



## <a name="remarks"></a>Remarques

Cette interface retourne la miniature moins efficacement que la méthode [**\_ GenerateThumbnail**](ivmdisplay--generatethumbnail.md) , mais elle est utilisable à partir des clients de script. La miniature est toujours de 64 pixels de large de 48 pixels de haut. Chaque pixel est 32 bits. Les 64 premiers éléments du tableau sont la première ligne de pixels de la miniature, les 64 suivants étant la deuxième ligne, et ainsi de suite.

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

 

