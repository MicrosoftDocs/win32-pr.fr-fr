---
description: Comment les périphériques matériels participent au filtre Graph
ms.assetid: 27e1c097-9bb4-4f9c-b9f9-0d4225c0d290
title: Comment les périphériques matériels participent au filtre Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68794bbc046e633e9a435b2628a20b8ea8aab174
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119869"
---
# <a name="how-hardware-devices-participate-in-the-filter-graph"></a>Comment les périphériques matériels participent au filtre Graph

cet article explique comment DirectShow interagit avec le matériel audio et vidéo.

**Filtres de wrapper**

tous les filtres de DirectShow sont des composants logiciels en mode utilisateur. pour qu’un périphérique matériel en mode noyau, tel qu’une carte de capture vidéo, puisse joindre un graphique de filtre DirectShow, l’appareil doit être représenté sous la forme d’un filtre en mode utilisateur. Cette fonction est exécutée par des filtres de « wrapper » spécialisés fournis avec DirectShow. Ces filtres incluent le filtre de [capture audio](audio-capture.md) , le filtre de [capture VFW](vfw-capture-filter.md) , le filtre de [Tuner TV](tv-tuner-filter.md) , le filtre [audio TV](tv-audio-filter.md) et le filtre de barre [vidéo analogique](analog-video-crossbar-filter.md) . DirectShow fournit également un filtre appelé KsProxy, qui peut représenter n’importe quel type de périphérique de streaming Windows Driver Model (WDM). Les fournisseurs de matériel peuvent étendre KsProxy pour prendre en charge des fonctionnalités personnalisées, en fournissant un *plug-in ksproxy*, qui est un objet com agrégé par ksproxy.

Les filtres Wrapper exposent les interfaces COM qui représentent les fonctionnalités de l’appareil. L’application utilise ces interfaces pour transmettre des informations vers et depuis le filtre. Le filtre traduit les appels de méthode COM en appels de pilote de périphérique, transmet ces informations au pilote en mode noyau, puis convertit le résultat en application. Le tuner TV, l’audio TV, le distributeur vidéo analogique et les filtres KsProxy prennent en charge les propriétés de pilote personnalisées via l’interface [**IKsPropertySet**](ikspropertyset.md) . Le filtre de capture VFW et le filtre de capture audio ne sont pas extensibles de cette façon.

pour les développeurs d’applications, les filtres de wrapper permettent à l’application de contrôler les appareils tout comme ils contrôlent les autres DirectShow filtre. Aucune programmation spéciale n’est requise. les détails de la communication avec l’appareil en mode noyau sont encapsulés dans le filtre.

**vidéo pour les appareils Windows**

le filtre de capture vfw prend en charge les cartes de capture vidéo précédentes pour Windows (VFW). lorsqu’une carte VfW est présente sur le système cible, elle peut être découverte et ajoutée au graphique de filtre à l’aide de l’énumérateur de l' [appareil DirectShow système](system-device-enumerator.md). Pour plus d’informations, consultez [énumération des appareils et des filtres](enumerating-devices-and-filters.md).

**Capture audio et mixage de périphériques (cartes son)**

Les cartes son plus récentes comportent des prises jack d’entrée pour les microphones et d’autres types d’appareils. En général, ces cartes disposent également de fonctionnalités de mixage intégrées pour contrôler le volume, les aigus et les basses de chaque entrée individuelle. dans DirectShow, les entrées et le mixage de la carte audio sont encapsulés par le filtre de Capture audio. Chaque carte audio peut être détectée avec l’énumérateur du périphérique système. Pour afficher les cartes son dans votre système, exécutez GraphEdit et sélectionnez dans la catégorie sources de capture audio. Chaque filtre de cette catégorie est une instance distincte du filtre de capture audio. (Consultez [utilisation de GraphEdit](using-graphedit.md).)

**Périphériques de streaming WDM**

