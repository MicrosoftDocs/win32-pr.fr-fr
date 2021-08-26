---
title: Fin de la session d’authentification
description: Une fois la session d’authentification terminée, le service d’authentification appelle la fonction RasEapEnd pour permettre au protocole d’authentification de libérer sa mémoire tampon de travail.
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee29ac4c4139fc8a575e7570e3c04fbe449aa4d619cea3e096cd12dfcf19bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948469"
---
# <a name="completion-of-the-authentication-session"></a>Fin de la session d’authentification

Une fois la session d’authentification terminée, le service d’authentification appelle la fonction [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) pour permettre au protocole d’authentification de libérer sa mémoire tampon de travail. Cette action est effectuée que l’authentification ait abouti ou non. L’appel de la fonction **RasEapEnd** garantit qu’aucun autre appel au protocole d’authentification n’est effectué à l’aide de cet utilisateur ou contexte sans appeler d’abord [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).

 

 