---
title: Raisons de l’inaccessibilité
description: Le tableau suivant répertorie les valeurs constantes qui indiquent la raison pour laquelle une interface est inaccessible.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b99d36ba895394a417130ab3ae45d1a47c7ed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031590"
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

 

 