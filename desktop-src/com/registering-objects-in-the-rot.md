---
title: Inscription d’objets dans le ROT
description: Inscription d’objets dans le ROT
ms.assetid: f479c2d1-0c55-4281-8f15-2f957fa03b70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b452ead94a717791910ecceaa5082535bc1b233c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379991"
---
# <a name="registering-objects-in-the-rot"></a>Inscription d’objets dans le ROT

En général, lorsqu’un client demande à un serveur de créer une instance d’objet, le serveur crée généralement un moniker pour l’objet et l’inscrit dans la table ROT (Running Object Table) par le biais d’un appel à [**IRunningObjectTable :: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register).

Lorsque le serveur appelle [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) pour créer un moniker de fichier à enregistrer dans la table ROT, les serveurs doivent transmettre les noms de fichiers locaux qui sont basés sur un lecteur, et non au format UNC. Cela permet de s’assurer que les données de comparaison du moniker générées par l’appel du Registre ROT correspondent à ce qui est utilisé lors d’une recherche de table ROT sur la partie d’un client distant. En effet, lorsque le service COM distribué reçoit une demande d’activation pour un fichier local sur le serveur à partir d’un client distant, le fichier est converti en chemin d’accès basé sur un lecteur local.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Installation d’une application en tant que service](installing-as-a-service-application.md)
</dt> <dt>

[Inscription d’une classe lors de l’installation](registering-a-class-at-installation.md)
</dt> <dt>

[Inscription d’un serveur exécutable en cours d’exécution](registering-a-running-exe-server.md)
</dt> <dt>

[Inscription automatique](self-registration.md)
</dt> </dl>

 

 




