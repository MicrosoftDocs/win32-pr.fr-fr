---
title: Méthode IVMVirtualPC FindVirtualNetwork (VPCCOMInterfaces. h)
description: Récupère un objet réseau virtuel qui correspond au nom demandé.
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- Méthode FindVirtualNetwork Virtual PC
- Méthode FindVirtualNetwork Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode FindVirtualNetwork
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc8cfb0b8f9b7ee5be7bfb25d7d4cd7ca7b215bcf1824262c576038e75e6ce0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592134"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a>IVMVirtualPC :: FindVirtualNetwork, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère un objet réseau virtuel qui correspond au nom demandé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*virtualNetworkName* \[ dans\]
</dt> <dd>

Nom du réseau virtuel à rechercher.

</dd> <dt>

*virtualNetwork* \[ out, retval\]
</dt> <dd>

Pointeur vers un nouvel objet [**IVMVirtualNetwork**](ivmvirtualnetwork.md) qui représente ce réseau virtuel.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                            | Description                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                        |
| <dl> <dt>**S \_ FALSe**</dt> <dt>1</dt> </dl>                                               | Le réseau virtuel spécifié est introuvable.<br/>                                    |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre *virtualNetwork* est **null** ou le réseau virtuel est introuvable.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | Le paramètre *virtualNetworkName* n’est pas valide ou est une chaîne vide.<br/>               |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)**</dt> <dt>0x80070002</dt> </dl> | Le fichier de réseau virtuel est introuvable.<br/>                                         |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                                    |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl>     | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Notes

Les noms de réseaux virtuels ne respectent pas la casse, par exemple, « MyNetwork » et « mynetwork » font référence au même réseau virtuel.

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

 

