---
title: Création du plug-in pour un magasin de type 1 en ligne
description: Création du plug-in pour un magasin de type 1 en ligne
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Windows Media Player Online stores, plug-ins
- magasins en ligne, plug-ins
- types 1 magasins en ligne, plug-ins
- Windows Media Player Online stores, création de plug-ins
- magasins en ligne, création de plug-ins
- types 1 magasins en ligne, création de plug-ins
- Windows Media Player Online stores, interface IWMPContentPartner
- magasins en ligne, interface IWMPContentPartner
- types 1 magasins en ligne, interface IWMPContentPartner
- plug-ins, Windows Media Player Online stores
- plug-ins, magasins en ligne
- plug-ins, type 1 magasins en ligne
- plug-ins, interface IWMPContentPartner
- plug-ins, génération
- Plug-ins du lecteur Windows Media, type 1 magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne Windows Media Player
- Plug-ins du lecteur Windows Media, interface IWMPContentPartner
- Plug-ins du lecteur Windows Media, génération
- IWMPContentPartner
- génération de plug-ins, tapez 1 magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36272e3497eebc7b5362d793a0ee265d2c3166fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106512084"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a>Création du plug-in pour un magasin de type 1 en ligne

Un magasin en ligne de type 1 doit fournir un plug-in qui implémente l’interface [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . Le plug-in s’exécute dans un processus distinct à partir du lecteur Windows Media.

Les étapes de création d’un plug-in qui s’exécute hors processus sont les suivantes :

1.  Écrivez votre plug-in comme s’il s’agissait d’un serveur COM in-process.
2.  Créez une entrée de Registre **DllSurrogate** sur l’ordinateur de l’utilisateur. L’entrée **DllSurrogate** informe le runtime com que votre plug-in doit être créé dans une instance du substitut de la dll par défaut, dllhost.exe.

Pour plus d’informations sur l’enregistrement de votre plug-in, consultez [clés et entrées de Registre pour un magasin de type 1 en ligne](registry-keys-and-entries-for-a-type-1-online-store.md).

Vous n’avez pas besoin de créer de code proxy ou stub pour votre plug-in. L’ensemble de la prise en charge du marshaling est fourni par le lecteur Windows Media.

Vous pouvez utiliser l’Assistant de plug-in de magasin en ligne pour créer rapidement un plug-in qui sert de point de départ. Pour plus d’informations, consultez [installation de l’Assistant de plug-in de boutique en ligne](installing-the-online-store-plug-in-wizard.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation pour les magasins de type 1 en ligne**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




