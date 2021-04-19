---
title: Création d’un fournisseur de protocole RDP (Remote Desktop Protocol)
description: Informations sur la création d’un fournisseur de protocole RDP (Remote Desktop Protocol). Le gestionnaire de protocole est implémenté en tant que serveur COM et enregistré dans un emplacement où le service Services Bureau à distance démarre.
ms.assetid: 9a3e6d5c-464f-4227-a06f-16eb8ed1079e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41265a350b4d5c559731a09abc21aa4c81b9b29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510182"
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

 

 




