---
description: Une extension de composant logiciel enfichable d’une pièce jointe doit permettre à l’utilisateur de modifier les informations de configuration relatives au service.
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: Modification des informations de configuration dans l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6158d76d0f5114bd2d7b483e0af3d00f8f2439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536819"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a>Modification des informations de configuration dans l’interface utilisateur

Une extension de composant logiciel enfichable d’une pièce jointe doit permettre à l’utilisateur de modifier les informations de configuration relatives au service. Les informations modifiées doivent être stockées par l’extension de composant logiciel enfichable d’attachement jusqu’à ce que le composant logiciel enfichable Configuration de la sécurité appelle les méthodes de l’interface [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) pour récupérer les informations.

Pour éviter les fuites de mémoire, libérez de la mémoire allouée par l’extension de composant logiciel enfichable en appelant [**ISceSvcAttachmentPersistInfo :: FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).

 

 



