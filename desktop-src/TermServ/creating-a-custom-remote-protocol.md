---
title: Création d’un fournisseur de protocole RDP (Remote Desktop Protocol)
description: Informations sur la création d’un fournisseur de protocole RDP (Remote Desktop Protocol). Le gestionnaire de protocole est implémenté en tant que serveur COM et enregistré dans un emplacement où le service Services Bureau à distance démarre.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a7905bfcc623174aca9152f0807a867112aee1a0c54976db810b87f8b3408f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856215"
---
# <a name="creating-a-remote-desktop-protocol-provider"></a>Création d’un fournisseur de protocole RDP (Remote Desktop Protocol)

Les sections suivantes contiennent des informations sur la création d’un fournisseur de protocole RDP (Remote Desktop Protocol). Le gestionnaire de protocole est implémenté en tant que serveur COM et enregistré dans un emplacement où le service Services Bureau à distance démarre.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Inscription du gestionnaire de protocole](registering-the-custom-protocol.md)
</dt> <dd>

Vous devez créer au moins une entrée de valeur de Registre pour votre gestionnaire de protocole afin que le service Services Bureau à distance puisse l’instancier.

</dd> <dt>

[Séquence d’appel de méthode](method-call-sequence.md)
</dt> <dd>

Le service Services Bureau à distance et votre fournisseur de protocole appellent l’un l’autre dans des séquences clairement définies.

</dd> </dl>

-   [Inscription du gestionnaire de protocole](registering-the-custom-protocol.md)
-   [Séquence d’appel de méthode](method-call-sequence.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API du fournisseur protocole RDP (Remote Desktop Protocol)](custom-remote-desktop-protocols.md)
</dt> <dt>

[Utilisation de Services Bureau à distance](using-terminal-services.md)
</dt> </dl>

 

 




