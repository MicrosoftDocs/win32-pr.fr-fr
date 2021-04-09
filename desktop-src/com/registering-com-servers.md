---
title: Inscription des serveurs COM
description: Inscription des serveurs COM
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102377"
---
# <a name="registering-com-servers"></a>Inscription des serveurs COM

Après avoir défini une classe dans le code (en veillant à ce qu’elle implémente [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) ou [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) et lui ait assigné un CLSID, vous devez placer dans le registre des informations qui permettront à com, à la demande d’un client avec le CLSID, de créer des instances de ses objets. Ces informations indiquent au système, pour un CLSID donné, où se trouve le code DLL ou EXE de cette classe et comment il doit être lancé.

Il existe plusieurs façons d’inscrire une classe dans le registre. En outre, il existe d’autres façons d’inscrire une classe dans le système lorsqu’elle s’exécute, de sorte que le système sait qu’un objet en cours d’exécution est actuellement dans le système.

Pour plus d’informations sur l’inscription, consultez les rubriques suivantes :

-   [Inscription d’une classe lors de l’installation](registering-a-class-at-installation.md)
-   [Inscription d’un serveur exécutable en cours d’exécution](registering-a-running-exe-server.md)
-   [Inscription d’objets dans le ROT](registering-objects-in-the-rot.md)
-   [Inscription automatique](self-registration.md)
-   [Installation d’une application en tant que service](installing-as-a-service-application.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Responsabilités du serveur COM](com-server-responsibilities.md)
</dt> </dl>

 

 