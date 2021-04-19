---
description: L’arrêt de la session peut provenir d’une demande de l’utilisateur, d’une déconnexion distante par l’autre partie ou pour des raisons spécifiques à l’application.
ms.assetid: 69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d
title: Terminer une session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac433f1c8104ec41a3c42dc44c32a2b110d79469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531424"
---
# <a name="terminate-a-session"></a>Terminer une session

L’arrêt de la session peut provenir d’une demande de l’utilisateur, d’une déconnexion distante par l’autre partie ou pour des raisons spécifiques à l’application. Lorsqu’une session est arrêtée, l' [identificateur de session](session-identifier-ovr.md) reste valide jusqu’à ce qu’il soit publié et peut être utilisé pour collecter des données après la connexion.

L’arrêt de la session est terminé en désallouant et en libérant les ressources associées à la session. Si une session est simplement supprimée ou déconnectée, mais que les ressources ne sont pas libérées, le résultat est une fuite de mémoire dans l’application et éventuellement dans le fournisseur de services.

**TAPI 2. x :** Consultez [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), [**lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall).

**TAPI 3. x :** Consultez [**ITBasicCallControl ::D éconnecter**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect), effectuez une mise en forme com standard sur le pointeur d’objet d’appel.

 

 
