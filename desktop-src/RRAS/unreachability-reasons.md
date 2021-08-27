---
title: Raisons de l’inaccessibilité
description: Le tableau suivant répertorie les valeurs constantes qui indiquent la raison pour laquelle une interface est inaccessible.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cb833409d9d2ba31adedbc2942d39399c0a5763ad4d65dc7cdcaf234f97efb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025409"
---
# <a name="unreachability-reasons"></a>Raisons de l’inaccessibilité

Le tableau suivant répertorie les valeurs constantes qui indiquent la raison pour laquelle une interface est inaccessible.



| Valeur                                       | Signification                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| administration de l' \_ interface MPR \_ \_ désactivée             | L’administrateur a désactivé l’interface.                                                  |
| échec de connexion de l' \_ interface MPR \_ \_         | La tentative de connexion précédente a échoué. Examinez le membre **dwLastError** pour obtenir le code d’erreur. |
| DIALOUT de l’interface MPR- \_ \_ \_ restriction des heures \_ | La numérotation à distance n’est pas autorisée à l’heure actuelle.                                                   |
| \_interface MPR \_ hors \_ des \_ ressources          | Aucun port ou périphérique ne peut être utilisé.                                                     |
| \_service d’interface MPR \_ \_ suspendu             | Le service est suspendu.                                                                         |
| \_interface MPR \_ aucune \_ détection de support \_            | Le câble réseau est déconnecté de la carte réseau.                                       |
| \_interface MPR \_ sans \_ appareil                  | La carte réseau a été supprimée de la machine.                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_Interface MPR \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[**\_Interface MPR \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[**\_IFROW MIB**](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[**\_IFSTATUS MIB**](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 