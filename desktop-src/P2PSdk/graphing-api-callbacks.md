---
description: 'L’API graphique utilise les rappels suivants :'
ms.assetid: a8e083ab-b5e3-4186-99fb-cbb536e9d529
title: Rappels d’API de graphique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0604c03ce768372e4f6fa81abfe69184ef45f49f41a2907d652b77b97902b6f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776249"
---
# <a name="graphing-api-callbacks"></a>Rappels d’API de graphique

L’API graphique utilise les rappels suivants :



| Rappel                                                          | Description                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*PFNPEER \_ les \_ données de sécurité gratuites \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_free_security_data) | Spécifie la fonction que l’infrastructure graphique des homologues appelle pour libérer les données retournées par [*PFNPEER \_ Secure \_ Record*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) et [*PFNPEER \_ valident \_*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) les rappels d’enregistrement. |
| [*\_enregistrement sécurisé \_ PFNPEER*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record)            | Spécifie la fonction que l’infrastructure graphique des homologues appelle pour sécuriser les enregistrements.                                                                                                                                        |
| [*PFNPEER \_ valider l' \_ enregistrement*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record)        | Spécifie la fonction que l’infrastructure graphique des homologues appelle pour valider les enregistrements.                                                                                                                                      |



 

 

 



