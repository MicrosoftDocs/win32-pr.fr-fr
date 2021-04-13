---
title: IVMVirtualMachine ShutdownActionOnQuit, propriété (VPCCOMInterfaces. h)
description: Action à exécuter sur cet ordinateur virtuel s’il est en cours d’exécution lorsque Windows Virtual PC est fermé.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- ShutdownActionOnQuit propriété Virtual PC
- ShutdownActionOnQuit, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété ShutdownActionOnQuit
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01469e48e767777c6ea3daa4d0f3a923dce67726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466383"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a>IVMVirtualMachine :: ShutdownActionOnQuit, propriété

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère et définit l’action à effectuer sur cet ordinateur virtuel (VM) s’il est en cours d’exécution lorsque Windows Virtual PC est fermé.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]          VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out, retval] VMShutdownAction *shutdownAction
);
```



## <a name="property-value"></a>Valeur de la propriété

Indique comment arrêter cette machine virtuelle si elle est en cours d’exécution au moment de la fermeture de Windows Virtual PC. Pour obtenir la liste des valeurs, consultez [**VMShutdownAction**](vmshutdownaction.md).

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>                                       |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre est **null** ou n’est pas une valeur valide.<br/>                     |
| <dl> <dt>E \_ ACCESSDENIED</dt> <dt>0x80070005</dt> </dl>    | L’utilisateur actuel ne dispose pas d’un accès suffisant au fichier de configuration.<br/> |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl> | La configuration est inconnue.<br/>                                       |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>                                   |



## <a name="remarks"></a>Notes

Par défaut, les machines virtuelles en cours d’exécution sont enregistrées lorsque Windows Virtual PC est fermé. L’action d’arrêt **vmShutdownAction \_ Save** (0) enregistre l’état de la machine virtuelle. L’action **vmShutdownAction \_ turnoff** (1) désactive la machine virtuelle. L’action d' **\_ arrêt vmShutdownAction** (2) arrêtera le système d’exploitation invité si les composants d’intégration sont disponibles et ENREGISTRERA la machine virtuelle dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**VMShutdownAction**](vmshutdownaction.md)
</dt> </dl>

 

