---
title: Fin de la session d’authentification
description: Une fois la session d’authentification terminée, le service d’authentification appelle la fonction RasEapEnd pour permettre au protocole d’authentification de libérer sa mémoire tampon de travail.
ms.assetid: 466795ac-fee5-4b82-adc7-af14b6ef3fc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27899ef348630e412b3d52d066f59ea9b5255244
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381846"
---
# <a name="completion-of-the-authentication-session"></a>Fin de la session d’authentification

Une fois la session d’authentification terminée, le service d’authentification appelle la fonction [**RasEapEnd**](/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)) pour permettre au protocole d’authentification de libérer sa mémoire tampon de travail. Cette action est effectuée que l’authentification ait abouti ou non. L’appel de la fonction **RasEapEnd** garantit qu’aucun autre appel au protocole d’authentification n’est effectué à l’aide de cet utilisateur ou contexte sans appeler d’abord [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)).

 

 