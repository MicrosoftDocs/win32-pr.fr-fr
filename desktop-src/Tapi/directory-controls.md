---
description: Le diagramme suivant illustre les principaux objets impliqués dans les contrôles de répertoires TAPI 3 Rendezvous. Les interfaces affichées sont des liens hypertexte vers les pages de référence appropriées.
ms.assetid: f5ca1d61-5266-4406-8199-338e6a712db8
title: Contrôles de répertoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87a7b9c0b11c76aac6067e1a3f67c3899552f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538853"
---
# <a name="directory-controls"></a>Contrôles de répertoire

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Le diagramme suivant illustre les principaux objets impliqués dans les contrôles de répertoires TAPI 3 Rendezvous. Les interfaces affichées sont des liens hypertexte vers les pages de référence appropriées.

![interfaces et objets de contrôle d’annuaire Rendezvous](images/renddir.png)

L’interface de contrôle d’annuaire principale est [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), qui doit être créée en appelant **CoCreateInstance**. L’objet Rendezvous expose des méthodes pour récupérer des listes de répertoires disponibles et pour créer des répertoires ou des objets d’annuaire.

Un répertoire réside sur un serveur et est une liste d’objets d’annuaire, ainsi que des informations descriptives. Les méthodes associées à [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) peuvent obtenir des informations associées à l’annuaire dans son ensemble, par exemple s’il s’agit d’un annuaire ils.

Un objet d’annuaire peut représenter une conférence ou un utilisateur. L’interface [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) fournit des méthodes qui permettent de récupérer ou de modifier des informations génériques sur un objet d’annuaire, telles que l’adresse de numérotation.

Les informations relatives aux conférences et aux utilisateurs, telles que l’URL d’une conférence ou le téléphone IP principal d’un utilisateur, sont manipulées par les méthodes fournies dans les interfaces [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) et [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) .

 

 



