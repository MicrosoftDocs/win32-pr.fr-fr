---
title: IVMHardDisk SizeInGuest, propriété (VPCCOMInterfaces. h)
description: Récupère la taille du disque dur virtuel dans le système d’exploitation invité.
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- SizeInGuest propriété Virtual PC
- SizeInGuest, propriété Virtual PC, IVMHardDisk, interface
- IVMHardDisk interface Virtual PC, propriété SizeInGuest
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeInGuest
- IVMHardDisk.get_SizeInGuest
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8efbdcf9f5aa60a8dfdce9c71de745e0567995b90df13ffd39b5969689de099c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653289"
---
# <a name="ivmharddisksizeinguest-property"></a>IVMHardDisk :: SizeInGuest, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère la taille du disque dur virtuel dans le système d’exploitation invité.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a>Valeur de la propriété

Taille, en octets, de l’image de disque dur. Cette valeur est une **variante** de type VT \_ Decimal.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                               | Signification                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                  |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre a la **valeur null**.<br/>                                                     |
| <dl> Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt> </dl> | Le fichier de disque dur virtuel actuel est introuvable.<br/>                         |
| <dl> <dt>Ordinateur virtuel \_ \_Échec d' \_ \_ ouverture \_ d’une image HD E</dt> <dt>0xA004067C</dt> </dl>                  | Une erreur s’est produite lors de la tentative d’ouverture du fichier image de disque dur actuel.<br/>   |
| <dl> <dt>Ordinateur virtuel \_ 0xA0040681 \_ d' \_ \_ accès à l’image HD</dt> <dt></dt> </dl>                      | Une erreur s’est produite lors de la tentative d’accès au fichier image du disque dur actuel.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                              |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

