---
title: Méthode IVMVirtualPC GetHardDiskFiles (VPCCOMInterfaces. h)
description: Récupère un tableau de fichiers de disque dur virtuel connus.
ms.assetid: 3f949ebc-5974-4919-84a2-8411f558f85f
keywords:
- Méthode GetHardDiskFiles Virtual PC
- Méthode GetHardDiskFiles Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode GetHardDiskFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDiskFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 902cd124db27ae65b8f589ded8b2b3188a7e0df67b0ff20071abd04daf5ab894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136572"
---
# <a name="ivmvirtualpcgetharddiskfiles-method"></a>IVMVirtualPC :: GetHardDiskFiles, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère un tableau de fichiers de disque dur virtuel connus.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetHardDiskFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outHardDiskFileList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*inAdditionalSearchPaths* \[ dans\]
</dt> <dd>

Ces chemins d’accès seront recherchés avec les chemins d’accès définis dans la propriété [**IVMVirtualPC :: SearchPaths**](ivmvirtualpc-searchpaths.md) .

</dd> <dt>

*outHardDiskFileList* \[ out, retval\]
</dt> <dd>

Tableau de chaînes de chemin d’accès pour les fichiers de disque dur virtuel trouvés dans les chemins de recherche spécifiés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                        | Description                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'opération a réussi.<br/>                                                        |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                | Le paramètre *outHardDiskFileList* a la **valeur null**.<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | Le paramètre *inAdditionalSearchPaths* n’est pas un tableau de chaînes.<br/>                  |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                        | Une erreur inattendue s’est produite.<br/>                                                    |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl> | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Remarques

Les chemins de recherche utilisés pour récupérer le tableau de fichiers incluent ceux qui ont été précédemment définis par [**IVMVirtualPC :: SearchPaths**](ivmvirtualpc-searchpaths.md) en plus de ceux spécifiés par le paramètre *inAdditionalSearchPaths* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
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

 

