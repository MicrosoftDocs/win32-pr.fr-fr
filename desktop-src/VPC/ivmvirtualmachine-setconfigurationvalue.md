---
title: Méthode IVMVirtualMachine SetConfigurationValue (VPCCOMInterfaces. h)
description: Définit la valeur du paramètre de configuration spécifié pour cette machine virtuelle.
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- Méthode SetConfigurationValue Virtual PC
- Méthode SetConfigurationValue Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode SetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7edef64484161f6151b1d2ac14fd6916a7d2a082c0c787b983019305027f4949
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652969"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a>IVMVirtualMachine :: SetConfigurationValue, méthode

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit la valeur du paramètre de configuration spécifié pour cette machine virtuelle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*configurationKey* \[ dans\]
</dt> <dd>

Clé utilisée pour identifier la valeur de configuration telle qu’elle est stockée dans le \* fichier « . vmc ».

> [!IMPORTANT]
> Les modifications doivent être apportées à " \* . VMC" uniquement à l’aide de la méthode **SetConfigurationValue** . La modification \* de « . VMC » à l’aide d’une autre méthode n’est pas prise en charge.

 

</dd> <dt>

*configurationValue* \[ dans\]
</dt> <dd>

Valeur de configuration. Cette valeur peut être l’un des types de **variantes** suivants : VT **\_ Array** \| **VT \_ UI1** (RAW bytes), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) ou **VT \_ bool** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                 | Description                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | Le paramètre *configurationKey* est **null** ou vide, ou le paramètre *configurationValue* n’est pas un type Variant valide.<br/> |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue </dl> | La configuration est inconnue.<br/>                                                                                            |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/>                                                                                        |



 

## <a name="remarks"></a>Remarques

Les valeurs suivantes sont prises en charge pour le paramètre *configurationKey* .



| valeur *configurationKey*                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Type de données            | Valeur par défaut     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| « matériel/BIOS/ \_ synchronisation de l’heure \_ au \_ démarrage »<br/>              | « true » si l’horloge CMOS de la machine virtuelle doit être synchronisée avec l’horloge de l’hôte au démarrage ; « false » dans le cas contraire.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | expression<br/> | "true"<br/> |
| « intégration/synchronisation de l’heure de l’hôte/de Microsoft/ \_ \_ activée »<br/> | « true » si la synchronisation de l’heure de l’hôte est activée dans les composants d’intégration ; « false » dans le cas contraire.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | expression<br/> | "true"<br/> |
| « options d’interface utilisateur \_ /publication de l' \_ application automatique \_ »<br/>                  | « true » si la publication automatique des applications est activée dans les composants d’intégration ; « false » dans le cas contraire. Cela est également appelé applications virtuelles.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | expression<br/> | "true"<br/> |
| « \_ options d’interface utilisateur/secondes \_ à \_ Enregistrer »<br/>                   | Nombre de secondes d’attente avant l’enregistrement de la machine virtuelle après la fermeture de toutes les applications. Toutefois, les valeurs inférieures à 20 et supérieures à 4 294 968 ont des significations particulières. Pour plus d’informations, consultez la liste suivante<br/> <dl> <dt><span id="0"></span>entre</dt> <dd> N’enregistrez jamais la machine virtuelle.<br/> </dd> <dt><span id="120"></span>1 20</dt> <dd> Patientez 20 secondes avant d’enregistrer la machine virtuelle.<br/> </dd> <dt><span id="214_294_967"></span>21 4 294 967</dt> <dd> Patientez le nombre de secondes spécifié avant d’enregistrer la machine virtuelle.<br/> </dd> <dt><span id="4_294_9684_294_967_295"></span>4 294 968 4 294 967 295</dt> <dd> Attendez 4 294 968 secondes avant d’enregistrer la machine virtuelle.<br/> </dd> </dl> | entière<br/> | 300<br/>    |



 

Cette méthode fournit un accès de bas niveau à toute valeur de configuration. Il peut être utilisé pour définir des valeurs de configuration pour les clés définies par le client. Soyez prudent si vous utilisez cette méthode pour définir les valeurs de configuration du système, car aucune vérification des erreurs n’est effectuée sur la valeur de configuration. En outre, certaines valeurs de configuration ne peuvent pas être modifiées pendant l’exécution de la machine virtuelle.

Les clés de configuration se trouvent dans le fichier « \* . vmc » de l’ordinateur virtuel au format XML. Les clés sont stockées de manière hiérarchique comme les clés de Registre dans Windows. Pour spécifier une sous-clé spécifique, un « chemin d’accès de clé » est construit, qui spécifie les différentes clés dans un format délimité par des barres obliques.

Par exemple, pour définir la valeur de la clé « RAM \_ Size » située dans l’arborescence de clé suivante :

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

La chaîne de chemin d’accès *configurationKey* est spécifiée comme suit :

``` syntax
"hardware/memory/ram_size"
```

Si l’une des clés de l’arborescence souhaitée a une valeur d’attribut « ID », l’attribut et sa valeur sont incorporés dans la chaîne de chemin d’accès *configurationKey* immédiatement après la clé de configuration associée en utilisant le format entre crochets suivant : « \[ @id = »*\_ valeur d’ID*« \] ».

Par exemple, pour définir la valeur de la clé « Golf » située dans l’arborescence de clé suivante :

``` syntax
<preferences>
  <alpha>
    <bravo>
      <charlie>
        <delta id="1">
          <echo id="0">
            <foxtrot>
              <golf type="string">D</golf>
```

La chaîne de chemin d’accès *configurationKey* est spécifiée comme suit :

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
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
</dt> <dt>

[**IVMVirtualPC::SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

