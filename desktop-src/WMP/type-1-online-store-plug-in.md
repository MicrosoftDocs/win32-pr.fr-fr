---
title: Type 1 plug-in de magasin en ligne
description: Type 1 plug-in de magasin en ligne
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Windows Media Player Online stores, plug-ins
- magasins en ligne, plug-ins
- types 1 magasins en ligne, plug-ins
- Windows Media Player Online stores, interface IWMPContentPartner
- magasins en ligne, interface IWMPContentPartner
- types 1 magasins en ligne, interface IWMPContentPartner
- plug-ins, Windows Media Player Online stores
- plug-ins, magasins en ligne
- plug-ins, type 1 magasins en ligne
- plug-ins, interface IWMPContentPartner
- Plug-ins du lecteur Windows Media, type 1 magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne Windows Media Player
- Plug-ins du lecteur Windows Media, interface IWMPContentPartner
- IWMPContentPartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104030940"
---
# <a name="type-1-online-store-plug-in"></a>Type 1 plug-in de magasin en ligne

Pour tirer parti des fonctionnalités d’intégration de la bibliothèque, tapez 1 les fournisseurs de magasin en ligne doivent créer un plug-in qui implémente l’interface [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . Cette interface fournit les méthodes appelées par le lecteur Windows Media pour informer le magasin en ligne sur les activités qui ont lieu dans le lecteur et pour récupérer des informations spécifiques sur le contenu du magasin en ligne, le catalogue ou le magasin lui-même.

Une fois que le lecteur Windows Media a instancié le plug-in, le lecteur appelle [IWMPContentPartner :: SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)et fournit un pointeur vers l’interface **IWMPContentPartnerCallback** . Cette interface permet à la Banque en ligne d’effectuer des appels au lecteur Windows Media pour fournir des informations d’État ou pour lancer des processus spécifiques, tels que le téléchargement d’une piste de musique.

Le lecteur Windows Media et le plug-in s’exécutent dans des processus distincts. Le plug-in est un serveur in-process qui s’exécute dans le substitut de DLL par défaut, dllhost.exe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Interface IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[**Interface IWMPContentPartnerCallback**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




