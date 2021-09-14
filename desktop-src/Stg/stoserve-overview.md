---
title: Présentation de StoServe
description: l’exemple de code StoServe montre comment utiliser les services Stockage structurés fournis dans l’implémentation des fichiers composés. L’utilisation des interfaces IStorage et IStream standard est décrite.
ms.assetid: 41ccd333-15c8-46b2-91c6-3e1929f7198c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0c8325fbc20d4917785d0b83ca70bffa996824
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095806"
---
# <a name="stoserve-overview"></a>Présentation de StoServe

## <a name="purpose"></a>Objectif

l’objectif principal de cet exemple de code est l’utilisation de services Stockage structurés fournis dans l’implémentation des fichiers composés. L’utilisation des interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) et [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) standard est décrite. **StoServe** fonctionne avec l’exemple de code [StoClien](structured-storage-client-sample--stoclien-.md) pour illustrer l’utilisation conjointe du stockage de fichiers composés par le client et le serveur.

## <a name="functionality"></a>Fonctionnalité

L’exemple **StoServe** présente l’objet com de l’en-papiers, qui représente virtuellement une feuille vierge de papier.

Les objets de copapier exposent un ensemble de caractéristiques pour le dessin libre sur l’aire de papier en utilisant l’entrée manuscrite de la couleur et de la largeur spécifiées. La fonctionnalité est semblable aux exemples de didacticiels « Scribble » dans de nombreuses versions de Microsoft Visual C++. La différence dans les exemples **StoServe** / **StoClien** est basée sur l’architecture, principalement sur la technologie com. Les fonctionnalités de papier de dessin électronique des objets de codocumentations sont disponibles pour les clients via une interface [**IPaper**](ipaper-methods.md) personnalisée. Le « codocument » implémente l’interface **IPaper** . Une distinction architecturale claire est conservée entre le client et le serveur. Aucune interface graphique utilisateur n’est fournie par le colivre. La conception de l’objet codocument s’appuie sur le client pour tous les comportements de l’interface graphique. Le coarticle encapsule uniquement la capture et le stockage des données d’encre dessinées sur le serveur.

Les données d’encre qui sont dessinées sur la surface du copapier peuvent être stockées dans et chargées à partir de fichiers composés. Les méthodes [**IPaper**](ipaper-methods.md), [**Save**](ipaper--save.md) et [**Load**](ipaper--load.md) acceptent un pointeur d’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Le coarticle utilise cette interface **IStorage** fournie par le client pour stocker les données de dessin.

Le coarticle est hébergé dans un serveur in-process et devient public en tant que composant COM personnalisé. Comme pour les autres serveurs de cette série de didacticiels, StoServe est un serveur COM à inscription automatique. Cela rend le type d’objet de l’élément de rapport disponible pour les clients en tant que composant DllPaper à l’aide \_ d’une inscription DLLPAPER CLSID dans le registre.

Comme dans le serveur d’ancienneté précédent, les fonctionnalités de l’objet connectable sont prises en charge dans le codocument. L’interface [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) est exposée et un point de connexion approprié est implémenté. Dans ce contexte, une interface IPaperSink personnalisée sortante est déclarée pour être utilisée lors de l’envoi de notifications au client.

Les deux interfaces personnalisées [**IPaper**](ipaper-methods.md) et [**IPaperSink**](ipapersink-methods.md) sont déclarées dans IPaper. H situé dans le répertoire Common frère \\ Inc. Les GUID pour les interfaces et les objets sont définis dans PAPGUIDS. H situé dans ce même répertoire include commun.

La fonctionnalité CThreaded dans APPUTIL est utilisée par **StoServe** pour assurer la sécurité des threads, comme c’était le cas dans l’exemple FRESERVE. Les objets de copapier sont dérivés de la classe CThreaded et héritent de ses méthodes OwnThis et UnOwnThis. Ces méthodes n’autorisent qu’un seul thread à la fois à accéder au serveur **StoServe** et aux objets coimprimés gérés par le serveur.

## <a name="copaper-com-object"></a>Objet COM de l’article

L’objet COM de l’en-papiers est le type d’objet unique géré par ce serveur in-process **StoServe** . Le coarticle est construit comme un objet COM connectable avec une implémentation de l’interface [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) standard et une implémentation de l’interface [**IPaper**](ipaper-methods.md) personnalisée. Le présentateur expose l’interface **IPaper** afin que les clients puissent exécuter un petit ensemble d’opérations de papier électronique sur une instance du copapier. Les opérations essentielles démarrent une séquence de dessin d’encre, dessinent les données d’encre sur l’aire de papier virtuel du copapier et terminent la séquence de dessin de l’encre. Dans ce schéma, le client est supposé être une application GUI pilotée par une souris ou un périphérique tablette. Le client est responsable de la conversion des mouvements de la souris en demandes en codocument, ce qui permet d’enregistrer ces demandes sous forme de données manuscrites.

