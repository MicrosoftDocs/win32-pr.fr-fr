---
title: Le gestionnaire OLE
description: Un gestionnaire OLE est une DLL contenant plusieurs composants interactifs utilisés pour la liaison et l’incorporation.
ms.assetid: 5a01b4be-38cf-4019-ba20-ee67b836a3e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9579f18b44a36a794ff807d9d616dd3a06dd1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029281"
---
# <a name="the-ole-handler"></a>Le gestionnaire OLE

Un *Gestionnaire OLE* est une DLL contenant plusieurs composants interactifs utilisés pour la liaison et l’incorporation. Pour éviter les frais de communication interprocessus constante entre un conteneur et son serveur, le gestionnaire est chargé dans l’espace de processus du conteneur pour agir au nom d’un serveur en tant que type de processus de substitution. Le gestionnaire OLE gère les demandes de conteneur qui ne requièrent pas l’attention de l’application serveur, telles que les demandes de dessin. Lorsqu’un conteneur demande un objet que le gestionnaire d’objets ne peut pas fournir, le gestionnaire communique avec l’application serveur à l’aide du mécanisme de communication hors processus COM.

Les composants du gestionnaire OLE incluent des éléments de communication à distance pour gérer la communication entre le gestionnaire et son serveur, un cache pour stocker les données d’un objet (ainsi que des informations sur la façon dont ces données doivent être mises en forme et affichées) et un objet de contrôle qui coordonne les activités des autres composants de la DLL. En outre, si un objet est un lien, la DLL comprend également un composant de liaison, ou un *objet lié*, qui assure le suivi du nom et de l’emplacement de la source de la liaison.

OLE fournit un gestionnaire par défaut que la plupart des applications utilisent pour la liaison et l’incorporation. Si la valeur par défaut ne correspond pas à la configuration requise de votre serveur, vous pouvez soit remplacer complètement le gestionnaire par défaut, soit utiliser des parties de la fonctionnalité qu’il fournit, le cas échéant. Dans ce dernier cas, le gestionnaire d’application est implémenté comme un objet d’agrégation composé d’un nouvel objet de contrôle et du gestionnaire par défaut. Les gestionnaires d’applications/par défaut combinés sont également appelés *gestionnaires in-process*. Le *Gestionnaire de communication à distance* est utilisé pour les objets qui ne sont pas affectés à un CLSID dans le registre système ou qui n’ont pas de gestionnaire spécifié. Tout ce qui est nécessaire à partir d’un gestionnaire pour ces types d’objets est qu’ils passent des informations à travers la limite de processus. Pour créer une nouvelle instance du gestionnaire par défaut, appelez [**OleCreateDefaultHandler**](/windows/desktop/api/Ole2/nf-ole2-olecreatedefaulthandler). Pour certaines circonstances spéciales, appelez [**OleCreateEmbeddingHelper**](/windows/desktop/api/Ole2/nf-ole2-olecreateembeddinghelper).

Lorsque vous créez une instance d’un gestionnaire pour une classe, vous ne pouvez pas l’utiliser pour une autre. Lorsqu’il est utilisé pour un document composé, le gestionnaire OLE implémente les structures de données côté conteneur lorsque vous accédez aux objets d’une classe particulière à distance.

OLE a défini le gestionnaire par défaut pour les clients de serveurs locaux de documents composés. Le gestionnaire par défaut implémentait un nombre d’interfaces que le serveur classique n’avait pas. Quand OLE permettait par la suite des serveurs in-process pour des documents composés, ils devaient créer une application auxiliaire d’incorporation qui implémentait ces interfaces supplémentaires afin que les clients puissent travailler en toute transparence avec eux.

Les concepteurs de Framework qui définissent et implémentent un gestionnaire côté client doivent tenir compte de ce problème dans leur conception et fournir un programme d’assistance in-process équivalent pour les mêmes raisons. Même si les concepteurs n’implémentent actuellement pas les interfaces sur le gestionnaire que les serveurs n’exposent pas, ils peuvent souhaiter définir une application d’assistance pour qu’ils puissent les ajouter à l’avenir. Sinon, il est possible d’implémenter les interfaces supplémentaires sur l’objet serveur lui-même.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaire de Client-Side léger](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 




