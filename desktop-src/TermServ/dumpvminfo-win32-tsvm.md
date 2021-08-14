---
title: Méthode DumpVmInfo de la classe Win32_TSVm
description: Ce membre est destiné à des fins de test interne et ne doit pas être utilisé dans votre code.
ms.assetid: 40cb4fdc-f657-47c6-8daa-684a12be30e4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DumpVmInfo
- Services Bureau à distance de la méthode DumpVmInfo, classe Win32_TSVm
- Win32_TSVm de la classe Services Bureau à distance, méthode DumpVmInfo
topic_type:
- apiref
api_name:
- Win32_TSVm.DumpVmInfo
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c74602e09f7aab4909e78bcd4696a450419e929b89769b35e16f21cbcafc080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354020"
---
# <a name="dumpvminfo-method-of-the-win32_tsvm-class"></a>Méthode DumpVmInfo de la \_ classe Win32 TSVm

Ce membre est destiné à des fins de test interne et ne doit pas être utilisé dans votre code.

## <a name="syntax"></a>Syntaxe


```mof
uint32 DumpVmInfo();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                             |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSVm Win32**](win32-tsvm.md)
</dt> </dl>

 

 





