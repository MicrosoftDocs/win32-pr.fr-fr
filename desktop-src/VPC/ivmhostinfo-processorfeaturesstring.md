---
title: IVMHostInfo ProcessorFeaturesString, propriété (VPCCOMInterfaces. h)
description: Récupère la liste des fonctionnalités prises en charge par le processeur hôte.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- ProcessorFeaturesString propriété Virtual PC
- ProcessorFeaturesString, propriété Virtual PC, IVMHostInfo, interface
- IVMHostInfo interface Virtual PC, propriété ProcessorFeaturesString
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorFeaturesString
- IVMHostInfo.get_ProcessorFeaturesString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1040702df250c906bb32af5068a340c37a9ba3faabee3af17d8397bfdc8059e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998889"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a>IVMHostInfo ::P propriété rocessorFeaturesString

\[Windows Virtual PC ne peut plus être utilisé à partir de Windows 8. Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Récupère la liste des fonctionnalités prises en charge par le processeur hôte.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a>Valeur de la propriété

Liste de fonctionnalités délimitées par des virgules. Par exemple : « MMX, SSE, SSE2, x86-64 ».



| Valeur                                                                                 | Signification                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>« AMD-V »</dt> </dl>    | Prend en charge les extensions de virtualisation AMD.<br/>              |
| <dl> <dt>« Intel VT »</dt> </dl> | Prend en charge les extensions de la technologie de virtualisation Intel.<br/> |
| <dl> <dt>"HAVD"</dt> </dl>     | La virtualisation d’assistance matérielle est désactivée.<br/>            |
| <dl> <dt>AVEZ</dt> </dl>     | La virtualisation d’assistance matérielle est activée.<br/>             |
| <dl> <dt>TECHNOLOGIE</dt> </dl>      | Prend en charge les extensions MMX.<br/>                             |
| <dl> <dt>SSE</dt> </dl>      | Prend en charge les extensions streaming SIMD.<br/>                  |
| <dl> <dt>SSE2</dt> </dl>     | Prend en charge les extensions streaming SIMD 2.<br/>                |
| <dl> <dt>SSE3</dt> </dl>     | Prend en charge les extensions streaming SIMD 3.<br/>                |
| <dl> <dt>"TXTE"</dt> </dl>     | Prend en charge les extensions de la technologie d’exécution de confiance.<br/>    |
| <dl> <dt>« x86-64 »</dt> </dl>   | Prend en charge les extensions x86-64.<br/>                              |



 

## <a name="error-codes"></a>Codes d’erreur



| Nom/valeur                                                                                                                                                    | Signification                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'opération a réussi.<br/>     |
| <dl> <dt>E \_ POINTEUR</dt> <dt>0x80004003</dt> </dl>         | Le paramètre a la **valeur null**.<br/>        |
| <dl> <dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt> </dl> | Une erreur inattendue s’est produite.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                     |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                          |
| Produit<br/>                  | Windows Virtual PC<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo est défini en tant que 5b5cf343-05ad-453B-BE99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

