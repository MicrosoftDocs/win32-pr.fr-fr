---
title: Méthode IRDVTaskPluginNotifySink OnTaskStateChange
description: Permet d’informer l’agent déclencheur que l’état d’une tâche a changé.
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnTaskStateChange
- Méthode OnTaskStateChange Services Bureau à distance, interface IRDVTaskPluginNotifySink
- Services Bureau à distance de l’interface IRDVTaskPluginNotifySink, méthode OnTaskStateChange
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510358"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a>IRDVTaskPluginNotifySink :: OnTaskStateChange, méthode

Permet d’informer l’agent déclencheur que l’état d’une tâche a changé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrIdentifier* \[ dans\]
</dt> <dd>

Type : **BSTR**

Identificateur de la tâche. Il s’agit de l’identificateur passé à la méthode [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*État* \[ dans\]
</dt> <dd>

Type : état de la **[ **\_ tâche \_ RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**

Valeur de l’énumération de l' [**\_ \_ État de la tâche RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) qui spécifie le nouvel état de la tâche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------|
| Client minimal pris en charge<br/> | Windows 7 Entreprise<br/>   |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**État de la \_ tâche RDV \_**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





