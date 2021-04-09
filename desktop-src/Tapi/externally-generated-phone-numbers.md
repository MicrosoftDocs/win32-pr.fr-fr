---
description: Un fournisseur de services peut indiquer des numéros de téléphone générés de manière externe en définissant les membres de la structure LINECALLINFO lors du traitement de la \_ fonction TSPI lineGetCallInfo.
ms.assetid: 10c83199-de7d-4a9b-84c4-ef8f5ea5055a
title: Numéros de téléphone générés de manière externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53e7039023ecec987a16c39367a569925c20ef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751613"
---
# <a name="externally-generated-phone-numbers"></a>Numéros de téléphone générés de manière externe

Un fournisseur de services peut indiquer des numéros de téléphone générés de manière externe (autrement dit, des chiffres pour les appels sortants générés en externe sur l’ordinateur) en définissant les membres **DisplayableAddress**, **CalledParty** ou [comments](./comment-ovr.md) dans la structure [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) lors du traitement de la fonction [**\_ lineGetCallInfo TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo) . Si TAPI n’a pas enregistré ses propres données pour ces membres, il laisse les données définies par le fournisseur de services inchangées. Si l’interface TAPI n’a pas de données mises en cache pour ces membres, TAPI ajoute son texte à la fin de la partie variable de la structure **LINECALLINFO** et remplace la taille et l’offset que le fournisseur de services a placé dans la partie fixe.

Un fournisseur de services peut également copier un nombre sortant dans le membre **CalledID** . Par conséquent, les applications de journalisation doivent vérifier le membre **CalledID** sur les appels sortants si les membres **DisplayableAddress** et **CalledParty** sont vides.

 

 
