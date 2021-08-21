---
title: Méthode IVMVirtualMachine GetActivationValue (VPCCOMInterfaces. h)
description: Récupère la valeur du paramètre d’activation spécifié pour cet ordinateur virtuel.
ms.assetid: 9a6f138f-6a8a-4cdf-8fb3-83d541d88fba
keywords:
- Méthode GetActivationValue Virtual PC
- Méthode GetActivationValue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode GetActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e03d1178df5961ba76a0ab61e74c781315cce07f32657903e5fa3e4e0a7623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123194"
---
# <a name="ivmvirtualmachinegetactivationvalue-method"></a>IVMVirtualMachine :: GetActivationValue, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère la valeur du paramètre d’activation spécifié pour cet ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetActivationValue(
  [in]          BSTR    activationKey,
  [out, retval] VARIANT *activationValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*clé* \[ dans\]
</dt> <dd>

Clé utilisée pour identifier la valeur d’activation telle qu’elle est stockée dans le \* fichier « . vmc ».

</dd> <dt>

*activationValue* \[ out, retval\]
</dt> <dd>

Valeur d’activation. Cette valeur peut être l’un des types de **variantes** suivants : VT **\_ tableau** VT \| **\_ UI1** (octets bruts), **VT \_ BSTR** (chaîne), **VT \_ I4** (entier) ou **VT \_ bool** (booléen).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                      | Description                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | L'opération a réussi.<br/>                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | Le paramètre *clé* est **null** ou vide.<br/>                          |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>              | Le paramètre *activationValue* a la **valeur null**.<br/>                                 |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl>      | La configuration est inconnue.<br/>                                                |
| <dl> <dt>**Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables**</dt> <dt>0xA0040300</dt> </dl> | La préférence est introuvable, ou cette configuration n’a pas d’activation valide.<br/> |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>      | Une erreur inattendue s’est produite.<br/>                                            |



 

## <a name="remarks"></a>Remarques

Cette méthode fournit un accès de bas niveau à toute valeur d’activation. Il peut être utilisé pour définir des valeurs d’activation pour les clés définies par le client. Lorsqu’un ordinateur virtuel est démarré, une copie de ses valeurs de configuration est créée, qui devient son ensemble de valeurs d’activation. Les valeurs d’activation sont conservées jusqu’à ce que la machine virtuelle soit arrêtée ou redémarrée. notez que Windows Virtual PC peut uniquement utiliser la configuration pour stocker des valeurs pour certaines clés, autrement dit, la valeur d’activation peut ne jamais être utilisée.

Les clés d’activation sont stockées en interne de manière hiérarchique, à l’instar des clés de Registre dans Windows. Pour spécifier une sous-clé spécifique, un « chemin d’accès de clé » est construit, qui spécifie les différentes clés dans un format délimité par des barres obliques.

Par exemple, pour lire la valeur de la clé « \_ action par défaut » située dans l’arborescence de clé suivante :

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

La chaîne de chemin d’accès *clé* est spécifiée comme suit :

``` syntax
"settings/undo_drives/default_action"
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

 

