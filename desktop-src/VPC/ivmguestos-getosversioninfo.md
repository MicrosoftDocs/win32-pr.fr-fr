---
title: Méthode IVMGuestOS GetOsVersionInfo (VPCCOMInterfaces. h)
description: Récupère des informations de version pour le système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- Méthode GetOsVersionInfo Virtual PC
- Méthode GetOsVersionInfo Virtual PC, interface IVMGuestOS
- IVMGuestOS interface Virtual PC, méthode GetOsVersionInfo
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef39259b429d096246bbdbe5cb23e6021f498b2d9d47cd14fb12409eca814c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653469"
---
# <a name="ivmguestosgetosversioninfo-method"></a>IVMGuestOS :: GetOsVersionInfo, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère des informations de version pour le système d’exploitation invité en cours d’exécution sur la machine virtuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*guestOsVersionInfo* \[ out, retval\]
</dt> <dd>

Pointeur vers une structure [**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                       | Description                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                             | L'opération a réussi.<br/>                                  |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                               | Le paramètre a la **valeur null**.<br/>                                     |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt> </dl> | La mémoire disponible est insuffisante pour effectuer cette requête.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                       | Une erreur inattendue s’est produite.<br/>                              |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt> </dl>                  | La machine virtuelle n’est pas en cours d’exécution.<br/>                                         |
| <dl> <dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt> </dl>    | Les composants d’intégration ne sont pas installés sur cette machine virtuelle.<br/>           |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

