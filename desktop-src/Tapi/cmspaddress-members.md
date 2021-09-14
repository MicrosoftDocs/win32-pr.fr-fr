---
description: La liste suivante contient les membres d’adresse CMSP.
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: Membres CMSPAddress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217937"
---
# <a name="cmspaddress-members"></a>Membres CMSPAddress



| Types de membres                    | Nom                    | Description                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| IUnknown                        | \*m \_ pFTM               | Pointeur vers le marshaleur libre de threads.                                                         |
| HANDLE                          | m \_ htEvent              | Handle de l’événement de Tapi3.dll, qui est utilisé pour notifier l’interface TAPI que le MSP souhaite lui envoyer des données. |
| entrée de liste \_                     | m \_ EventList            | Liste des événements.                                                                                  |
| CMSPCritSection                 | m \_ EventDataLock        | Verrou qui protège les données relatives à la gestion des événements avec l’interface TAPI.                             |
| ITTerminalManager               | \*m \_ pITTerminalManager | Pointeur vers l’objet du gestionnaire de terminal.                                                      |
| CMSPArray <ITTerminal \*> | \_terminaux m            | Liste des terminaux statiques qui peuvent être utilisés sur l’adresse.                                    |
| BOOL                            | m \_ fTerminalsUpToDate   | Cet indicateur a la **valeur true** si la liste des terminaux est à jour.                                        |
| CMSPCritSection                 | m \_ TerminalDataLock     | Verrou qui protège les membres de données liés aux terminaux.                                        |



 

 

 



