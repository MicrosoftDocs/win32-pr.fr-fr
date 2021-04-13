---
title: Méthode IVMVirtualMachine RemoveConfigurationValue (VPCCOMInterfaces. h)
description: Supprime la valeur du paramètre de configuration spécifié pour cet ordinateur virtuel.
ms.assetid: 2d75a667-9656-4d4c-bafe-f3f8be3763f5
keywords:
- Méthode RemoveConfigurationValue Virtual PC
- Méthode RemoveConfigurationValue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683cad2c7cce34822f6f5607ea2676902284baf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466154"
---
# <a name="ivmvirtualmachineremoveconfigurationvalue-method"></a>IVMVirtualMachine :: RemoveConfigurationValue, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Supprime la valeur du paramètre de configuration spécifié pour cet ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR configurationKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*configurationKey* \[ dans\]
</dt> <dd>

Clé utilisée pour identifier la valeur de configuration telle qu’elle est stockée dans le \* fichier « . vmc ».

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                      | Description                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | L'opération a réussi.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | Le paramètre a la **valeur null** ou est vide.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>      | La configuration est inconnue.<br/>       |
| <dl> <dt>**Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables**</dt> <dt>0xA0040300</dt> </dl> | La préférence est introuvable.<br/>       |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>      | Une erreur inattendue s’est produite.<br/>   |



 

## <a name="remarks"></a>Notes

Cette méthode fournit un accès de bas niveau à toute valeur de configuration. Il peut être utilisé pour supprimer des valeurs de configuration pour les clés définies par le client. Soyez prudent si vous utilisez cette méthode pour supprimer les valeurs de configuration système, car certaines valeurs ne peuvent pas être modifiées pendant l’exécution de la machine virtuelle.

Les clés de configuration se trouvent dans le fichier « \* . vmc » de l’ordinateur virtuel au format XML. Les clés sont stockées de manière hiérarchique comme les clés de Registre dans Windows. Pour spécifier une sous-clé spécifique, un « chemin d’accès de clé » est construit, qui spécifie les différentes clés dans un format délimité par des barres obliques.

Par exemple, pour supprimer la valeur de la clé « RAM \_ Size » située dans l’arborescence de clé suivante :

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

La chaîne de chemin d’accès *configurationKey* est spécifiée comme suit :

``` syntax
"hardware/memory/ram_size"
```

Si l’une des clés de l’arborescence souhaitée a une valeur d’attribut « ID », l’attribut et sa valeur sont incorporés dans la chaîne de chemin d’accès *configurationKey* immédiatement après la clé de configuration associée en utilisant le format entre crochets suivant : « \[ @id = »*\_ valeur d’ID*« \] ».

Par exemple, pour supprimer la valeur de la clé « Absolute » située dans l’arborescence de clé suivante :

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

La chaîne de chemin d’accès *configurationKey* est spécifiée comme suit :

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

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
</dt> </dl>

 

