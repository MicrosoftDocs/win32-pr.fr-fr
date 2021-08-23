---
title: IVMDisplay CanResize, propriété (VPCCOMInterfaces. h)
description: Détermine si l’invité autorise les modifications de résolution.
ms.assetid: 97f2aad9-aa27-4db2-ac5d-fa9645f0e674
keywords:
- CanResize propriété Virtual PC
- CanResize, propriété Virtual PC, IVMDisplay, interface
- IVMDisplay interface Virtual PC, propriété CanResize
topic_type:
- apiref
api_name:
- IVMDisplay.CanResize
- IVMDisplay.get_CanResize
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b55bc4ab9599b119988b68df022c098048aeee9ea19194e2c3dcbfdaefde479
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473579"
---
# <a name="ivmdisplaycanresize-property"></a>IVMDisplay :: CanResize, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Détermine si l’invité autorise les modifications de résolution.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_CanResize(
  [out, retval] VARIANT_BOOL *canResize
);
```



## <a name="property-value"></a>Valeur de la propriété

**Variante \_ TRUE** si l’invité autorise les modifications de résolution et la **\_ valeur false** dans le cas contraire.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                       | Signification                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'opération a réussi.<br/>                                                                                                              |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                            | Le paramètre a la **valeur null**.<br/>                                                                                                                 |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue </dl>                    | La configuration est inconnue.<br/>                                                                                                              |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt> </dl>               | L’ordinateur virtuel doit être en cours d’exécution pour cette opération.<br/>                                                                                    |
| <dl> <dt>Ordinateur virtuel \_ E \_ aucun \_ </dt> <dt>0xA0040850</dt> d’affichage </dl>                    | Aucun périphérique vidéo n’a été trouvé pour la machine virtuelle.<br/>                                                                                   |
| <dl> <dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt> </dl> | La fonctionnalité composants d’intégration n’est pas disponible. soit les composants d’intégration ne sont pas installés, soit la fonctionnalité a été désactivée.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                    | Une erreur inattendue s’est produite.<br/>                                                                                                          |



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

 

