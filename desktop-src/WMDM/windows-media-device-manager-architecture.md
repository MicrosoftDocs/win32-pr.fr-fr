---
title: Windows Architecture du Gestionnaire de périphériques multimédia
description: Windows Architecture du Gestionnaire de périphériques multimédia
ms.assetid: 3c1b2da4-559d-427b-b502-5ef8dc055a8e
keywords:
- Windows Gestionnaire de périphériques de média, architecture
- Gestionnaire de périphériques, architecture
- architecture pour Windows Media Gestionnaire de périphériques
- Windows Gestionnaire de périphériques de média, applications de bureau
- Gestionnaire de périphériques, applications de bureau
- Windows Gestionnaire de périphériques de support, fournisseurs de services
- Gestionnaire de périphériques, fournisseurs de services
- Windows Gestionnaire de périphériques de média, plug-ins
- Gestionnaire de périphériques, plug-ins
- applications de bureau, Windows Gestionnaire de périphériques architecture multimédia
- fournisseurs de services, architecture du Gestionnaire de périphériques Windows Media
- plug-ins, Windows Gestionnaire de périphériques architecture multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fda87e4ed4bce2c82bbb9c0863c119851965940
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192811"
---
# <a name="windows-media-device-manager-architecture"></a>Windows Architecture du Gestionnaire de périphériques multimédia

Windows Le Gestionnaire de périphériques de média permet à une application ou à un plug-in de communiquer avec un appareil. Les applications peuvent demander des métadonnées d’appareil, énumérer et explorer des appareils attachés, et envoyer ou recevoir des objets (dossiers, fichiers, sélections, etc.). Windows Media Gestionnaire de périphériques fournit une API unique à l’application appelante, quel que soit le type d’appareil appelé (classe MTP ou Stockage de masse, fournisseurs de services basés sur la version 10 ou les fournisseurs de services basés sur des versions antérieures de Windows Media Gestionnaire de périphériques).

Windows Media Gestionnaire de périphériques agit comme un passage pour les trois principaux composants du système : l’application, qui effectue des demandes (pour des informations, pour lire ou écrire des données, etc.); un fournisseur de contenu sécurisé, qui est un composant qui gère les communications avec les fichiers protégés par DRM ; et un fournisseur de services, qui reçoit les demandes de l’application et communique avec l’appareil pour effectuer ces requêtes. l’application et le fournisseur de services sont basés sur le kit de développement logiciel (SDK) Gestionnaire de périphériques Windows Media.

le diagramme suivant montre comment une application de bureau communique avec un appareil à l’aide de Windows média Gestionnaire de périphériques 11.

![Diagramme montrant une application communiquant avec quatre types différents d’appareils.](images/wmdm-device-communication.gif)

Le diagramme précédent illustre une application communiquant avec quatre types différents d’appareils, chacun avec son propre fournisseur de services. Chaque fournisseur de services est conçu pour communiquer avec un type spécifique d’appareil. ce diagramme illustre les trois fournisseurs de services fournis par Microsoft (pilotes de classes génériques pour les appareils de classe de masse Stockage, les périphériques RAPI et les appareils MTP), ainsi qu’un fournisseur de services personnalisé pour un appareil propriétaire créé par un tiers. quand un appareil se connecte, Windows Media Gestionnaire de périphériques instancie une instance du fournisseur de services inscrite pour cet appareil. les fournisseurs de services obtiennent des requêtes à partir de l’application par le biais d’Windows interfaces de Gestionnaire de périphériques de média qu’ils implémentent, utilisent des pilotes appropriés pour communiquer avec l’appareil et renvoient les résultats appropriés. la Communication entre le fournisseur de services et l’appareil se trouve en dehors du domaine de Windows Gestionnaire de périphériques de média.

Les fournisseurs de services sont invisibles pour l’application ; une application ne voit qu’une liste de « périphériques », car Windows Media Gestionnaire de périphériques expose un ensemble standard de méthodes et d’interfaces pour tous les appareils. si un fabricant crée un fournisseur de services personnalisé, il doit gérer toutes les méthodes de Gestionnaire de périphériques de support Windows standard si les applications doivent être en mesure d’utiliser l’appareil.

Ce diagramme montre également un module SCP (Secure Content Provider). Ce module est responsable de la gestion du contenu protégé par la gestion des droits numériques (DRM). Microsoft fournit un module SCP qui peut gérer des fichiers WMA et WMV protégés par DRM. Si une application ou un appareil envisage de gérer d’autres formats protégés, elle doit fournir son propre module SCP. L’application et le fournisseur de services ne traitent pas directement le SCP.

