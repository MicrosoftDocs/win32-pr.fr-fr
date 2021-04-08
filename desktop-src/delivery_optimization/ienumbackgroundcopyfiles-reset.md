---
title: Méthode de réinitialisation IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Réinitialise la séquence d'énumération au début.
ms.assetid: 6A303069-105C-4053-A8C5-2ECF60E789DE
keywords:
- Reset (méthode)
- Reset, méthode, interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, méthode Reset
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Reset
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314c7cae44ae48402642c202a624b9a60590e55b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843385"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a>IEnumBackgroundCopyFiles :: Reset, méthode

Réinitialise la séquence d'énumération au début.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com **HRESULT** standard en cas d’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles est défini en tant que CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





