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
ms.openlocfilehash: 6bc0c09f802a63a5bfad92b49f76fcbb4ee242d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103540"
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

Retourne S \_ OK en cas de réussite, ou l’un des codes d’erreur Windows standard.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