Il existe deux niveaux de sauvegarde des données manuscrites dans le codocument. Le codocument enregistre les données d’encre dans un tableau basé sur la mémoire RAM qui représente le dessin actuel, et le colivre enregistre de manière permanente un dessin entier dans un fichier composé. Les méthodes de l’interface [**IPaper**](ipaper-methods.md) effectuent les deux.

Étant donné que le client ne gère pas les données papier dessinées, mais qu’il est chargé de le rendre en tant qu’image à l’écran, l’implémentation [**IPaper**](ipaper-methods.md) dans le codocument doit exposer une méthode qui permet au client d’obtenir les données de dessin. La technologie d’objets connectable dans le coarticle est utilisée à cette fin. Un \_ point de connexion CONNPOINT PAPERSINK est implémenté par le colivre afin qu’un client puisse se connecter au colivre pour recevoir les données d’entrée manuscrite pour le dessin. Le client appelle d’abord la méthode [IPaper :: Redraw](ipaper--redraw.md) sur l’objet du codocument pour demander toutes les données d’encre du dessin actuel. L’implémentation du codocument de redessin utilise ensuite l’implémentation cliente de [**IPaperSink**](ipapersink-methods.md) pour transmettre les données au client.

À mesure que l’utilisateur dessine de manière interactive dans le client, il peint immédiatement les données à l’écran tout en l’envoyant également au colivre pour l’enregistrer. Lorsque le client demande que l’écran soit [redessiné](ipaper--redraw.md) , il appelle la méthode de redessin du colivre. Ce type de redessin est courant dans les applications. Par exemple, le redessin se produit lorsque la fenêtre cliente est superposée par une autre fenêtre d’application. Le client dispose d’un rendu bitmap de l’image dessinée, mais le bitmap est facilement perdu et doit souvent être redessiné. Le client s’appuie sur le colivre dans le serveur pour les données d’encre requises pour le redessin.

Il s’agit d’une division client/serveur courante. Cela s’avère particulièrement utile lorsque plusieurs clients ont besoin de partager les données. Le colivre est codé pour activer cette. Elle utilise la fonction APPUTIL CThreaded pour assurer la sécurité des threads. Une application qui peut exploiter cette conception est une application de tableau blanc partagé, où plusieurs clients peuvent contribuer à un dessin fréquemment consulté. La prise en charge de COM pour DCOM (Distributed COM) prend en charge ce type d’utilisation d’applications de groupe de travail sur le réseau. Pour plus d’informations, consultez l’exemple REMCLIEN précédent.

Une utilisation plus modeste du schéma « client/serveur » est d’intégrer le comportement des objets implémentés dans des applications différentes sur le même ordinateur. dans ce cas, les clients peuvent être un conteneur ActiveX dans des applications distinctes qui partagent des données gérées par le même objet. Ces données ne sont peut-être pas les données de dessin manuscrits prises en charge par le composant DllPaper. **StoServe** peut être utilisé comme infrastructure de départ pour la programmation de composants qui gèrent d’autres types de données partagées.

## <a name="support-information"></a>Informations de support

Le Makefile **StoServe** inscrit le composant COM **StoServe** DllPaper dans le registre. Ce composant doit être inscrit avant que **StoServe** soit disponible pour les clients COM externes en tant que serveur pour ce composant. Cette inscription automatique s’effectue à l’aide de l’utilitaire de Register.exe intégré à l’exemple REGISTER. Pour générer ou exécuter **StoServe**, commencez par générer l’exemple de code Register.

Pour plus d’informations sur la configuration de votre système pour générer et tester les exemples de code de cette série de didacticiels COM, consultez [Comment générer des exemples](how-to-build-samples.md). Le Makefile fourni (MAKEFILE) est compatible avec Microsoft NMAKE. Pour créer une version Debug, émettez la commande NMAKE dans la fenêtre d’invite de commandes.

pour une utilisation pratique dans Microsoft Visual Studio, un fichier projet est fourni pour chaque exemple. pour charger le projet pour l’exemple **StoServe** , vous pouvez exécuter Visual Studio à l’invite de commandes dans le répertoire samples comme suit :

MSDEV STOSERVE. DSP

vous pouvez également double-cliquer sur le fichier Stoserve. dsp dans Windows Explorer pour charger un exemple de projet dans Visual Studio. dans Visual Studio vous pouvez parcourir les classes C++ de l’exemple de source et effectuer généralement les autres opérations de modification-compilation-débogage.

> [!Note]  
> dans le cadre du kit de développement logiciel (SDK) de la plateforme, la compilation de ces exemples à partir de Visual Studio requiert le paramètre approprié des chemins d’accès aux répertoires dans Visual Studio. Pour plus d’informations, consultez [Comment générer des exemples](how-to-build-samples.md).

 

 

 