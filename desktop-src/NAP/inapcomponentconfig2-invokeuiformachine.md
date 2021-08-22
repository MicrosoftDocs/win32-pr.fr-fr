---
title: Méthode INapComponentConfig2 InvokeUIForMachine (NapCommon. h)
description: Est implémenté par les validateurs d’intégrité système (SHV) si nécessaire pour gérer la configuration distante directement sur l’ordinateur spécifié. Cette méthode lance une interface utilisateur de gestion de la configuration.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- Méthode InvokeUIForMachine NAP
- Méthode InvokeUIForMachine NAP, interface INapComponentConfig2
- INapComponentConfig2 interface NAP, méthode InvokeUIForMachine
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8321425cf878bd9b3d8702f73fa464ae069420cd0e59f57e2500151fda01b191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940187"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a>INapComponentConfig2 :: InvokeUIForMachine, méthode

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La méthode **InvokeUIForMachine** est implémentée par les validateurs d’intégrité système (SHV) si nécessaire pour gérer la configuration distante directement sur l’ordinateur spécifié. Cette méthode lance une interface utilisateur de gestion de la configuration.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwndParent* \[ dans\]
</dt> <dd>

Handle de la fenêtre parente ou propriétaire. Un handle de fenêtre valide doit être fourni.

</dd> <dt>

*nomordinateur* \[ dans\]
</dt> <dd>

Pointeur vers un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient le nom de l’ordinateur du client NAP.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

retourne \_ la valeur OK si l’opération réussit ou l’un des codes d’erreur Windows standard.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





