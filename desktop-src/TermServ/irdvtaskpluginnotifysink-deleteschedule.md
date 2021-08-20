---
title: Méthode IRDVTaskPluginNotifySink DeleteSchedule
description: Appelé par l’agent de tâche pour supprimer une tâche planifiée.
ms.assetid: 67a9493e-367a-48c9-8f94-276d696406b7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode DeleteSchedule
- Méthode DeleteSchedule Services Bureau à distance, interface IRDVTaskPluginNotifySink
- Services Bureau à distance de l’interface IRDVTaskPluginNotifySink, méthode DeleteSchedule
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.DeleteSchedule
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5674b3624edc102be6943e63b72444ec68f403fa1066e90a410f028008894d29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129141"
---
# <a name="irdvtaskpluginnotifysinkdeleteschedule-method"></a>IRDVTaskPluginNotifySink ::D méthode eleteSchedule

Appelé par l’agent de tâche pour supprimer une tâche planifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeleteSchedule(
  [in] BSTR bstrIdentifier
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrIdentifier* \[ dans\]
</dt> <dd>

Identificateur de la tâche planifiée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------|
| Client minimal pris en charge<br/> | Windows 7 Entreprise<br/>   |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





