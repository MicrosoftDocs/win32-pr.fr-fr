---
title: Interface IMsRdpInputSink
description: Récepteur d’entrée Bureau à distance.
ms.assetid: ec30b64a-63bb-4f8f-8979-ab2ef9ece6b0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpInputSink
- Services Bureau à distance de l’interface IMsRdpInputSink, Description
topic_type:
- apiref
api_name:
- IMsRdpInputSink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad3112b3bb6df92bfb7e403e779773a2203f2cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118722"
---
# <a name="imsrdpinputsink-interface"></a>Interface IMsRdpInputSink

Récepteur d’entrée Bureau à distance.

## <a name="members"></a>Membres

L’interface **IMsRdpInputSink** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpInputSink** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMsRdpInputSink** possède ces méthodes.



| Méthode                                                               | Description                          |
|:---------------------------------------------------------------------|:-------------------------------------|
| [**AddTouchInput**](/previous-versions/windows/desktop/legacy/mt786987(v=vs.85))               | Ajoute une entrée tactile.<br/>         |
| [**BeginTouchFrame**](/previous-versions/windows/desktop/legacy/mt786988(v=vs.85))           | Commencez le cadre tactile.<br/>        |
| [**EndTouchFrame**](/previous-versions/windows/desktop/legacy/mt786989(v=vs.85))               | Cadre tactile final.<br/>          |
| [**SendKeyboardEvent**](/previous-versions/windows/desktop/legacy/mt786990(v=vs.85))       | Envoie un événement de clavier.<br/>     |
| [**SendMouseButtonEvent**](/previous-versions/windows/desktop/legacy/mt786991(v=vs.85)) | Envoie l’événement du bouton de la souris.<br/> |
| [**SendMouseMoveEvent**](/previous-versions/windows/desktop/legacy/mt786992(v=vs.85))     | Envoie l’événement de déplacement de la souris.<br/>   |
| [**SendMouseWheelEvent**](/previous-versions/windows/desktop/legacy/mt786993(v=vs.85))   | Envoie l’événement de roulette de la souris.<br/>  |
| [**SendSyncEvent**](/previous-versions/windows/desktop/legacy/mt786994(v=vs.85))               | Envoie l’événement de synchronisation.<br/>         |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                      |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpInputSink est défini en tant que 4606850E-76A7-4E28-A47E-C7174F619351<br/>     |



 

