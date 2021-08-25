---
title: À propos de la synchronisation des sélections
description: À propos de la synchronisation des sélections
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Lecteur Windows Media, synchronisation des sélections
- Lecteur Windows Media modèle objet, synchronisation de playlists
- modèle objet, synchronisation des sélections
- contrôle de ActiveX Lecteur Windows Media, synchronisation des sélections
- contrôle de ActiveX, synchronisation des sélections
- Lecteur Windows Media contrôle Mobile ActiveX, synchronisation des sélections
- Lecteur Windows Media Mobile, synchronisation de playlists
- synchronisation des appareils, des sélections
- synchronisation des appareils, sélections
- sélections, synchronisation
- Windows Sélections de métafichiers multimédia, synchronisation
- sélections de métafichiers, synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe54bef188fea2baee64da962dabf4eb8f700b72407772d591d73f52be2d4289
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956869"
---
# <a name="about-playlist-synchronization"></a>À propos de la synchronisation des sélections

Lecteur Windows Media 10 ou version ultérieure est conçu pour synchroniser le contenu multimédia numérique sur des appareils à l’aide d’un modèle de synchronisation de sélection. Cela signifie que le contenu destiné à être copié sur un appareil doit faire partie d’une sélection. lorsque l’utilisateur choisit de transférer le contenu multimédia numérique individuel de son ordinateur vers un appareil, Lecteur Windows Media ajoute le contenu à une sélection par défaut pour la copie.

les api de synchronisation des appareils Lecteur Windows Media sont également conçues pour fonctionner de la même manière. comme Lecteur Windows Media, votre programme peut présenter à l’utilisateur une liste de sélections qu’il a définies. Vous pouvez ensuite permettre à l’utilisateur de choisir les playlists à synchroniser avec un périphérique particulier et de définir l’ordre de priorité pour le processus de synchronisation.

Étant donné que les appareils mobiles ont une capacité de stockage limitée, il est possible pour l’utilisateur de choisir de synchroniser plus de contenu multimédia numérique que l’appareil peut stocker. Lecteur Windows Media synchronise le contenu par ordre de priorité. L’utilisateur peut définir l’ordre de priorité à l’aide d’une boîte de dialogue à laquelle vous pouvez accéder à partir de la fonctionnalité **appareils** . En réponse à l’entrée utilisateur de votre programme, vous pouvez modifier l’ordre de priorité par programmation en modifiant les valeurs de certains attributs de sélection. Collectivement, ces attributs sont appelés attributs de *synchronisation* .

Chaque playlist d’une bibliothèque a 16 attributs de synchronisation : **Sync01** à **Sync16**. Chaque attribut représente l’appareil qui a l’index de partenariat correspondant. La valeur de chaque attribut vous indique deux choses :

-   Indique si la sélection doit être synchronisée avec l’appareil.
-   Valeur de priorité pour la sélection.

la valeur zéro indique que Lecteur Windows Media ne doit pas tenter de synchroniser la playlist avec l’appareil. Toute autre valeur est un numéro de priorité. Les valeurs inférieures reçoivent une priorité plus élevée au moment de la synchronisation.

Les sélections ont également un attribut **SyncOnly** qui indique si la sélection est disponible uniquement pour la synchronisation.

Les éléments individuels du contenu multimédia numérique contiennent également des métadonnées sur la synchronisation. Lorsque vous récupérez un objet **média** à partir de la bibliothèque, vous pouvez inspecter la valeur de l’attribut **SyncState** . Cet attribut fournit des informations étendues indiquant si le contenu a été correctement copié sur l’appareil ou si la copie du contenu a échoué en raison de l’impossibilité de le faire.

> [!Note]  
> Vous devez éviter de fournir des éléments d’interface utilisateur qui permettent à l’utilisateur de créer des listes de lecture à partir de tout le contenu de la bibliothèque pour la synchronisation.

 

pour optimiser les performances, Lecteur Windows Media applique un ensemble de règles pour la création de sélections de synchronisation. Votre programme doit uniquement créer des sélections de synchronisation pour le contenu que vous avez fourni. autoriser Lecteur Windows Media à créer des sélections de synchronisation pour le contenu que l’utilisateur a ajouté à la bibliothèque à partir d’autres sources.

Au lieu de créer votre propre interface utilisateur de sélection, vous pouvez présenter aux utilisateurs une boîte de dialogue par défaut pour choisir des sélections et gérer le partenariat pour un appareil. Pour ce faire, appelez [IWMPSyncDevice :: showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings). quand vous appelez cette méthode, Lecteur Windows Media affiche sa boîte de dialogue paramètres de synchronisation. lorsque l’utilisateur ferme la boîte de dialogue, Lecteur Windows Media revient automatiquement à son état d’ancrage antérieur et passe le contrôle à votre programme distant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos de la synchronisation des appareils**](about-device-synchronization.md)
</dt> <dt>

[**Gestion des sélections de synchronisation**](managing-synchronization-playlists.md)
</dt> <dt>

[**Attributs de sélection**](playlist-attributes.md)
</dt> </dl>

 

 




