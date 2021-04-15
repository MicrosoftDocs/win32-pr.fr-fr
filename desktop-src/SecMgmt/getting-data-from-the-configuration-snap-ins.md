---
description: 'L’extension de composant logiciel enfichable pièce jointe n’a aucun moyen d’interroger directement la base de données de sécurité afin de récupérer des informations. Au lieu de cela, il doit interroger ces informations à partir des composants logiciels enfichables de configuration de sécurité à l’aide de ISceSvcAttachmentData :: GetData.'
ms.assetid: 1171beed-5b28-4f31-b33f-533e3c631b0d
title: Obtention de données à partir des composants logiciels enfichables de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c888cef92a354f73f01e87fca12cee2567dab48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529638"
---
# <a name="getting-data-from-the-configuration-snap-ins"></a>Obtention de données à partir des composants logiciels enfichables de configuration

L’extension de composant logiciel enfichable pièce jointe n’a aucun moyen d’interroger directement la base de données de sécurité afin de récupérer des informations. Au lieu de cela, il doit interroger ces informations à partir des composants logiciels enfichables de configuration de sécurité à l’aide de [**ISceSvcAttachmentData :: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).

Le composant logiciel enfichable d’une pièce jointe peut récupérer toutes les données lorsqu’il s’initialise lui-même, ou il peut récupérer des informations lorsque son nœud est ouvert.

> [!Note]  
> Vous devez utiliser la méthode [**ISceSvcAttachmentData :: FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) pour libérer la mémoire tampon allouée par la méthode de composant logiciel enfichable Configuration de la sécurité [**ISceSvcAttachmentData :: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).

 

 

 



