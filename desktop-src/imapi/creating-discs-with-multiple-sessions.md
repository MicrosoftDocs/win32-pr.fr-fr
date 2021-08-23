---
title: Création de disques avec plusieurs sessions
description: IMAPi est en charge de la création de disques de données à plusieurs sessions. Il existe quelques considérations à prendre en compte lors de la création d’un disque à sessions multiples.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b108a6b7b07d6d82230362899da26e7264e62a460c197338e223f0e95078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977119"
---
# <a name="creating-discs-with-multiple-sessions"></a>Création de disques avec plusieurs sessions

IMAPi est en charge de la création de disques de données à plusieurs sessions. Il existe quelques considérations à prendre en compte lors de la création d’un disque à sessions multiples.

La méthode [**IDiscMaster :: SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) détermine s’il existe un disque multi-session IMAPI dans le lecteur actif sur le paramètre. Si c’est le cas, IMAPi passe automatiquement en mode de session multiple. L’utilisation de [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) après l’établissement du mode de session multiple entraîne le retour de IMAPI en mode session unique. Cela signifie qu’un disque vierge est requis pour une gravure [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) . Si le disque est en mode multi-session, le même disque doit se trouver dans l’enregistreur actif ou un code d’erreur IMAPi \_ E \_ WRONGDISC est renvoyé.

Si vous sélectionnez un enregistreur au format Joliet, IMAPi lit les informations du disque actuellement installé. Si le disque est un disque IMAPi Joliet antérieur qui a de l’espace pour une autre session, IMAPi se définit automatiquement en mode multi-session. Ce disque doit être présent dans l’enregistreur actif lors de l’appel de [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).

La fermeture de la première session sur un disque nécessite 21 Mo. Chaque session supplémentaire nécessite 11 Mo pour se fermer.

 

 




