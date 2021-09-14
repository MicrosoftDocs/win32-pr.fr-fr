---
title: Inscription d’une classe lors de l’installation
description: Si une classe est destinée à être disponible pour les clients à tout moment, dans la mesure où la plupart des applications sont, vous l’inscrivez généralement par le biais d’un programme d’installation et d’installation.
ms.assetid: 6d78c2ce-56d8-4866-9801-35125ec9cac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4253c40cb3feb7e737368c947c0b20715f5becbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923123"
---
# <a name="registering-a-class-at-installation"></a>Inscription d’une classe lors de l’installation

Si une classe est destinée à être disponible pour les clients à tout moment, dans la mesure où la plupart des applications sont, vous l’inscrivez généralement par le biais d’un programme d’installation et d’installation. Cela implique de placer des informations sur l’application dans le registre, notamment comment et où ses objets doivent être instanciés. Ces informations doivent être inscrites pour tous les CLSID. D’autres informations sont facultatives. Les outils tels que regsvr32 facilitent l’écriture d’un programme d’installation qui inscrit des serveurs lors de l’installation.

Si vous ne vous fiez pas aux valeurs système par défaut, il existe deux clés importantes dans le registre : le CLSID et l’AppID. Parmi les informations importantes sous ces clés, citons l’instanciation de l’objet. Les objets peuvent être désignés en tant que in-process, hors processus local ou à distance hors processus.

Sous la clé AppID se trouvent plusieurs valeurs qui définissent des informations spécifiques à cette application. Parmi celles-ci, citons [RemoteServerName](remoteservername.md) et [ActivateAtStorage](activateatstorage.md), qui peuvent être utilisées pour permettre à un client de créer un objet, le client n’ayant aucune connaissance intégrée de l’emplacement du serveur. (Pour plus d’informations sur l’instanciation distante, consultez [localisation d’un objet distant](locating-a-remote-object.md) et [fonctions d’assistance de création d’instance](instance-creation-helper-functions.md).)

Un serveur peut également être installé en tant que service ou exécuté sous un compte d’utilisateur spécifique. Pour plus d’informations, consultez [installation de en tant qu’application de service](installing-as-a-service-application.md).

Un serveur ou un objet ROT qui n’est pas un service ou qui s’exécute sous un compte d’utilisateur spécifique peut être appelé serveur « activer en tant qu’activateur ». Pour ces serveurs, le contexte de sécurité et la station ou le bureau Windows du client doivent correspondre à la version du serveur. Un client qui tente de se connecter à un serveur distant est considéré comme ayant un bureau ou une station de fenêtre **null** , de sorte que seul le contexte de sécurité du serveur est comparé dans cette instance. (Pour plus d’informations sur les SID, consultez [sécurité dans com](security-in-com.md).) COM met en cache la station ou le bureau Windows d’un processus lorsque le processus se connecte pour la première fois au service COM distribué. Par conséquent, les clients et les serveurs COM ne doivent pas modifier leur station Windows ou les bureaux de thread du processus après avoir appelé [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).

Quand une classe est inscrite en tant que processus in-process, un appel à [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) pour créer son objet de classe est passé automatiquement par com à la fonction [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) , que la classe doit implémenter pour accorder à l’objet appelant un pointeur vers son objet de classe.

Les classes implémentées dans des exécutables peuvent spécifier que COM doit exécuter leur processus et attendre que le processus enregistre l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) de l’objet de classe via un appel à la fonction [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clés de registre COM](com-registry-keys.md)
</dt> <dt>

[Installation d’une application en tant que service](installing-as-a-service-application.md)
</dt> <dt>

[Inscription d’un serveur exécutable en cours d’exécution](registering-a-running-exe-server.md)
</dt> <dt>

[Inscription des composants](registering-components.md)
</dt> <dt>

[Inscription d’objets dans le ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Inscription automatique](self-registration.md)
</dt> </dl>

 

 