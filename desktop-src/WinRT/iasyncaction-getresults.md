---
description: Obtient le résultat d’une action asynchrone.
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: 'IAsyncAction :: GetResults, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 62196c7f8ded67bed0ecdb3ea33420de54301bbd379615126ada158ea9e725ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561051"
---
# <a name="iasyncactiongetresults-method"></a>IAsyncAction :: GetResults, méthode

Obtient le résultat d’une action asynchrone.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetResults();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Cette méthode retourne toujours **S \_ OK**.

## <a name="remarks"></a>Remarques

L’appel de la méthode **GetResults** n’a aucun effet si l’implémentation actuelle a un type dynamique [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                    |
| En-tête<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
