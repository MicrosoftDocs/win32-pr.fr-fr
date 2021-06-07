---
title: IVMVirtualPC DefaultVMConfigurationPath, propriété (VPCCOMInterfaces. h)
description: Répertoire par défaut dans lequel rechercher les fichiers de configuration d’ordinateur virtuel disponibles.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- DefaultVMConfigurationPath propriété Virtual PC
- DefaultVMConfigurationPath, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété DefaultVMConfigurationPath
topic_type:
- apiref
api_name:
- IVMVirtualPC.DefaultVMConfigurationPath
- IVMVirtualPC.get_DefaultVMConfigurationPath
- IVMVirtualPC.put_DefaultVMConfigurationPath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09f6370dfb868ec386e05f361240a74412f13a7d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387635"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a>IVMVirtualPC ::D propriété efaultVMConfigurationPath

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère et définit le répertoire par défaut dans lequel rechercher les fichiers de configuration d’ordinateur virtuel disponibles.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie le chemin d’accès au répertoire pour les fichiers de configuration d’ordinateur virtuel par défaut. Dans la chaîne de chemin d’accès, une barre oblique inverse ( \\ ) peut apparaître immédiatement avant le caractère null de fin.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                               | Signification                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                                                                                 |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre *ConfigurationPath* a la **valeur null**.<br/>                                                                                                |
| <dl> Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt> </dl> | Le système ne peut pas trouver le répertoire spécifié par le paramètre *ConfigurationPath* .<br/>                                                          |
| <dl> Valeur <dt>HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)</dt> <dt>0x80070003</dt> </dl> | Le système ne trouve pas le chemin d’accès spécifié par le paramètre *ConfigurationPath* .<br/>                                                               |
| <dl> Valeur <dt>HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)</dt> <dt>0x8007007b</dt> </dl>    | Le paramètre *ConfigurationPath* contient un caractère non valide (l’un des éléments suivants : " \* ? <>/ \| " : ").<br/>                                   |
| <dl> Valeur <dt>HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)</dt> <dt>0x800700a1</dt> </dl>    | Le paramètre *ConfigurationPath* spécifie un chemin d’accès vide ou relatif. Un chemin d’accès absolu est requis.<br/>                                          |
| <dl> Valeur <dt>HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)</dt> <dt>0x8007006f</dt> </dl> | Le chemin d’accès spécifié par le paramètre *ConfigurationPath* est trop long. La longueur du chemin d’accès doit être inférieure à la longueur **maximale \_** (260) caractères.<br/> |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                                                                                             |
| <dl> <dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt> </dl>     | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/>                                                          |



## <a name="remarks"></a>Remarques

Par défaut, cette valeur de propriété est définie sur le répertoire suivant : « % LocalAppData% \\ Microsoft \\ Windows Virtual PC \\ machines virtuelles \\ ».

## <a name="requirements"></a>Spécifications



| Condition requise | Value |
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

 

