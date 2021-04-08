---
title: Gestionnaires d’objets
description: Gestionnaires d’objets
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7294ddd48d2acaa010ad15c0e2497fd33c7f071
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839529"
---
# <a name="object-handlers"></a>Gestionnaires d’objets

Si une application serveur OLE est un serveur local, ce qui signifie qu’elle s’exécute dans son propre espace de processus, la communication entre le conteneur et le serveur doit être effectuée au-delà des limites du processus. Étant donné que ce processus est onéreux, OLE s’appuie sur un objet de substitution chargé dans l’espace de processus du conteneur pour agir pour le compte d’une application serveur locale. Cet objet de substitution, connu sous le nom de *Gestionnaire d’objets*, demande de conteneur de services qui ne requiert pas l’attention de l’application serveur, comme les demandes de dessin. Lorsqu’un conteneur demande un objet que le gestionnaire d’objets ne peut pas fournir, le gestionnaire communique avec l’application serveur à l’aide du mécanisme de communication out-of-process de COM.

Un gestionnaire d’objets est unique à une classe d’objet. Lorsque vous créez une instance d’un gestionnaire pour une classe, vous ne pouvez pas l’utiliser pour une autre. Lorsqu’il est utilisé pour un document composé, le gestionnaire d’objets implémente les structures de données côté conteneur lorsque vous accédez aux objets d’une classe particulière à distance.

OLE fournit un gestionnaire d’objets par défaut que les applications serveur locales peuvent utiliser. Pour les applications qui requièrent des comportements spéciaux, les développeurs peuvent implémenter un gestionnaire personnalisé qui remplace le gestionnaire par défaut ou l’utilise pour fournir certains comportements par défaut.

Un gestionnaire d’objets est une DLL contenant plusieurs composants interactifs. Ces composants incluent des éléments de communication à distance pour gérer la communication entre le gestionnaire et son application serveur, un cache pour le stockage des données d’un objet, ainsi que des informations sur la façon dont ces données doivent être mises en forme et affichées, ainsi qu’un objet de contrôle qui coordonne les activités des autres composants de la DLL. En outre, si un objet est un lien, la DLL comprend également un composant de liaison, ou un *objet lié*, qui assure le suivi du nom et de l’emplacement de la source de la liaison.

Le *cache* contient des données et des informations de présentation suffisantes pour que le gestionnaire affiche un objet chargé, mais pas en cours d’exécution, dans son conteneur. OLE fournit une implémentation du cache utilisé par le gestionnaire d’objets par défaut d’OLE et l’objet Link. Le cache stocke les données dans les formats requis par le gestionnaire d’objets pour répondre aux demandes de dessin de conteneur. Lorsque les données d’un objet sont modifiées, l’objet envoie une notification au cache pour qu’une mise à jour puisse se produire. Pour plus d’informations sur le cache, consultez [afficher la mise en cache](view-caching.md).

Pour plus d'informations, voir la rubrique suivante :

-   [Gestionnaire par défaut et gestionnaires personnalisés](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Documents composés](compound-documents.md)
</dt> </dl>

 

 




