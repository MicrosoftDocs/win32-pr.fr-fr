---
title: Opérations de connexion RAS
description: Windows NT et les versions ultérieures fournissent les fonctions RasPhonebookDlg et RasDialDlg qui affichent l’interface utilisateur intégrée pour démarrer une opération de connexion RAS.
ms.assetid: 1e0f82e1-5995-4b47-970b-e6a7ff6d52e0
keywords:
- Opérations de connexion, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e86ddf1586ce11f43e6b34ef15b89cb2d382b28911968f0b0f08dabd086a86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868459"
---
# <a name="ras-connection-operations"></a>Opérations de connexion RAS

Windows NT et les versions ultérieures fournissent les fonctions [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) et [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) qui affichent l’interface utilisateur intégrée pour démarrer une opération de connexion RAS. Pour la plupart des applications, il s’agit de la méthode recommandée pour démarrer une opération de connexion RAS. Windows 95 ne prend pas en charge ces fonctions pour le moment.

Le reste de cette section décrit les fonctions de bas niveau pour le démarrage d’une connexion RAS. ces fonctions sont disponibles sur bothWindows NT 4,0 (et versions ultérieures) et Windows 95.

Une application cliente RAS utilise la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) pour établir une connexion à un serveur RAS. La fonction **rasdial** démarre l’opération de connexion, qui est ensuite effectuée par le gestionnaire de connexions d’accès à distance.

Le gestionnaire de connexions d’accès à distance est un service qui gère les détails de l’établissement de la connexion au serveur distant. Ce service fournit également au client des informations d’État pendant l’opération de connexion. Le gestionnaire de connexions d’accès à distance démarre automatiquement lorsqu’une application charge le RASAPI32.DLL.

L’appel de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) spécifie les informations suivantes lors du démarrage d’une opération de connexion :

-   [Informations de connexion](phone-book-files-and-connection-information.md) dont le gestionnaire de connexions d’accès à distance a besoin pour établir la connexion.
-   Gestionnaire de [notification](notification-handlers.md) facultatif qui reçoit des notifications de progression pendant l’opération de connexion. Si l’appel de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) spécifie un gestionnaire de notification, l’appel est [asynchrone](asynchronous-operations.md); dans le cas contraire, il est [synchrone](synchronous-operations.md).
-   Structure [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) facultative permettant d’activer ou de désactiver les extensions de l’opération [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . Les extensions permettent à un client RAS d’activer directement certains paramètres de modem pour contrôler si RAS utilise les préfixes et les suffixes dans une entrée d’annuaire téléphonique, et pour prendre en charge les [États suspendus](paused-states.md) pendant l’opération de connexion.

 

 