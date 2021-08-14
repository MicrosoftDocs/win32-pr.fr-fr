---
title: Interface IVMKeyboard (VPCCOMInterfaces. h)
description: Contrôle le périphérique clavier au sein d’un ordinateur virtuel. Le IVMKeyboard d’un ordinateur virtuel peut être récupéré à l’aide de la propriété de clavier IVMVirtualMachine.
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- Virtual PC de l’interface IVMKeyboard
- IVMKeyboard interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMKeyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7284c4e2bb164cd53c8a34357c881ed096f342ae2c2230422985fac4c1fdae9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344796"
---
# <a name="ivmkeyboard-interface"></a>Interface IVMKeyboard

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Contrôle le périphérique clavier au sein d’un ordinateur virtuel. Le **IVMKeyboard** d’un ordinateur virtuel peut être récupéré à l’aide de la propriété [**IVMVirtualMachine :: Keyboard**](ivmvirtualmachine-keyboard.md) .

## <a name="members"></a>Membres

L’interface **IVMKeyboard** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMKeyboard** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IVMKeyboard** possède ces méthodes.



| Méthode                                                       | Description                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**IsPressed**](ivmkeyboard-ispressed.md)                   | Détermine si la touche spécifiée est enfoncée.<br/>                      |
| [**PressAndReleaseKey**](ivmkeyboard-pressandreleasekey.md) | Simule une touche enfoncée, puis relâchée.<br/>              |
| [**PressKey**](ivmkeyboard-presskey.md)                     | Simule une touche enfoncée.<br/>                                |
| [**ReleaseKey**](ivmkeyboard-releasekey.md)                 | Simule une touche en cours de libération.<br/>                                    |
| [**TypeAsciiText**](ivmkeyboard-typeasciitext.md)           | Simule une série de touches ASCII tapées dans l’invité.<br/>       |
| [**TypeKeySequence**](ivmkeyboard-typekeysequence.md)       | Simule une liste délimitée par des virgules des clés en cours de saisie dans l’invité.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IVMKeyboard** possède les propriétés suivantes.



| Propriété                                                                | Type d’accès           | Description                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md)<br/> | Lecture/écriture<br/> | Indique si cet objet a un contrôle exclusif sur le périphérique clavier de l’ordinateur virtuel.<br/> |



 

## <a name="remarks"></a>Remarques

Les clés peuvent être tapées dans la machine virtuelle de plusieurs façons. Pour taper une séquence de caractères ASCII normale, utilisez la méthode [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) . Si vous avez besoin d’une plus grande flexibilité, **IVMKeyboard** dispose de plusieurs méthodes conçues pour être utilisées avec les codes de touches de la liste suivante. La méthode [**TypeKeySequence**](ivmkeyboard-typekeysequence.md) peut accepter une chaîne délimitée par des virgules de codes clés, qui sera appuyée et libérée, dans l’ordre, dans l’ordinateur virtuel. En plus de ces codes clés, les mots clés UP et UpDown peuvent être utilisés pour forcer une touche à uniquement être enfoncée ou être libérée. Les mots clés UP et UpDown s’appliquent uniquement au code clé qui suit directement le mot clé.

Pour éviter que plusieurs scripts, applications ou utilisateurs essaient d’accéder simultanément au même périphérique clavier, affectez la valeur **true** à la propriété [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) . Si l’accès exclusif est acquis par un processus, toute tentative d’envoi d’une entrée au clavier par d’autres processus est ignorée jusqu’à ce que l’accès exclusif soit libéré.

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

[Windows Interfaces Virtual PC](virtual-pc-interfaces.md)
</dt> <dt>

[Séquences de touches](key-sequences.md)
</dt> </dl>

 

