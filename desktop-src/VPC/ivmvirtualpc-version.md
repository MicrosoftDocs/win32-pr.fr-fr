---
title: Propriété version de IVMVirtualPC (VPCCOMInterfaces. h)
description: récupère la version de cette instance de Windows Virtual PC.
ms.assetid: efcd5e71-8752-45a2-8138-4bc214762f39
keywords:
- Propriété de version Virtual PC
- Propriété de version Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, propriété version
topic_type:
- apiref
api_name:
- IVMVirtualPC.Version
- IVMVirtualPC.get_Version
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fad1f72c5a87e047001f013c70e5b730bcd06b342d8e56cc390b62b2f284ae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591692"
---
# <a name="ivmvirtualpcversion-property"></a>IVMVirtualPC :: version, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

récupère la version de cette instance de Windows Virtual PC.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Version(
  [out, retval] BSTR *version
);
```



## <a name="property-value"></a>Valeur de la propriété

Version.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                           | Signification                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                              | L'opération a réussi.<br/>                                                        |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                                | Le paramètre a la **valeur null**.<br/>                                                           |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                        | Une erreur inattendue s’est produite.<br/>                                                    |
| <dl> <dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt> </dl> | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/> |



## <a name="remarks"></a>Notes

les informations de version de Windows Virtual PC sont retournées sous la forme d’une valeur de chaîne au format suivant : «*v*. *s*. *BBB*. *tee*», où *v* est le numéro de version principale, *s* est le numéro de version mineure, *bbb* est le numéro de build, *t* est le type de build (0 = version release) et *ee* est l’édition server (SE = Édition Standard, EE = Êdition Entreprise).

## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

