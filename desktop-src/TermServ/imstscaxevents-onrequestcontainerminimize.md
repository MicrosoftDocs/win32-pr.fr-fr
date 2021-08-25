---
title: Méthode IMsTscAxEvents OnRequestContainerMinimize
description: Appelé lorsque l’utilisateur appuie sur le bouton réduire de la barre de connexion en mode plein écran. Le déclenchement de cet événement est une demande que l’application conteneur réduit.
ms.assetid: fc052f9b-cf59-4d5a-ba39-571627b72f2a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnRequestContainerMinimize
- Méthode OnRequestContainerMinimize Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnRequestContainerMinimize
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRequestContainerMinimize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 344bd85d8d224a5901517c55c8e0a95c854ed246e74a9d0c8def1eebae515305
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125059"
---
# <a name="imstscaxeventsonrequestcontainerminimize-method"></a>IMsTscAxEvents :: OnRequestContainerMinimize, méthode

Appelé lorsque l’utilisateur appuie sur le bouton **réduire** de la barre de connexion en mode plein écran. Le déclenchement de cet événement est une demande que l’application conteneur réduit.

## <a name="syntax"></a>Syntaxe


```C++
void OnRequestContainerMinimize();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode sera appelée uniquement si le mode plein écran géré par le conteneur est activé. pour plus d’informations, consultez [**IMsTscAdvancedSettings ::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





