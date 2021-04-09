---
title: IVMHardDisk SizeOnHost, propriété (VPCCOMInterfaces. h)
description: Taille du fichier de disque dur virtuel sur l’ordinateur hôte.
ms.assetid: f787ec4b-7b4f-4d35-b07c-4844424d91cf
keywords:
- SizeOnHost propriété Virtual PC
- SizeOnHost, propriété Virtual PC, IVMHardDisk, interface
- IVMHardDisk interface Virtual PC, propriété SizeOnHost
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeOnHost
- IVMHardDisk.get_SizeOnHost
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a000a70e1713b28f8fb8eea3590a53fb46ff0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033071"
---
# <a name="ivmharddisksizeonhost-property"></a>IVMHardDisk :: SizeOnHost, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère la taille du fichier de disque dur virtuel sur l’ordinateur hôte.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SizeOnHost(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a>Valeur de la propriété

Taille, en octets, du fichier image de disque dur. Cette valeur est une **variante** de type **VT \_ Decimal**.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                               | Signification                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>           |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre a la **valeur null**.<br/>              |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>       |
| <dl> Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt> </dl> | Le fichier image de disque dur est introuvable.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

