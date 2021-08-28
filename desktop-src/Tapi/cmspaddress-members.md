---
description: La liste suivante contient les membres d’adresse CMSP.
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: Membres CMSPAddress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ccbf01bed8ea3a567adf19a72c71f00e24e49b38bcb25d5f4564484afb509e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118869193"
---
# <a name="cmspaddress-members"></a>Membres CMSPAddress



| Types de membres                    | Name                    | Description                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| IUnknown                        | \*m \_ pFTM               | Pointeur vers le marshaleur libre de threads.                                                         |
| HANDLE                          | m \_ htEvent              | Handle de l’événement de Tapi3.dll, qui est utilisé pour notifier l’interface TAPI que le MSP souhaite lui envoyer des données. |
| entrée de liste \_                     | m \_ EventList            | Liste des événements.                                                                                  |
| CMSPCritSection                 | m \_ EventDataLock        | Verrou qui protège les données relatives à la gestion des événements avec l’interface TAPI.                             |
| ITTerminalManager               | \*m \_ pITTerminalManager | Pointeur vers l’objet du gestionnaire de terminal.                                                      |
| CMSPArray <ITTerminal \*> | \_terminaux m            | Liste des terminaux statiques qui peuvent être utilisés sur l’adresse.                                    |
| BOOL                            | m \_ fTerminalsUpToDate   | Cet indicateur a la **valeur true** si la liste des terminaux est à jour.                                        |
| CMSPCritSection                 | m \_ TerminalDataLock     | Verrou qui protège les membres de données liés aux terminaux.                                        |



 

 

 



