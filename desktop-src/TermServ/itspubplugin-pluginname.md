---
title: ItsPubPlugin propriété pluginName
description: Récupère le nom du plug-in.
ms.assetid: c1ea46b6-fac6-4140-a278-cb04ee9af739
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété pluginName
- Services Bureau à distance de la propriété pluginName, interface ItsPubPlugin
- Services Bureau à distance de l’interface ItsPubPlugin, propriété pluginName
topic_type:
- apiref
api_name:
- ItsPubPlugin.pluginName
- ItsPubPlugin.get_pluginName
api_location:
- Cpubplugin.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f5aa6ff6659047e9be48fd7b7a41f652c5cfd9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919812"
---
# <a name="itspubpluginpluginname-property"></a>ItsPubPlugin ::p propriété luginName

Récupère le nom du plug-in.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_pluginName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers une variable **BSTR** devant recevoir le nom du plug-in.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                         |
| MIDL<br/>                      | <dl> <dt>Cpubplugin. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ItsPubPlugin**](/windows/desktop/api/tspubplugincom/nn-tspubplugincom-itspubplugin)
</dt> </dl>

 

 





