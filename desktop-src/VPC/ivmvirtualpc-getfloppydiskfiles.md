---
title: Méthode IVMVirtualPC GetFloppyDiskFiles (VPCCOMInterfaces. h)
description: Récupère un tableau de fichiers de disquettes virtuelles connus.
ms.assetid: c40f2780-eb84-4e0c-a493-1d1e5706cc8b
keywords:
- Méthode GetFloppyDiskFiles Virtual PC
- Méthode GetFloppyDiskFiles Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode GetFloppyDiskFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9759a3b909bb4f4ac179c166635185a701a8a16e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743444"
---
# <a name="ivmvirtualpcgetfloppydiskfiles-method"></a>IVMVirtualPC :: GetFloppyDiskFiles, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère un tableau de fichiers de disquettes virtuelles connus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFloppyDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outFloppyDiskFileList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*inAdditionalSearchPaths* \[ dans\]
</dt> <dd>

Ces chemins d’accès seront recherchés avec les chemins d’accès définis dans la propriété [**IVMVirtualPC :: SearchPaths**](ivmvirtualpc-searchpaths.md) .

</dd> <dt>

*outFloppyDiskFileList* \[ out, retval\]
</dt> <dd>

Tableau de fichiers de disquette virtuelle trouvés dans les chemins de recherche spécifiés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                        | Description                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'opération a réussi.<br/>                                                        |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                | Le paramètre *outFloppyDiskFileList* a la **valeur null**.<br/>                                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | Le paramètre *inAdditionalSearchPaths* n’est pas un tableau de chaînes.<br/>                  |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                        | Une erreur inattendue s’est produite.<br/>                                                    |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl> | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Notes

Les chemins de recherche utilisés pour récupérer le tableau de fichiers incluent ceux qui ont été précédemment définis par [**IVMVirtualPC :: SearchPaths**](ivmvirtualpc-searchpaths.md) en plus de ceux spécifiés par le paramètre *inAdditionalSearchPaths* et l’emplacement du programme d’installation du module Integration Components.

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

 

