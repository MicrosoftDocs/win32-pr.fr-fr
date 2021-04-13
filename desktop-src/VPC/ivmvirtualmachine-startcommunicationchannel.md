---
title: Méthode IVMVirtualMachine StartCommunicationChannel (VPCCOMInterfaces. h)
description: Configure un canal de communication entre l’hôte et le système d’exploitation invité.
ms.assetid: e4b04aa8-8400-4aa4-ad54-71ef57dec82a
keywords:
- Méthode StartCommunicationChannel Virtual PC
- Méthode StartCommunicationChannel Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode StartCommunicationChannel
topic_type:
- apiref
api_name:
- IVMVirtualMachine.StartCommunicationChannel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac6ab73b6a955b6810eaea280dc25732e2a6721
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466379"
---
# <a name="ivmvirtualmachinestartcommunicationchannel-method"></a>IVMVirtualMachine :: StartCommunicationChannel, méthode

\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Configure un canal de communication entre l’hôte et le système d’exploitation invité.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT StartCommunicationChannel(
  [in] VMEndpointType inHostEndpointType,
  [in] BSTR           inHostEndPointName,
  [in] VMEndpointType inGuestEndpointType,
  [in] BSTR           inGuestEndpointName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*inHostEndpointType* \[ dans\]
</dt> <dd>

Ce paramètre doit être **vmEndpoint \_ NamedPipe** (0).

</dd> <dt>

*inHostEndPointName* \[ dans\]
</dt> <dd>

Nom de canal unique. Cette chaîne doit avoir la forme suivante : " \\ \\ . \\ canal \\ *pipeName*". La partie *pipeName* du nom peut inclure n’importe quel caractère autre qu’une barre oblique inverse, y compris des chiffres et des caractères spéciaux. La chaîne du nom de canal entier peut comporter jusqu’à 256 caractères. Les noms de canaux ne respectent pas la casse.

</dd> <dt>

*inGuestEndpointType* \[ dans\]
</dt> <dd>

Ce paramètre doit être **vmEndpoint \_ tcpip** (1).

</dd> <dt>

*inGuestEndpointName* \[ dans\]
</dt> <dd>

Numéro de port sur lequel le serveur TCP de l’invité écoute.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code/valeur de retour                                                                                                                                                                                  | Description                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                        | L'opération a réussi.<br/>                                                                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                       | Le paramètre *inHostEndpointType* n’est pas **vmEndpoint \_ NamedPipe** (0) ou le paramètre *inGuestEndpointType* n’est pas **vmEndpoint \_ tcpip** (1).<br/> |
| <dl> <dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt> </dl>                                          | Le paramètre *inHostEndPointName* ou *inGuestEndpointName* est **null** ou n’est pas une valeur valide.<br/>                                                    |
| <dl> <dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt> </dl>                                  | Une erreur inattendue s’est produite.<br/>                                                                                                                |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (handle d’erreur \_ non valide \_ )**</dt> <dt>0x80070006</dt> </dl>        | Un descripteur n’est pas valide.<br/>                                                                                                                           |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt> </dl>            | La mémoire disponible est insuffisante pour effectuer cette requête.<br/>                                                                                   |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ non \_ prête)**</dt> <dt>0x80070015</dt> </dl>             | Le système sous-jacent qu’il utilise pour fournir les services réseau est actuellement en cours d’initialisation.<br/>                                                        |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt> </dl>        | Le nom du canal est déjà utilisé.<br/>                                                                                                                 |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (canal d’erreur \_ \_ occupé)**</dt> <dt>0x800700e7</dt> </dl>             | Un ou plusieurs canaux sont en cours d’exécution et peuvent bientôt être disponibles.<br/>                                                                          |
| <dl> Valeur <dt>**HRESULT \_ À partir de \_ Win32 (nombre maximal d’erreurs de \_ \_ sessions \_ atteint)**</dt> <dt>0x80070161</dt> </dl> | Le nombre maximal de canaux de communication disponibles est en cours d’utilisation. Impossible de démarrer un autre canal pour l’instant.<br/>                              |
| <dl> Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ \_ incompatibilité de révision d’erreur)**</dt> <dt>0x8007051a</dt> </dl>     | Il existe une incompatibilité entre la version des sous-systèmes hôtes et invités. Pour plus d’informations, consultez le journal des événements Windows.<br/>                             |
| <dl> <dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt> </dl>                             | La machine virtuelle n’est pas en cours d’exécution.<br/>                                                                                                                           |



 

## <a name="remarks"></a>Notes

L’implémentation actuelle prend en charge uniquement l’interface de canal nommé sur l’hôte et l’interface TCP/IP sur le système d’exploitation invité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**VMEndpointType**](vmendpointtype.md)
</dt> </dl>

 

