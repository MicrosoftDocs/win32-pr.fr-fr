---
title: Méthode IVMDVDDrive AttachHostDrive (VPCCOMInterfaces. h)
description: Attache un lecteur hôte au lecteur de DVD de l’ordinateur virtuel.
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- Méthode AttachHostDrive Virtual PC
- Méthode AttachHostDrive Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, méthode AttachHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c82229488ebb705cab1a684a207f973356d2d43177c4123ae4f456b55fbe6840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136852"
---
# <a name="ivmdvddriveattachhostdrive-method"></a>IVMDVDDrive :: AttachHostDrive, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Attache un lecteur hôte au lecteur de DVD de l’ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

lettre de *lecteur* \[ dans\]
</dt> <dd>

Lettre du lecteur hôte à attacher.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                    | Description                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                          | L'opération a réussi.<br/>                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>         | Aucune lettre de lecteur n’a été spécifiée, ou la lettre de lecteur spécifiée n’est pas valide.<br/>                                                                                                  |
| <dl> <dt>**E \_ ÉCHEC**</dt> <dt>0x80004005</dt> </dl>               | Une erreur inattendue s’est produite.<br/>                                                                                                                                         |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>    | L’ordinateur virtuel est introuvable.<br/>                                                                                                                                   |
| <dl> <dt>**Ordinateur virtuel \_ \_Lecteur E \_ en cours d' \_ utilisation**</dt> <dt>0xA0040727</dt> </dl> | Un lecteur DVD hôte ou une image ISO est déjà attaché à ce lecteur au sein de la machine virtuelle, ou le lecteur hôte spécifié est déjà utilisé dans un autre ordinateur virtuel.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt> </dl> | L’emplacement du bus pour ce lecteur n’est pas valide, ou le lecteur ne semble pas être un lecteur de DVD valide.<br/>                                                                         |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>    | Une erreur inattendue s’est produite.<br/>                                                                                                                                         |



 

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

 

