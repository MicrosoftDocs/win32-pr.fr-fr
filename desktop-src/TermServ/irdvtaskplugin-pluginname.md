---
title: IRDVTaskPlugin PluginName, propriété (Tspubplugincom. h)
description: Contient le nom complet de l’agent de tâche.
ms.assetid: 6f414270-e90b-4075-80fe-f918acbdd205
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PluginName
- Services Bureau à distance de la propriété PluginName, interface IRDVTaskPlugin
- Services Bureau à distance de l’interface IRDVTaskPlugin, propriété PluginName
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.PluginName
- IRDVTaskPlugin.get_PluginName
api_location:
- tspubplugincom.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078934c8f19085bf233df78501798a8416ceadf7ba6a0b663cb14b8a8c46b223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129330"
---
# <a name="irdvtaskpluginpluginname-property"></a>IRDVTaskPlugin ::P propriété luginName

Contient le nom complet de l’agent de tâche. Ce nom est utilisé uniquement à des fins de journalisation.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_PluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valeur de la propriété

Nom complet de l’agent de tâche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7 Entreprise<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Tspubplugincom. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





