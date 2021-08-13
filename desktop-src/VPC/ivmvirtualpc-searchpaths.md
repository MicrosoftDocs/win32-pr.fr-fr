---
title: IVMVirtualPC SearchPaths, propriété (VPCCOMInterfaces. h)
description: chemins d’accès de système de fichiers utilisés pour rechercher des fichiers associés à Windows Virtual PC.
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- SearchPaths propriété Virtual PC
- SearchPaths, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété SearchPaths
topic_type:
- apiref
api_name:
- IVMVirtualPC.SearchPaths
- IVMVirtualPC.get_SearchPaths
- IVMVirtualPC.put_SearchPaths
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4ef75bf0a696494b839f330063ca310927a0d796829d96575721f492b8b691
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471249"
---
# <a name="ivmvirtualpcsearchpaths-property"></a>IVMVirtualPC :: SearchPaths, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

récupère et définit les chemins d’accès du système de fichiers qui sont utilisés pour rechercher des fichiers associés à Windows Virtual PC.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_SearchPaths(
  [in]          VARIANT searchPaths
);

HRESULT get_SearchPaths(
  [out, retval] VARIANT *searchPaths
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie un SafeArray contenant un chemin d’accès au système de fichiers pour chaque entrée.

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                               | Signification                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | L'opération a réussi.<br/>                                                                                               |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                                    | Le paramètre a la **valeur null**.<br/>                                                                                                  |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                                 | Le paramètre *searchPaths* n’est pas valide et n’a pas pu être analysé dans un tableau de chemins d’accès.<br/>                                    |
| <dl> Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt> </dl> | Le système ne peut pas trouver un répertoire spécifié dans le paramètre *searchPaths* .<br/>                                                |
| <dl> Valeur <dt>HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)</dt> <dt>0x80070003</dt> </dl> | Le système ne trouve pas de chemin d’accès spécifié par le paramètre *searchPaths* .<br/>                                                     |
| <dl> Valeur <dt>HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)</dt> <dt>0x8007007b</dt> </dl>    | Un chemin d’accès spécifié dans le paramètre *searchPaths* contient des caractères non conformes. Les caractères non autorisés sont « \* ? <>/ \| » : «».<br/> |
| <dl> Valeur <dt>HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)</dt> <dt>0x800700a1</dt> </dl>    | Un chemin d’accès contenu dans le paramètre *searchPaths* spécifie un chemin d’accès vide ou relatif. Un chemin d’accès absolu est requis.<br/>          |
| <dl> Valeur <dt>HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)</dt> <dt>0x8007006f</dt> </dl> | Le chemin d’accès spécifié dans le paramètre *searchPaths* est trop long. La longueur du chemin d’accès doit être inférieure à 260 caractères.<br/>     |
| <dl> <dt>Ordinateur virtuel \_ E \_ Préférences \_ \_ introuvables</dt> <dt>0xA0040300</dt> </dl>                       | La préférence est introuvable.<br/>                                                                                               |
| <dl> <dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt> </dl>     | Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).<br/>                                        |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                            | Une erreur inattendue s’est produite.<br/>                                                                                           |



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

 

