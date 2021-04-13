---
title: Objet agent de révocation des licences
description: Objet agent de révocation des licences
ms.assetid: 19b0e697-1648-40e3-b6ef-c726905a47a2
keywords:
- Windows Media Format SDK, objets de l’agent de révocation des licences
- ASF (Advanced Systems Format), objets de l’agent de révocation des licences
- ASF (format des systèmes avancés), objets de l’agent de révocation des licences
- objets, objets de l’agent de révocation des licences
- révocation de licence, objets de l’agent de révocation des licences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a02e07c0f5e2f25c90b39ffcf21e15048e55dc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381479"
---
# <a name="license-revocation-agent-object"></a>Objet agent de révocation des licences

L’objet agent de révocation de licence gère le côté client de la révocation de licence. La révocation des licences est le processus par lequel un serveur de licences peut supprimer des licences du magasin de licences sur l’ordinateur client. Le processus consiste à transmettre plusieurs messages entre l’application cliente et le serveur de licences. Les méthodes exposées sur ce processus d’objet et génèrent ces messages.

L’objet agent de révocation de licences est créé par la fonction [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) , qui définit un pointeur vers une interface [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) . **IUnknown** et **IWMLicenseRevocationAgent** sont les seules interfaces prises en charge par cet objet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> </dl>

 

 




