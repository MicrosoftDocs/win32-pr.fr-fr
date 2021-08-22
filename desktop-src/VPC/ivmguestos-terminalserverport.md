---
title: IVMGuestOS propriété TerminalServerPort
description: Port utilisé par Services Bureau à distance dans le système d’exploitation invité.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- TerminalServerPort propriété Virtual PC
- TerminalServerPort, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété TerminalServerPort
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServerPort
- IVMGuestOS.get_TerminalServerPort
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b9eea5c545613f05dbd828a9436175fab6bfc5a05ba2fe5f59588f78da913
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512159"
---
# <a name="ivmguestosterminalserverport-property"></a>IVMGuestOS :: TerminalServerPort, propriété

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Port utilisé par Services Bureau à distance (anciennement services Terminal Server) dans le système d’exploitation invité.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a>Valeur de la propriété

Retourne le port utilisé par Services Bureau à distance dans le système d’exploitation invité.



| Valeur                                                                              | Signification                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>3389</dt> </dl>    | Valeur par défaut<br/>                      |
| <dl> <dt>1 65535</dt> </dl> | Plage valide<br/>                        |
| <dl> <dt>0</dt> </dl>       | La valeur de port valide n’est pas disponible.<br/> |



 

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                                       | Signification                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'opération a réussi.<br/>                                                 |
| <dl> <dt>S \_ FALSe</dt> <dt>1</dt> </dl>                                       | Services Bureau à distance n’est pas encore initialisée dans le système d’exploitation invité.<br/> |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>                            | Le paramètre *tsPort* a la **valeur null**.<br/>                                           |
| <dl> <dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt> </dl>               | L’ordinateur virtuel n’est pas en cours d’exécution.<br/>                                           |
| <dl> <dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt> </dl> | Les composants d’intégration ne sont pas installés sur cet ordinateur virtuel.<br/>             |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl>                    | Une erreur inattendue s’est produite.<br/>                                             |



## <a name="remarks"></a>Remarques

La valeur de cette propriété n’est pas valide, sauf si la propriété [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) est définie sur **\_ true**.

Si la valeur de la propriété [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) est **\_ false** en raison d’une erreur de connexion sur le port, la valeur retournée par la propriété **TerminalServerPort** contient la valeur de l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                 |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                      |
| MIDL<br/>                      | <dl> <dt>IVMGuestOS. idl</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

