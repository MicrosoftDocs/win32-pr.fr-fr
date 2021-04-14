---
title: Afficher la mise en cache
description: Afficher la mise en cache
ms.assetid: d19c111c-1367-43a2-97a9-35dc0ff5dcc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c5bc2555e907cdc4e600465b807387c3a5548
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382927"
---
# <a name="view-caching"></a>Afficher la mise en cache

Une application conteneur doit être en mesure d’obtenir une présentation d’un objet afin de l’afficher ou de l’imprimer pour les utilisateurs lorsque le document est ouvert, mais que l’application serveur de l’objet n’est pas en cours d’exécution ou n’est pas installée sur l’ordinateur de l’utilisateur. Toutefois, en supposant que les serveurs pour tous les objets qui peuvent se trouver dans un document sont installés sur l’ordinateur de chaque utilisateur et peuvent toujours s’exécuter à la demande est irréaliste. Le gestionnaire d’objets par défaut, qui est disponible à tout moment, résout ce dilemme en mettant en cache les présentations d’objets dans le stockage du document et en manipulant ces présentations sur n’importe quelle plateforme, quel que soit le disponibilité du serveur d’objets sur une installation particulière du conteneur.

Les conteneurs peuvent conserver des présentations de dessin pour un ou plusieurs appareils cibles spécifiques en plus de celui requis pour gérer l’objet à l’écran. En outre, si vous portez l’objet d’une plateforme à une autre, OLE convertit automatiquement les formats de données de l’objet en ceux pris en charge sur la nouvelle plateforme. Par exemple, si vous déplacez un objet de Windows vers le Macintosh, OLE convertit ses présentations de métafichiers au format PICT.

Pour présenter une représentation exacte d’un objet incorporé à l’utilisateur, l’application conteneur de l’objet lance une boîte de dialogue avec le gestionnaire d’objets, en demandant des données et des instructions de dessin. Pour pouvoir traiter les demandes du conteneur, le gestionnaire doit implémenter les interfaces [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)et [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) .

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) permet à une application de conteneur OLE d’extraire et d’envoyer des données à ses objets incorporés ou liés. Lorsque les données sont modifiées dans un objet, cette interface permet à l’objet de rendre ses nouvelles données disponibles à son conteneur et fournit au conteneur un moyen de mettre à jour les données dans sa copie de l’objet. (Pour plus d’informations sur le transfert de données en général, consultez le chapitre 4, Transfert de données.)

L’interface [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) est très similaire à l’interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , à ceci près qu’elle demande à un objet de se dessiner lui-même sur un contexte de périphérique, tel qu’un écran, une imprimante ou un métafichier, plutôt que de déplacer ou de copier ses données vers la mémoire ou un autre moyen de transfert. L’objectif de l’interface est de permettre à un conteneur OLE d’obtenir des représentations graphiques alternatives de ses objets incorporés, dont il possède déjà les données, évitant ainsi la surcharge liée à la nécessité de transférer des instances entièrement nouvelles des mêmes objets de données simplement pour obtenir de nouvelles instructions de dessin. Au lieu de cela, l’interface **IViewObject2** permet au conteneur de demander à un objet de fournir une représentation graphique de lui-même en dessinant sur un contexte de périphérique spécifié par le conteneur.

Lors de l’appel de l’interface [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) , une application conteneur peut également spécifier que l’objet se dessine sur un appareil cible différent de celui sur lequel il sera effectivement rendu. Cela permet au conteneur, si nécessaire, de générer différents rendus à partir d’un seul objet. Par exemple, l’appelant peut demander à l’objet de se composer lui-même pour une imprimante même si le dessin qui en résulte s’affiche à l’écran. Le résultat, bien sûr, serait un aperçu avant impression de l’objet.

L’interface [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)fournit également des méthodes qui permettent aux conteneurs de s’inscrire pour les notifications de modification d’affichage. Comme avec les données et les avis OLE, une connexion de notification de vue permet à un conteneur de mettre à jour ses rendus d’un objet à sa propre commodité plutôt qu’en réponse à un appel de l’objet. Par exemple, si une nouvelle version de l’application serveur d’un objet devait offrir des vues supplémentaires des mêmes données, le gestionnaire par défaut de l’objet appellera l’implémentation de [**IAdviseSink :: OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange) de chaque conteneur pour signaler que les nouvelles présentations étaient disponibles. Le conteneur récupère ces informations à partir du récepteur de notifications uniquement lorsque cela est nécessaire.

Étant donné que les contextes de périphérique Windows ont une signification uniquement au sein d’un processus unique, vous ne pouvez pas passer de pointeurs [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) au-delà des limites de processus. Par conséquent, les serveurs OLE locaux et distants n’ont pas besoin d’implémenter l’interface, ce qui ne fonctionnerait pas correctement même s’ils l’ont fait. Seuls les gestionnaires d’objets et les serveurs in-process implémentent l’interface **IViewObject2**. OLE fournit une implémentation par défaut, que vous pouvez utiliser dans vos propres serveurs OLE in-process et gestionnaires d’objets en agrégeant simplement le gestionnaire OLE par défaut. Vous pouvez ou écrire votre propre implémentation de **IViewObject2**.

Un objet implémente l’interface [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) afin de permettre au gestionnaire de connaître les fonctionnalités qu’il doit mettre en cache. Le gestionnaire d’objets possède également le cache et s’assure qu’il est tenu à jour. Lorsque l’objet incorporé passe à l’État en cours d’exécution, le gestionnaire définit des connexions de notifications appropriées sur l’objet serveur, avec lui-même le récepteur. Les implémentations de l’interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) et [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)fonctionnent à partir de données mises en cache côté client. L’implémentation du gestionnaire de **IViewObject2** est responsable de la détermination des formats de données à mettre en cache pour répondre aux demandes de dessin du client. L’implémentation de **IDataObject** par le gestionnaire est chargée d’obtenir des données dans différents formats, etc., entre la mémoire et l’instance [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) sous-jacente de l’objet incorporé. Les gestionnaires personnalisés peuvent utiliser ces implémentations en regroupant sur le gestionnaire par défaut.

> [!Note]  
> L’interface [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) est une extension fonctionnelle simple de [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) et doit être implémentée à la place de la dernière interface, qui est désormais obsolète. En plus de fournir les méthodes **IViewObject** , l’interface **IViewObject2** fournit un membre supplémentaire unique, [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject2-getextent), qui permet à une application de conteneur d’obtenir la taille de la présentation d’un objet à partir du cache sans avoir d’abord à déplacer l’objet vers l’État en cours d’exécution avec un appel à [**IOleObject :: GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Documents composés](compound-documents.md)
</dt> </dl>

 

 