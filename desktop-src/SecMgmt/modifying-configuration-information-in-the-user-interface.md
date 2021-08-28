---
description: Une extension de composant logiciel enfichable d’une pièce jointe doit permettre à l’utilisateur de modifier les informations de configuration relatives au service.
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: Modification des informations de configuration dans l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 414e2ab1475ec1c3241d60b96d182a522c299a9f5cf6134f50339c2088c99d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005117"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a>Modification des informations de configuration dans l’interface utilisateur

Une extension de composant logiciel enfichable d’une pièce jointe doit permettre à l’utilisateur de modifier les informations de configuration relatives au service. Les informations modifiées doivent être stockées par l’extension de composant logiciel enfichable d’attachement jusqu’à ce que le composant logiciel enfichable Configuration de la sécurité appelle les méthodes de l’interface [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) pour récupérer les informations.

Pour éviter les fuites de mémoire, libérez de la mémoire allouée par l’extension de composant logiciel enfichable en appelant [**ISceSvcAttachmentPersistInfo :: FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).

 

 



