---
title: Méthode IVMVirtualPC GetVirtualMachineFiles (VPCCOMInterfaces. h)
description: Récupère un tableau de fichiers de configuration d’ordinateur virtuel connus.
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- Méthode GetVirtualMachineFiles Virtual PC
- Méthode GetVirtualMachineFiles Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode GetVirtualMachineFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d1fe248b76756b39846d181341278f669d2f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317466"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a>IVMVirtualPC :: GetVirtualMachineFiles, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère un tableau de fichiers de configuration d’ordinateur virtuel connus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*inAdditionalSearchPaths* \[ dans\]
</dt> <dd>

Ces chemins d’accès seront recherchés avec les chemins d’accès définis dans les propriétés [**IVMVirtualPC :: SearchPaths**](ivmvirtualpc-searchpaths.md) et [**IVMVirtualPC ::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) .

</dd> <dt>

*inExcludedRegisteredVMs* \[ dans\]
</dt> <dd>

**True** si les machines virtuelles inscrites doivent être exclues du retour de tableau dans le paramètre *outVirtualMachineFileList* et **false** dans le cas contraire.

</dd> <dt>

*outVirtualMachineFileList* \[ out, retval\]
</dt> <dd>

Tableau de chaînes de chemin d’accès pour les fichiers de configuration d’ordinateur virtuel trouvés dans les chemins de recherche spécifiés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                        | Description                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'opération a réussi.<br/>                                                        |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                | Le paramètre *outVirtualMachineFileList* a la **valeur null**.<br/>                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | Le paramètre *inAdditionalSearchPaths* n’est pas un tableau de chaînes.<br/>                  |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                        | Une erreur inattendue s’est produite.<br/>                                                    |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl> | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Notes

Les chemins de recherche utilisés pour récupérer le tableau de fichiers de configuration incluent ceux qui ont été précédemment définis par [**IVMVirtualPC :: SearchPaths**](ivmvirtualpc-searchpaths.md) et [**IVMVirtualPC ::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) en plus de ceux spécifiés par le paramètre *inAdditionalSearchPaths* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

