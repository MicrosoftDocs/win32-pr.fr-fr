---
title: Méthode IVMVirtualMachine GetConfigurationValue (VPCCOMInterfaces. h)
description: Récupère la valeur du paramètre de configuration spécifié pour cet ordinateur virtuel.
ms.assetid: fd3c509e-8a40-4828-b866-6bd2cb455ab2
keywords:
- Méthode GetConfigurationValue Virtual PC
- Méthode GetConfigurationValue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode GetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b58a048b2dd93f6aab7f071912519dac356896d6e32a13809f4560a3db9fb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592714"
---
# <a name="ivmvirtualmachinegetconfigurationvalue-method"></a>IVMVirtualMachine :: GetConfigurationValue, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère la valeur du paramètre de configuration spécifié pour cet ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    configurationKey,
  [out, retval] VARIANT *configurationValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*configurationKey* \[ dans\]
</dt> <dd>

Clé utilisée pour identifier la valeur de configuration telle qu’elle est stockée dans le \* fichier « . vmc ».

</dd> <dt>

*configurationValue* \[ out, retval\]
</dt> <dd>

Valeur de configuration. Cette valeur peut être l’un des types de **variantes** suivants : VT **\_ tableau** VT \| **\_ UI1** (octets bruts), **VT \_ BSTR** (chaîne), **VT \_ I4** (entier) ou **VT \_ bool** (booléen).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                      | Description                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | L'opération a réussi.<br/>                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | Le paramètre *configurationKey* est **null** ou vide.<br/> |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>              | Le paramètre *configurationValue* a la **valeur null**.<br/>        |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>      | La configuration est inconnue.<br/>                          |
| <dl> <dt>**Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables**</dt> <dt>0xA0040300</dt> </dl> | La préférence est introuvable.<br/>                          |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>      | Une erreur inattendue s’est produite.<br/>                      |



 

## <a name="remarks"></a>Notes

Cette méthode fournit un accès de bas niveau à toute valeur de configuration. Il peut être utilisé pour lire les valeurs de configuration des clés définies par le client.

Les clés de configuration se trouvent dans le fichier « \* . vmc » de l’ordinateur virtuel au format XML. Les clés sont stockées de manière hiérarchique comme les clés de Registre dans Windows. Pour spécifier une sous-clé spécifique, un « chemin d’accès de clé » est construit, qui spécifie les différentes clés dans un format délimité par des barres obliques.

Par exemple, pour lire la valeur de la clé « RAM \_ Size » située dans l’arborescence de clé suivante :

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

Par exemple, pour lire la valeur de la clé « Absolute » située dans l’arborescence de clé suivante :

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
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

