---
title: Méthode IVMVirtualPC SetConfigurationValue (VPCCOMInterfaces. h)
description: Définit la valeur du paramètre de configuration spécifié.
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- Méthode SetConfigurationValue Virtual PC
- Méthode SetConfigurationValue Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode SetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecb8ff3bb68829e944461cedb1c86904c7150593
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509034"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a>IVMVirtualPC :: SetConfigurationValue, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Définit la valeur du paramètre de configuration spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*preferenceKey* \[ dans\]
</dt> <dd>

Clé utilisée pour identifier la préférence, telle qu’elle est stockée dans le fichier de configuration par utilisateur (Options.xml dans « % LocalAppData% \\ Microsoft \\ Windows Virtual PC »).

> [!IMPORTANT]
> Les modifications doivent être apportées à Options.xml uniquement à l’aide de la méthode **SetConfigurationValue** . La modification de Options.xml à l’aide d’une autre méthode n’est pas prise en charge.

 

</dd> <dt>

*preferenceValue* \[ dans\]
</dt> <dd>

Valeur de préférence. Cette valeur peut être l’un des types de **variantes** suivants : VT **\_ tableau** VT \| **\_ UI1** (octets bruts), **VT \_ BSTR** (chaîne), **VT \_ UI4** (entier) ou **VT \_ bool** (booléen).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                        | Description                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'opération a réussi.<br/>                                                        |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                | Le paramètre *preferenceKey* ou *PreferenceValue* a la **valeur null**.<br/>                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | Le paramètre *preferenceKey* n’est pas valide ou est une chaîne vide.<br/>                    |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                        | Une erreur inattendue s’est produite.<br/>                                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>0x80070005</dt> </dl>                           | L’utilisateur actuel ne dispose pas d’un accès suffisant au fichier de configuration.<br/>                  |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl> | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Notes

Les valeurs suivantes sont prises en charge pour le paramètre *preferenceKey* .



| valeur *preferenceKey*      | Description                                                                                                                                                                           | Type de données            | Valeur par défaut   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| « \_ délai d’inactivité »<br/> | Nombre de secondes pendant lesquelles vpc.exe doit attendre avant de quitter s’il n’y a pas de machines virtuelles ou d’applications actives utilisant les [interfaces de PC virtuels Windows](virtual-pc-interfaces.md).<br/> | entière<br/> | "30"<br/> |



 

Cette méthode fournit un accès de bas niveau à toute valeur de configuration. Il peut être utilisé pour définir des valeurs de configuration pour les clés définies par le client. Soyez prudent si vous utilisez cette méthode pour définir les valeurs de configuration du système, car aucune vérification des erreurs n’est effectuée sur la valeur de configuration. En outre, certaines valeurs de configuration ne peuvent pas être modifiées tant qu’un ordinateur virtuel est en cours d’exécution.

Les clés de configuration se trouvent dans le fichier « Options.xml » de l’ordinateur virtuel au format XML. Les clés sont stockées de manière hiérarchique comme les clés de Registre dans Windows. Pour spécifier une sous-clé spécifique, un « chemin d’accès de clé » est construit, qui spécifie les différentes clés dans un format délimité par des barres obliques.

Par exemple, pour définir la valeur de la clé « délai d’inactivité \_ » située dans l’arborescence de clé suivante :

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

La chaîne de chemin d’accès *preferenceKey* est spécifiée comme suit :

``` syntax
"idle_timeout"
```

Si l’une des clés de l’arborescence souhaitée a une valeur d’attribut « ID », l’attribut et sa valeur sont incorporés dans la chaîne de chemin d’accès *preferenceKey* immédiatement après la clé de configuration associée en utilisant le format entre crochets suivant : « \[ @id = »*\_ valeur d’ID*« \] ».

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

La chaîne de chemin d’accès *preferenceKey* est spécifiée comme suit :

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

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
</dt> <dt>

[**IVMVirtualMachine::SetConfigurationValue**](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

