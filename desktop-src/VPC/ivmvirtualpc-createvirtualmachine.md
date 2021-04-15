---
title: Méthode IVMVirtualPC CreateVirtualMachine (VPCCOMInterfaces. h)
description: Crée une nouvelle configuration d’ordinateur virtuel et récupère l’objet ordinateur virtuel.
ms.assetid: 35f7364f-debd-4b9c-8240-23c0512eb004
keywords:
- Méthode CreateVirtualMachine Virtual PC
- Méthode CreateVirtualMachine Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, méthode CreateVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 494d5166271e6c4086b8dfee12deb61e32ae8a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466266"
---
# <a name="ivmvirtualpccreatevirtualmachine-method"></a>IVMVirtualPC :: CreateVirtualMachine, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Crée une nouvelle configuration d’ordinateur virtuel et récupère l’objet ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ConfigurationName* \[ dans\]
</dt> <dd>

Nom de la machine virtuelle à créer. La longueur du nom ne peut pas dépasser 80 caractères et la longueur combinée du nom et du chemin d’accès aux fichiers VMC et VMCX ne peut pas dépasser les caractères de **\_ chemin d’accès maximal** (260). Les extensions de nom de fichier. vmc et. vmcx seront ajoutées à la fin du nom de l’ordinateur virtuel lors de la création des fichiers de configuration. Si ce paramètre a la **valeur null** ou est une chaîne vide, le paramètre *ConfigurationPath* doit spécifier le chemin d’accès complet au fichier VMC.

</dd> <dt>

*ConfigurationPath* \[ dans\]
</dt> <dd>

Chemin d’accès au dossier qui contiendra le fichier VMC. Ce dossier sera créé s’il n’existe pas. Si *ConfigurationName* a la **valeur null** ou est une chaîne vide, le chemin d’accès complet du nouveau fichier de configuration doit être spécifié.

</dd> <dt>

*VirtualMachine* \[ out, retval\]
</dt> <dd>

Pointeur vers un nouvel objet [**IVMVirtualMachine**](ivmvirtualmachine.md) qui représente cet ordinateur virtuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                            | Description                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                                                                                                                                       |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre *ConfigurationName* ou *ConfigurationPath* n’est pas valide, ou le paramètre *VirtualMachine* est **null**.<br/>                                                                               |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt> </dl> | Le système ne trouve pas le chemin d’accès spécifié par le paramètre *ConfigurationPath* .<br/>                                                                                                                     |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt> </dl>    | Le paramètre *ConfigurationPath* contient un caractère non valide (l’un des « \* ?: <>/ \| »).<br/>                                                                                                        |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt> </dl>    | Le paramètre *ConfigurationPath* spécifie un chemin d’accès vide ou relatif. Un chemin d’accès absolu est requis.<br/>                                                                                                |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt> </dl> | Le chemin d’accès spécifié par les paramètres *ConfigurationName* et *ConfigurationPath* génère un chemin d’accès trop long. La longueur totale du chemin d’accès doit être inférieure à la longueur **maximale \_** (260) caractères.<br/> |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt> </dl>  | Un fichier de configuration portant ce nom existe déjà à cet emplacement.<br/>                                                                                                                                |
| <dl> <dt>**Ordinateur virtuel \_ E \_ config \_ sans \_ nom**</dt> <dt>0xA0040400</dt> </dl>                       | Le paramètre *ConfigurationName* est vide.<br/>                                                                                                                                                         |
| <dl> <dt>**Ordinateur virtuel \_ Nom de la \_ configuration E \_ \_ trop \_ long**</dt> <dt>0xA0040401</dt> </dl>                | La longueur du paramètre *ConfigurationName* dépasse 80 caractères.<br/>                                                                                                                                  |
| <dl> <dt>**Ordinateur virtuel \_ Nom de la configuration E 0xA0040402 \_ \_ \_ \_ char non valide**</dt> <dt></dt> </dl>            | Le paramètre *ConfigurationName* contient un caractère non valide (l’un des « \* ?: <>/ \| \\ »).<br/>                                                                                                      |
| <dl> <dt>**Ordinateur virtuel \_ \_ \_ \_ Nom en double de la configuration E**</dt> <dt>0xA0040403</dt> </dl>                | Il existe déjà un ordinateur virtuel portant ce nom.<br/>                                                                                                                                                  |
| <dl> <dt>**Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée**</dt> <dt>0xA0040951</dt> </dl>     | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/>                                                                                                                |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Notes

Les noms de machine virtuelle ne respectent pas la casse, par exemple, « MyVM » et « MyVM » font référence à la même machine virtuelle.

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

 

