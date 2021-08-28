---
title: Surveillance du système
description: Surveillance du système
ms.assetid: e0318aca-4e3e-4272-ba31-c770d6b05272
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26be8b5527af1ffb8dfc9e2626fee9248dc28c25babbb7feb345c7d77da4ed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047352"
---
# <a name="monitoring-the-system"></a>Surveillance du système

la restauration du système dans Windows Vista et versions ultérieures permet d’enregistrer une copie du volume lors de la génération d’un point de restauration. La restauration du système nécessite un minimum de 300 Mo d’espace disque libre sur le lecteur système lors de l’installation.

la restauration du système dans Windows XP surveille un ensemble de base de fichiers système et d’application, en archivant les états de ces fichiers avant que les modifications du système ne soient apportées. La restauration du système enregistre également un instantané complet du Registre et certains fichiers système dynamiques. La restauration du système nécessite un minimum de 200 Mo d’espace disque libre sur le lecteur système lors de l’installation. Lorsque la quantité d’espace disque disponible passe sous 50 Mo sur un lecteur quelconque, la restauration du système passe en mode veille et arrête la création de points de restauration. Tous les points de restauration sont supprimés à ce moment-là. La restauration du système réactive et reprend la création de points de restauration dès que 200 Mo d’espace disque sont libres sur le lecteur système. Les fichiers qui sont surveillés ou exclus de l’analyse sont spécifiés dans le fichier% windir% \\ system32 \\ restore \\Filelist.xml. Pour plus d’informations, consultez [extensions de nom de fichier surveillées](monitored-file-extensions.md).

 

 