l’application et le fournisseur de services reposent sur Windows Gestionnaire de périphériques multimédia, qui achemine les appels entre l’application et le fournisseur de services approprié pour un appareil. le fournisseur de services est responsable de la communication directe avec l’appareil. Windows Media Gestionnaire de périphériques effectue certaines actions, telles que l’énumération des appareils connectés, le routage des appels et la vérification des composants. Toutefois, la majeure partie du travail est effectuée par le fournisseur de services, qui reçoit les demandes de l’application et communique avec l’appareil.

une application basée sur Windows media Gestionnaire de périphériques peut communiquer avec des appareils et des fournisseurs de services basés sur des versions antérieures de Windows Gestionnaire de périphériques de média. Toutefois, ces appareils plus anciens seront exécutés jusqu’à la série de 9 composants (non illustrés) et ne prendront pas en charge les fonctionnalités les plus récentes, en particulier la technologie de gestion des droits numériques plus avancée.

Architecture d’un appareil

le diagramme suivant montre une hiérarchie simplifiée d’appareils et de stockage, telle qu’elle est vue par une application qui utilise Windows Gestionnaire de périphériques de média.

![Diagramme montrant les stockages sur un appareil.](images/wmdm-basic-device-layout.gif)

le diagramme précédent illustre une version simplifiée d’un lecteur flash connecté, tel qu’il est vu par une application de Gestionnaire de périphériques multimédia Windows. Le lecteur flash possède des attributs et des propriétés, tels qu’un numéro de série et des configurations de format prises en charge. Un enfant immédiat du périphérique flash est l’objet de stockage racine, qui contient un dossier, qui contient lui-même une image et une chanson.

Une application énumère la liste des périphériques attachés en appelant une méthode d’énumération exposée par l’interface [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) racine. Les appareils sont représentés par une interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) (ou dérivée). Cette interface expose des méthodes pour récupérer le nom de l’appareil, les fonctionnalités de format, le numéro de série, etc., ainsi qu’une méthode qui énumère les *stockages* sur l’appareil. dans Windows Gestionnaire de périphériques de média, un stockage est tout type d’objet sur l’appareil, qu’il s’agisse ou non d’un blob de données réel. Par exemple : les fichiers audio, les fichiers texte, les dossiers, les sélections stockés en tant que fichiers et les sélections stockées en tant que métadonnées sont tous considérés comme des stockages, même si les dossiers et les éléments de métadonnées ne représentent probablement pas un fichier physique. Le type (ou le format) d’un stockage peut être récupéré en appelant [**GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) (ou [**GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata), en demandant le format du stockage).

Les stockages sur un appareil sont stockés hiérarchiquement et tous les appareils ont un stockage racine. Chaque stockage peut contenir zéro ou plusieurs objets enfants, énumérés en appelant la méthode [**IWMDMStorage :: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) de ce stockage.

Notez que chaque stockage dans le diagramme possède des attributs et des métadonnées qui lui sont associés (toutes les valeurs ne sont pas affichées). Les attributs sont des informations booléennes simples qui décrivent souvent des informations de gestion ou de navigation (telles que « has Folders » ou « Delete »), tandis que les métadonnées peuvent être des valeurs de chaîne, des nombres ou des informations complexes (telles que des fonctionnalités de rendu). Les attributs sont décrits par un ensemble d’indicateurs assez limité défini par le kit de développement logiciel (SDK) et récupérés par l’appel de [**IWMDMStorage :: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) ou [**IWMDMStorage2 :: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2). Les valeurs de métadonnées sont extraites par un nom unique ; le kit de développement logiciel (SDK) définit un certain nombre de valeurs de métadonnées que les appareils doivent prendre en charge, mais les appareils peuvent définir leurs propres [constantes de métadonnées](metadata-constants.md). Toutefois, si un appareil ou un fournisseur de services définit une nouvelle constante de métadonnées, les applications ne sont pas en mesure de demander ou de définir cette valeur, sauf si les développeurs d’applications ont pris connaissance de cette nouvelle constante. Un fournisseur de services doit prendre en charge [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) ou version ultérieure pour prendre en charge la récupération ou la définition des métadonnées. Pour plus d’informations, consultez [obtention et définition des métadonnées et des attributs](getting-and-setting-metadata-and-attributes.md).

Fournisseurs de services

Le fournisseur de services joue le rôle d’intermédiaire entre l’application et l’appareil. Le fournisseur de services est invisible pour le développeur de l’application, de sorte qu’un développeur d’applications n’a pas besoin de tout savoir sur le développement d’un fournisseur de services. Toutefois, il s’agit du fournisseur de services qui effectue le travail de communication avec un appareil.

