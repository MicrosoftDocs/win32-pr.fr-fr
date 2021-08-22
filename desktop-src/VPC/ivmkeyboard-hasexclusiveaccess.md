---
title: IVMKeyboard HasExclusiveAccess, propriété (VPCCOMInterfaces. h)
description: Indique si cet objet a un contrôle exclusif sur le périphérique clavier de la machine virtuelle.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- HasExclusiveAccess propriété Virtual PC
- HasExclusiveAccess, propriété Virtual PC, IVMKeyboard, interface
- IVMKeyboard interface Virtual PC, propriété HasExclusiveAccess
topic_type:
- apiref
api_name:
- IVMKeyboard.HasExclusiveAccess
- IVMKeyboard.get_HasExclusiveAccess
- IVMKeyboard.put_HasExclusiveAccess
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c01e13e331824a0d1b6834cbb27da7eb4b5420a3cd3dbec94cdbdd494c79c95b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136722"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a>IVMKeyboard :: HasExclusiveAccess, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Indique si cet objet dispose d’un contrôle exclusif sur le périphérique clavier de l’ordinateur virtuel.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a>Valeur de la propriété

**True** si l’accès exclusif au clavier de l’ordinateur virtuel a été acquis ; sinon, **false** .

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                   | Signification                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                      | L'opération a réussi.<br/>                                                                                                                                                                                                        |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                        | Le paramètre *isExclusive* a la **valeur null**.<br/>                                                                                                                                                                                             |
| <dl> <dt>S \_ FALSe</dt> <dt>1</dt> </dl>                                   | Le mode exclusif demandé est déjà défini pour cet appareil. Cela peut se produire lorsque vous tentez de définir le mode exclusif lorsqu’il a déjà été acquis, ou lorsque vous essayez de libérer le mode exclusif lorsqu’il n’a pas été acquis précédemment.<br/> |
| <dl> <dt>Ordinateur virtuel \_ Échec de la \_ définition du \_ \_ mode \_ exclusif</dt> <dt>0xA0040825</dt> </dl> | Échec de la définition ou de la libération du mode exclusif comme demandé. Cela peut être dû au fait que la machine virtuelle n’est plus en cours d’exécution ou qu’un autre processus a déjà acquis le mode exclusif sur le périphérique clavier de la machine virtuelle.<br/>                                 |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                     | La chaîne spécifiée est vide ou contient un code de clé non valide.<br/>                                                                                                                                                                      |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                | Une erreur inattendue s’est produite.<br/>                                                                                                                                                                                                    |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard est défini en tant que 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

