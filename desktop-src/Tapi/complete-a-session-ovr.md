---
description: Les opérations d’achèvement permettent à une application de spécifier la manière dont elle souhaite gérer une session lorsque des facteurs tels qu’une destination occupée empêchent une connexion normale.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Terminer une session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533613"
---
# <a name="complete-a-session"></a>Terminer une session

Les opérations d’achèvement permettent à une application de spécifier la manière dont elle souhaite gérer une session lorsque des facteurs tels qu’une destination occupée empêchent une connexion normale.

Les [ \_ constantes LINECALLCOMPLMODE](./linecallcomplmode--constants.md) définissent les options possibles qu’une application peut avoir, en fonction des fonctionnalités du fournisseur de services.

Plusieurs demandes d’achèvement d’appel peuvent être en attente pour une adresse donnée à un moment donné. Pour identifier des demandes individuelles, l’implémentation retourne un [identificateur de saisie semi-automatique](completion-id-ovr.md). L’annulation d’une demande d’achèvement d’appel en cours utilise également cet identificateur d’achèvement d’appel.

**TAPI 2. x :** Consultez [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).

**TAPI 3. x :** Consultez [**ITBasicCallControl :: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl ::D éconnecter**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
