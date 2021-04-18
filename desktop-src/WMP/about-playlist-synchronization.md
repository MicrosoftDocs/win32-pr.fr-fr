---
title: À propos de la synchronisation des sélections
description: À propos de la synchronisation des sélections
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Lecteur Windows Media, synchronisation des sélections
- Modèle objet du lecteur Windows Media, synchronisation des sélections
- modèle objet, synchronisation des sélections
- Contrôle ActiveX du lecteur Windows Media, synchronisation des sélections
- Contrôle ActiveX, synchronisation des sélections
- Contrôle ActiveX Windows Media Player Mobile, synchronisation des sélections
- Lecteur Windows Media Mobile, synchronisation des sélections
- synchronisation des appareils, des sélections
- synchronisation des appareils, sélections
- sélections, synchronisation
- Sélections de métafichiers Windows Media, synchronisation
- sélections de métafichiers, synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc019b31518fda1a49c8d3ae86f2d03c4ecefc8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314245"
---
# <a name="about-playlist-synchronization"></a>À propos de la synchronisation des sélections

Le lecteur Windows Media 10 (ou version ultérieure) est conçu pour synchroniser le contenu multimédia numérique sur des appareils à l’aide d’un modèle de synchronisation de sélection. Cela signifie que le contenu destiné à être copié sur un appareil doit faire partie d’une sélection. Lorsque l’utilisateur choisit de transférer le contenu multimédia numérique individuel de son ordinateur vers un appareil, le lecteur Windows Media ajoute le contenu à une sélection par défaut pour la copie.

Les API de synchronisation des périphériques du lecteur Windows Media sont également conçues pour fonctionner de la même manière. À l’instar de Windows Media Player, votre programme peut présenter à l’utilisateur une liste de sélections qu’il a définies. Vous pouvez ensuite permettre à l’utilisateur de choisir les playlists à synchroniser avec un périphérique particulier et de définir l’ordre de priorité pour le processus de synchronisation.

Étant donné que les appareils mobiles ont une capacité de stockage limitée, il est possible pour l’utilisateur de choisir de synchroniser plus de contenu multimédia numérique que l’appareil peut stocker. Le lecteur Windows Media synchronise le contenu par ordre de priorité. L’utilisateur peut définir l’ordre de priorité à l’aide d’une boîte de dialogue à laquelle vous pouvez accéder à partir de la fonctionnalité **appareils** . En réponse à l’entrée utilisateur de votre programme, vous pouvez modifier l’ordre de priorité par programmation en modifiant les valeurs de certains attributs de sélection. Collectivement, ces attributs sont appelés attributs de *synchronisation* .

Chaque playlist d’une bibliothèque a 16 attributs de synchronisation : **Sync01** à **Sync16**. Chaque attribut représente l’appareil qui a l’index de partenariat correspondant. La valeur de chaque attribut vous indique deux choses :

-   Indique si la sélection doit être synchronisée avec l’appareil.
-   Valeur de priorité pour la sélection.

La valeur zéro indique que le lecteur Windows Media ne doit pas tenter de synchroniser la playlist avec l’appareil. Toute autre valeur est un numéro de priorité. Les valeurs inférieures reçoivent une priorité plus élevée au moment de la synchronisation.

Les sélections ont également un attribut **SyncOnly** qui indique si la sélection est disponible uniquement pour la synchronisation.

Les éléments individuels du contenu multimédia numérique contiennent également des métadonnées sur la synchronisation. Lorsque vous récupérez un objet **média** à partir de la bibliothèque, vous pouvez inspecter la valeur de l’attribut **SyncState** . Cet attribut fournit des informations étendues indiquant si le contenu a été correctement copié sur l’appareil ou si la copie du contenu a échoué en raison de l’impossibilité de le faire.

> [!Note]  
> Vous devez éviter de fournir des éléments d’interface utilisateur qui permettent à l’utilisateur de créer des listes de lecture à partir de tout le contenu de la bibliothèque pour la synchronisation.

 

Pour optimiser les performances, le lecteur Windows Media met en œuvre un ensemble de règles pour la création de sélections de synchronisation. Votre programme doit uniquement créer des sélections de synchronisation pour le contenu que vous avez fourni. Autoriser le lecteur Windows Media à créer des sélections de synchronisation pour le contenu que l’utilisateur a ajouté à la bibliothèque à partir d’autres sources.

Au lieu de créer votre propre interface utilisateur de sélection, vous pouvez présenter aux utilisateurs une boîte de dialogue par défaut pour choisir des sélections et gérer le partenariat pour un appareil. Pour ce faire, appelez [IWMPSyncDevice :: showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings). Lorsque vous appelez cette méthode, le lecteur Windows Media affiche la boîte de dialogue Paramètres de synchronisation. Lorsque l’utilisateur ferme la boîte de dialogue, le lecteur Windows Media revient automatiquement à son état d’ancrage antérieur et transmet le contrôle à votre programme distant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos de la synchronisation des appareils**](about-device-synchronization.md)
</dt> <dt>

[**Gestion des sélections de synchronisation**](managing-synchronization-playlists.md)
</dt> <dt>

[**Attributs de sélection**](playlist-attributes.md)
</dt> </dl>

 

 




