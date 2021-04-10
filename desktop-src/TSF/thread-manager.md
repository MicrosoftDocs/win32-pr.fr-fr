---
title: Gestionnaire de threads
description: Le gestionnaire de threads est le composant de base du gestionnaire TSF.
ms.assetid: fd43b4c3-80bb-4118-a880-bdea07022c95
keywords:
- Text Services Framework (TSF), gestionnaire de threads
- TSF (Text Services Framework), gestionnaire de threads
- services de texte, gestionnaire de threads
- Applications compatibles TSF, gestionnaire de threads
- Gestionnaire de threads
- Gestionnaire TSF
- notifications d'événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b29596c5c39267181c6a2c301aede3f15ca7297
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031487"
---
# <a name="thread-manager"></a>Gestionnaire de threads

Le gestionnaire de threads est le composant de base du gestionnaire TSF. Le gestionnaire de threads effectue des tâches courantes liées aux applications et aux services de texte (clients). Ces tâches incluent, sans s’y limiter, l’activation et la désactivation des services de texte TSF, la création de gestionnaires de documents et la maintenance de la relation appropriée entre les documents et le focus d’entrée. Le gestionnaire de thread est défini par l’interface [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) .

La majorité des interfaces et des objets fournis par le gestionnaire TSF peuvent être obtenus à l’aide des méthodes fournies par l’interface du gestionnaire de threads.

## <a name="applications"></a>Applications

Une application crée un objet de gestionnaire de threads en appelant [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec CLSID \_ TFThreadMgr.

## <a name="text-services"></a>Services de texte

Un service de texte obtient un objet de gestionnaire de threads dans la méthode text service [ITfTextInputProcessor :: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) .

## <a name="event-notifications"></a>Notifications d'événements

Le gestionnaire de threads fournit également des notifications d’événements aux clients. Dans TSF, les notifications d’événements sont fournies au moyen d’un récepteur d’événements, qui est un objet COM. Pour recevoir des notifications du gestionnaire de threads, un client implémente un objet [ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink) et installe le récepteur d’événements. Le récepteur d’événements est installé en interrogeant le gestionnaire de threads pour IID \_ ITfSource et en appelant [ITfSource :: ADVISESINK](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) avec IID \_ ITfThreadMgrEventSink.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[ITfTextInputProcessor :: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[ITfThreadMgrEventSink](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgreventsink)
</dt> <dt>

[ITfSource :: AdviseSink](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> </dl>

 

 