les décodeurs matériels et les cartes de capture les plus récents sont conformes à la spécification du Windows Driver Model (WDM). Ces appareils ont des fonctionnalités supérieures à celles des appareils VfW. Les cartes de capture vidéo WDM peuvent prendre en charge des fonctionnalités qui ne sont pas disponibles sous VfW, y compris l’énumération des formats de capture, le contrôle par programmation des paramètres vidéo tels que la teinte et la luminosité, la sélection d’entrée par programmation et la prise en charge du tuner TV.

pour prendre en charge les périphériques de streaming WDM, DirectShow fournit le filtre KsProxy (ksproxy.ax). KsProxy a été appelé « filtre pour les couteaux suisses », car il fait beaucoup de choses différentes. Le nombre de broches sur le filtre et le nombre d’interfaces COM exposées par le filtre dépendent des fonctionnalités du pilote sous-jacent. KsProxy n’apparaît pas dans le graphique de filtre sous le nom « KsProxy ». Il prend toujours le nom convivial de l’appareil, qui se trouve dans le registre. Pour afficher les périphériques WDM sur votre système, exécutez GraphEdit et sélectionnez dans les catégories de streaming WDM. Même si votre système ne possède qu’une seule carte WDM, cette carte peut contenir plusieurs appareils. Chaque appareil est représenté sous la forme d’un filtre distinct, et chacun de ces filtres est en fait KsProxy.

Une application utilise l’énumérateur de périphérique système pour rechercher des monikers de périphérique WDM sur le système. KsProxy est instancié en appelant **BindToObject** sur le moniker. Comme KsProxy peut représenter tous les types d’appareils WDM, il doit interroger le pilote pour déterminer les jeux de propriétés que le pilote prend en charge. Les jeux de propriétés sont des collections de structures de données utilisées par les pilotes WDM, ainsi que par certains filtres en mode utilisateur, tels que les décodeurs logiciels MPEG-2. KsProxy configure lui-même pour exposer les interfaces COM qui correspondent à ces jeux de propriétés. KsProxy convertit les appels de méthode COM en jeux de propriétés et les envoie au pilote. Les fournisseurs de matériel peuvent étendre KsProxy en fournissant des plug-ins, qui sont des interfaces spécifiques au fournisseur qui exposent les fonctionnalités spéciales d’un appareil. Tous ces détails sont masqués dans l’application. l’application contrôle l’appareil par le biais de KsProxy, de la même façon que n’importe quel autre filtre de DirectShow.

**Streaming de noyau**

Les périphériques WDM prennent en charge la diffusion en continu de noyau, dans laquelle les données sont entièrement diffusées en mode noyau, sans jamais passer en mode utilisateur. Le basculement entre le mode noyau et le mode utilisateur est gourmand en ressources informatiques. le streaming de noyau permet des vitesses de transmission élevées sans nécessiter le processeur de l’ordinateur hôte. Les filtres WDM peuvent utiliser la diffusion en continu du noyau pour transmettre des données multimédias directement d’un périphérique matériel à un autre, sur la même carte ou sur une autre carte, sans copier les données dans la mémoire principale du système.

Du point de vue d’une application, elle apparaît comme si les données se déplacent d’un filtre en mode utilisateur à la suivante. En réalité, les données risquent de ne jamais passer en mode utilisateur, mais elles peuvent être transmises directement d’un appareil en mode noyau à un autre jusqu’à ce qu’elles soient rendues sur la carte vidéo. Certains scénarios, tels que la capture dans un fichier, requièrent que les données passent du mode noyau au mode utilisateur à un moment donné. Toutefois, ce commutateur ne requiert pas nécessairement la copie des données vers un nouvel emplacement en mémoire.

Les développeurs d’applications n’ont généralement pas besoin de se préoccuper des détails de la diffusion en continu du noyau, à l’exception des informations d’arrière-plan. Consultez Microsoft DDK pour obtenir des informations plus détaillées sur WDM, Kernel streaming, KsProxy et les rubriques connexes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[le filtre Graph et ses composants](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



