---
title: Notification d’événements WMT_STATUS dans DirectShow
description: '\_Notification d’événement d’État WMT dans DirectShow'
ms.assetid: 6b777c7e-2777-445b-88de-a9a28be6da9c
keywords:
- Windows Media Format SDK, WMT_STATUS les notifications d’événements dans DirectShow
- Windows Media Format SDK, notifications d’événements
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), WMT_STATUS les notifications d’événements dans DirectShow
- ASF (format de systèmes avancés), WMT_STATUS les notifications d’événements dans DirectShow
- ASF (Advanced Systems Format), notifications d’événements
- ASF (format des systèmes avancés), notifications d’événements
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, notifications d’événements
- DirectShow, notifications d’événements WMT_STATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12c953b2c9b1509ad1b3adc2831d2276fcd474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199285"
---
# <a name="wmt_status-event-notification-in-directshow"></a>\_Notification d’événement d’État WMT dans DirectShow

Le lecteur ASF et l’enregistreur ASF transfèrent les événements d' [**\_ État WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) aux applications. Le writer transfère tous les événements de ce type, et le lecteur transfère uniquement ceux qui appartiennent à l’acquisition de licence DRM. Pour recevoir ces notifications d’événements dans votre application, ajoutez un cas pour l' **\_ \_ événement EC WMT** dans votre fonction de gestion des événements. Le *paramètre lParam1* associé à l’événement contient le code d' **\_ État WMT** (qui peut être une erreur WMT) et lParam2 contient des [**données d’événement « am \_ \_ \_ WMT**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) **\_ »** qui incluent le **HRESULT**.

 

 