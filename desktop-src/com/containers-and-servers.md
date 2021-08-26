---
title: Conteneurs et serveurs
description: Conteneurs et serveurs
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136d301d85bc317cd4e60d609e73b6b7232cfb5634a33bf32a2496fe8cd672d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993569"
---
# <a name="containers-and-servers"></a>Conteneurs et serveurs

Les applications de document composé sont de deux types de base : les applications de conteneur et les applications serveur. Les applications de conteneur OLE fournissent aux utilisateurs la possibilité de créer, de modifier, d’enregistrer et de récupérer des documents composés. Les applications serveur OLE fournissent aux utilisateurs les moyens de créer des documents et d’autres représentations de données qui peuvent être contenus comme des liens ou des incorporations dans les applications de conteneur. Une application OLE peut être une application de conteneur, une application serveur, ou les deux.

Les applications serveur OLE varient également selon qu’elles sont implémentées en tant que *serveurs in-process* ou *serveurs locaux*. Un serveur in-process est une bibliothèque de liens dynamiques (DLL) qui s’exécute dans l’espace de processus de l’application conteneur. Vous ne pouvez exécuter un serveur in-process qu’à partir de l’application conteneur.

> [!Note]  
> Les versions ultérieures d’OLE activent la liaison et l’incorporation à travers les limites de l’ordinateur, de sorte qu’une application de conteneur sur un ordinateur puisse utiliser un objet de document composé fourni par un *serveur distant* exécuté sur un autre ordinateur. Du point de vue d’une application de conteneur, toute application serveur OLE qui s’exécute dans son propre espace de processus, que ce soit sur le même ordinateur ou sur un ordinateur distant, est un *serveur hors processÂ*.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Documents composés](compound-documents.md)
</dt> <dt>

[Serveurs in-process](in-process-servers.md)
</dt> </dl>

 

 




