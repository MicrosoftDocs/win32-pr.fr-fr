---
title: Méthode IVMDVDDrive SetBusLocation (VPCCOMInterfaces. h)
description: Attache le lecteur de DVD à l’emplacement de bus spécifié sur l’ordinateur virtuel.
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- Méthode SetBusLocation Virtual PC
- Méthode SetBusLocation Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, méthode SetBusLocation
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 593a42c21d1ed688185a7fe7123e972998859c010775a2cf4efd5f3bbbbaa98f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595842"
---
# <a name="ivmdvddrivesetbuslocation-method"></a>IVMDVDDrive :: SetBusLocation, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Attache le lecteur de DVD à l’emplacement de bus spécifié sur l’ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*busNumber* \[ dans\]
</dt> <dd>

Numéro de bus auquel ce lecteur doit être attaché. Par exemple, sur un bus IDE, ce nombre indique s’il faut utiliser le numéro de bus principal ou secondaire.

</dd> <dt>

*deviceNumber* \[ dans\]
</dt> <dd>

Numéro de l’appareil auquel ce lecteur doit être attaché. Par exemple, sur un bus IDE, ce nombre indique s’il faut utiliser l’emplacement de l’appareil principal ou secondaire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                            | Description                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | L'opération a réussi.<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                 | L’emplacement de bus spécifié n’est pas valide.<br/>                                                                                     |
| <dl> <dt>**E \_ ÉCHEC**</dt> <dt>0x80004005</dt> </dl>                       | Une erreur inattendue s’est produite.<br/>                                                                                            |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt> </dl> | Impossible de définir l’emplacement du bus pendant que l’ordinateur virtuel est en cours d’exécution ou dans un état enregistré.<br/>                                     |
| <dl> <dt>**machine \_ virtuelle \_ E \_ bus \_ en cours d' \_ utilisation**</dt> </dl>                                                                      | Un autre périphérique est déjà attaché à l’emplacement de bus spécifié.<br/>                                                            |
| <dl> <dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt> </dl>         | Impossible d’initialiser le lecteur actif.<br/>                                                                                  |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>            | Les modifications n’ont pas pu être écrites dans le fichier de préférences, car l’ordinateur virtuel pour ce lecteur n’a pas pu être déterminé.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>            | Une erreur inattendue s’est produite.<br/>                                                                                            |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