un fournisseur de services est une DLL COM reposant sur Windows Media Gestionnaire de périphériques qui reçoit les demandes d’une application et communique avec l’appareil pour les exécuter. la Communication avec l’application de bureau est conforme à Windows Media Gestionnaire de périphériques ; la communication avec l’appareil est sous le contrôle du fournisseur de services.

Un fournisseur de services reçoit les demandes de l’application pour énumérer le contenu de l’appareil, les demandes de fonctionnalités de l’appareil, les demandes de lecture ou d’écriture de données, etc. Il doit connaître la conception d’un appareil suffisamment bien qu’il puisse envoyer des commandes dans le format et le protocole appropriés. Il doit également être en mesure de masquer les exigences spécifiques aux appareils, telles qu’une extension de fichier requise pour les sélections, afin que les applications n’aient pas besoin de connaître ces exigences pour pouvoir utiliser l’appareil.

Microsoft fournit un certain nombre de fournisseurs de services pour les types d’appareils standard, notamment les appareils MTP génériques, les appareils de classe Stockage de masse et les appareils RAPI. La seule raison pour laquelle un concepteur d’appareils doit créer un fournisseur de services personnalisé est si un appareil a des exigences de stockage de données spécifiques ou inhabituelles qui ne sont pas gérées par les fournisseurs de services standard (par exemple, si les fichiers doivent être stockés dans des emplacements spécifiques et que le système d’exploitation de l’appareil ne les gère pas automatiquement).

quand un appareil est connecté à l’ordinateur, le système d’exploitation crée une instance du fournisseur de services approprié pour chaque application Windows Media Gestionnaire de périphériques. si une deuxième Windows Media Gestionnaire de périphériques application démarre, une deuxième instance du fournisseur de services est chargée. Toutefois, chaque fournisseur de services peut gérer plusieurs appareils. Le diagramme suivant illustre ce point.

![Diagramme montrant deux appareils MTP communiquant avec deux applications.](images/wmdm-sp-to-device.gif)

Le diagramme précédent montre deux applications différentes communiquant avec deux appareils MTP. Les appareils utilisent la même classe de fournisseur de service, mais chaque application possède sa propre instance du même fournisseur de services. Chaque instance du fournisseur de services communique avec les appareils. Les différentes instances du fournisseur de services ne sont pas conscientes les unes des autres.

De nombreuses méthodes d’application ont une méthode de fournisseur de service nommée correspondante. lorsque l’application appelle une méthode, Windows média Gestionnaire de périphériques achemine l’appel vers la méthode correspondante sur le fournisseur de services (bien qu’il puisse d’abord effectuer des actions internes supplémentaires). par exemple, quand l’application appelle [**IWMDMDevice3 :: getproperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty), Windows média Gestionnaire de périphériques achemine cet appel à l’implémentation du fournisseur de services de [**IMDSPDevice3 :: getproperty**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-getproperty). (La plupart des interfaces d’application commencent par IWMDM, et l’interface du fournisseur de services correspondante commence par IMDSP). Le fournisseur de services est censé gérer cet appel de méthode et retourner un résultat approprié.

Une application n’explore jamais ou ne communique pas directement avec un appareil (sauf si elle appelle [**IWMDMDevice3 ::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) ou [**IWMDMStorage :: SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)); l’application communique avec le fournisseur de services, qui doit représenter un appareil de la manière la plus logique et la plus simple possible. Lorsque l’application demande des informations sur l’appareil ou énumère des objets sur l’appareil, le fournisseur de services interroge l’appareil de manière appropriée et acquiert et retourne les informations appropriées. Il peut exposer l’Organisation des fichiers sur l’appareil différemment de la façon dont il est stocké physiquement sur l’appareil, si cela est approprié. Toutefois, il expose l’appareil, il doit être de manière cohérente et logique, afin de permettre à l’application de trouver ce dont elle a besoin et de gérer les commandes qu’elle envoie. Un bon fournisseur de services masquera les particularités propres à l’appareil : par exemple, si l’appareil stocke physiquement une sélection dans un fichier avec une extension de fichier personnalisée, le fournisseur de services doit ajouter cette extension automatiquement quand l’application crée une sélection sur l’appareil. il ne doit pas s’attendre à ce que l’application connaisse l’extension appropriée lors de la création d’un objet playlist.

Les fournisseurs de services s’exécutent dans le processus de l’application appelante. La seule exception est le fournisseur de services MTP, qui s’exécute dans son propre processus. Pour cette raison, il existe un risque qu’un fournisseur de services bloqué entraîne le blocage de l’application appelante. Par conséquent, les fournisseurs de services doivent être conçus pour être robustes et empêcher le blocage, et les applications doivent être conçues pour éviter les blocages si un appel de méthode particulier ne retourne pas rapidement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Prise en main**](getting-started.md)
</dt> </dl>

 

 




