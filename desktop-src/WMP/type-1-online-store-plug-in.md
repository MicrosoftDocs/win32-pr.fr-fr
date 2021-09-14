---
title: Type 1 plug-in de magasin en ligne
description: Type 1 plug-in de magasin en ligne
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Lecteur Windows Media des magasins en ligne, plug-ins
- magasins en ligne, plug-ins
- types 1 magasins en ligne, plug-ins
- Lecteur Windows Media des magasins en ligne, interface IWMPContentPartner
- magasins en ligne, interface IWMPContentPartner
- types 1 magasins en ligne, interface IWMPContentPartner
- plug-ins, Lecteur Windows Media magasins en ligne
- plug-ins, magasins en ligne
- plug-ins, type 1 magasins en ligne
- plug-ins, interface IWMPContentPartner
- Lecteur Windows Media les plug-ins, tapez 1 magasins en ligne
- plug-ins Lecteur Windows Media, magasins en ligne
- plug-ins Lecteur Windows Media, Lecteur Windows Media les magasins en ligne
- plug-ins Lecteur Windows Media, interface IWMPContentPartner
- IWMPContentPartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403807"
---
# <a name="type-1-online-store-plug-in"></a>Type 1 plug-in de magasin en ligne

Pour tirer parti des fonctionnalités d’intégration de la bibliothèque, tapez 1 les fournisseurs de magasin en ligne doivent créer un plug-in qui implémente l’interface [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . cette interface fournit les méthodes qui Lecteur Windows Media appels pour notifier le magasin en ligne des activités qui se produisent dans le lecteur et pour récupérer des informations spécifiques sur le contenu du magasin en ligne, le catalogue ou le magasin lui-même.

une fois que Lecteur Windows Media a instancié le plug-in, le lecteur appelle [IWMPContentPartner :: SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)et fournit un pointeur vers l’interface **IWMPContentPartnerCallback** . cette interface donne au magasin en ligne un moyen d’effectuer des appels dans Lecteur Windows Media pour fournir des informations d’état ou pour lancer des processus spécifiques, comme le téléchargement d’une piste de musique.

Lecteur Windows Media et le plug-in s’exécutent dans des processus distincts. Le plug-in est un serveur in-process qui s’exécute dans le substitut de DLL par défaut, dllhost.exe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Interface IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[**Interface IWMPContentPartnerCallback**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




