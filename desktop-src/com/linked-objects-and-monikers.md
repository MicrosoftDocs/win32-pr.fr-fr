---
title: Objets liés et monikers
description: Les objets liés, comme les objets incorporés, s’appuient sur un gestionnaire d’objets pour communiquer avec les applications serveur.
ms.assetid: f72557b9-cd24-4d96-8144-94a5344ec2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c14f4cc74ee84fbf745e730d77203ebb4f43b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197280"
---
# <a name="linked-objects-and-monikers"></a>Objets liés et monikers

Les objets liés, comme les objets incorporés, s’appuient sur un gestionnaire d’objets pour communiquer avec les applications serveur. Toutefois, l’objet lié lui-même gère l’affectation de noms et le suivi des sources de liens. L’objet lié agit comme un serveur in-process. Par exemple, lorsqu’il est activé, un objet lié localise et lance l’application serveur OLE qui est la source de la liaison.

Le gestionnaire d’un objet lié se compose de deux composants principaux : le composant de gestionnaire et le composant de liaison. Le composant Handler contient les éléments de contrôle et de communication à distance, ainsi qu’un gestionnaire pour un objet incorporé. Le composant de liaison a son propre contrôleur et son propre cache, et il permet d’accéder au stockage structuré de l’objet. Le contrôleur de composants de liaison prend en charge le nom de la source via l’utilisation de monikers, et la liaison, le processus de localisation et d’exécution de la source de liaison. (Pour plus d’informations sur les monikers et la liaison, consultez [modèle objet de composant](the-component-object-model.md).)

Lorsqu’un utilisateur crée initialement un objet lié ou charge un objet existant à partir du stockage, le conteneur charge une instance du composant de liaison en mémoire, ainsi que le gestionnaire d’objets. Le composant de liaison fournit des interfaces, notamment [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink), qui identifient l’objet comme un lien et lui permettent de gérer l’affectation de noms, le suivi et la mise à jour de sa source de liaison.

En implémentant l’interface [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) , un objet lié fournit son conteneur avec les fonctions qui prennent en charge la liaison. Seuls les objets liés implémentent **IOleLink**, et en interrogeant cette interface, un conteneur peut déterminer si un objet donné est incorporé ou lié. La fonction la plus importante fournie par **IOleLink** permet à un conteneur de se lier à la source de l’objet lié, autrement dit, d’activer la connexion au document qui stocke les données natives de l’objet lié. **IOleLink** définit également des fonctions pour la gestion des informations relatives à l’objet lié, telles que les données de présentation mises en cache et l’emplacement de la source de liaison.

Lorsqu’un document composé contenant un objet lié est enregistré, les données du lien sont enregistrées avec la source du lien, et non avec le conteneur. Seules les informations relatives à son nom et à son emplacement sont enregistrées avec le document composé. Ce comportement est différent de celui d’un objet incorporé, dont les données sont stockées avec celles de son conteneur.

Les applications de conteneur peuvent fournir des informations sur leurs objets incorporés, de sorte que ces dernières, ou parties, puissent agir comme des sources de liaison. En implémentant la prise en charge de la liaison aux objets incorporés de votre conteneur, vous rendez les imbrications imbriquées possibles, ce qui évite à l’utilisateur d’avoir à repérer les originaux de chaque objet d’incorporation auquel un lien est souhaité. Par exemple, si un utilisateur souhaite incorporer une feuille de calcul Microsoft Excel dans Microsoft Word, et que la feuille de calcul contient une bitmap créée dans Paintbrush, l’utilisateur peut créer un lien vers une copie de l’image bitmap contenue dans la feuille de calcul plutôt que dans l’original.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Documents composés](compound-documents.md)
</dt> <dt>

[Serveurs in-process](in-process-servers.md)
</dt> <dt>

[Gestionnaires d’objets](object-handlers.md)
</dt> </dl>

 

 




