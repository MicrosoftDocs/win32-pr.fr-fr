---
title: Indicateurs de route
description: Indicateurs de route
ms.assetid: 17deae88-573f-48ec-887e-521549b39c32
keywords:
- Route
- Indicateurs de route
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1476742f1204eb14dd2bb96b289825d179a58e5bec01ff0aee18bcfbdb13a9b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081239"
---
# <a name="route-flags"></a>Indicateurs de route

## <a name="state-of-the-route-constants"></a>État des constantes de routage



| Constante                    | Valeur | Description             |
|-----------------------------|-------|-------------------------|
| État de l' \_ itinéraire RTM \_ \_ créé  | 0     | L’itinéraire a été créé. |
| suppression de l’état de l' \_ itinéraire RTM \_ \_ | 1     | L’itinéraire est en cours de suppression. |
| État de l' \_ itinéraire RTM \_ \_ supprimé  | 2     | L’itinéraire a été supprimé. |



 

## <a name="route-update-flags"></a>Indicateurs de mise à jour de routage



| Constante                  | Valeur      | Description                                                                                                                                                                                |
|---------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modification du routage RTM en \_ \_ \_ premier | 0x01       | Indique que le gestionnaire de table de routage ne doit pas vérifier le membre **voisin** de la structure d' [**\_ \_ informations d’itinéraire RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) lors de la détermination du moment où deux itinéraires sont égaux. |
| \_ \_ nouvelle modification de l’itinéraire \_ RTM   | 0x02       | Retourné par le gestionnaire de tables de routage pour indiquer qu’un nouvel itinéraire a été créé.                                                                                                                 |
| \_ \_ meilleure modification de l’itinéraire RTM \_  | 0x00010000 | Retourné par le gestionnaire de tables de routage pour indiquer que l’itinéraire ajouté ou mis à jour était le meilleur itinéraire, ou qu’en raison de la modification, un nouvel itinéraire est devenu le meilleur itinéraire.           |



 

## <a name="unicast-flags"></a>Indicateurs de monodiffusion



| Constante                  | Valeur  | Description                                                            |
|---------------------------|--------|------------------------------------------------------------------------|
| \_ \_ indicateurs \_ locaux de l’itinéraire RTM  | 0x0010 | Indique qu’une destination est sur un réseau directement accessible.            |
| \_indicateurs de route RTM \_ \_ distants | 0x0020 | Indique que la destination n’est pas sur un réseau directement accessible. |
| \_indicateurs de route RTM moi- \_ \_ même | 0x0040 | Indique que la destination est l’une des adresses du routeur.            |



 

## <a name="broadcast-and-multicast-flags"></a>Indicateurs de diffusion et de multidiffusion



| Constante                           | Valeur  | Description                                                                                                                                                                                                |
|------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_indicateurs d’itinéraire RTM \_ \_ mcast           | 0x0100 | Indique que cet itinéraire est un itinéraire vers une adresse de multidiffusion.                                                                                                                                               |
| \_indicateurs d’itinéraire RTM \_ \_ local \_ mcast    | 0x0200 | Indique que cet itinéraire est un itinéraire vers une adresse de multidiffusion locale.                                                                                                                                         |
| \_indicateurs de route RTM \_ \_ limité \_ BC     | 0x0400 | Indique que cet itinéraire est une adresse de diffusion limitée. Les paquets vers cette destination ne doivent pas être transférés.                                                                                             |
| \_zéros des indicateurs d’itinéraires RTM \_ \_ \_ NETBC    | 0x1000 | Indique que la destination correspond à l’adresse de diffusion tout-zéro de l’interface. Si le transfert de diffusion est activé, les paquets doivent recevoir et renvoyer toutes les interfaces appropriées.               |
| \_zéros des indicateurs d’itinéraires RTM \_ \_ \_ SUBNETBC | 0x2000 | Indique que la destination correspond à l’adresse de diffusion de sous-réseau tout-zéro de l’interface. Si le transfert de diffusion sous-réseau est activé, les paquets doivent recevoir et renvoyer toutes les interfaces appropriées. |
| \_indicateurs d’itinéraire RTM \_ \_ \_ NETBC     | 0x4000 | Indique que la destination correspond à l’adresse de diffusion tout-à-un d’une interface. Si le transfert de diffusion est activé, les paquets doivent recevoir et renvoyer toutes les interfaces appropriées.                |
| \_indicateurs d’itinéraire RTM \_ \_ \_ SUBNETBC  | 0x8000 | Indique que la destination correspond à l’adresse de diffusion de sous-réseau toutes les autres de l’interface. Si le transfert de diffusion sous-réseau est activé, les paquets doivent recevoir et renvoyer toutes les interfaces appropriées.  |



 

## <a name="grouping-of-flags"></a>Regroupement d’indicateurs



| Groupe                            | Membres                                                                                                                                                                  | Description                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| \_transfert des \_ indicateurs de routage RTM \_    | indicateurs d’itinéraire RTM \_ \_ \_ MARTIAN, RTM \_ indicateurs d’itinéraires \_ \_ BLACKHOLE, RTM \_ indicateurs d’itinéraire \_ \_ ignorés, \_ indicateurs de route RTM \_ \_ inactifs                                                        | Spécifie les indicateurs de transfert.                          |
| \_l’itinéraire RTM \_ signale \_ toute \_ monodiffusion  | indicateurs d’itinéraire RTM \_ \_ \_ local, \_ indicateurs d’itinéraire RTM \_ \_ à distance, \_ indicateurs de routage RTM moi- \_ \_ même                                                                                           | Spécifie des indicateurs de monodiffusion.                             |
| \_l’itinéraire RTM \_ signale \_ un \_ mcast    | \_indicateurs d’itinéraire RTM \_ \_ MCAST, \_ paramètres d’itinéraire RTM \_ \_ local \_ mcast                                                                                                                | Spécifie des indicateurs de monodiffusion.                             |
| \_Bcast de \_ \_ sous-réseau des indicateurs de route RTM \_ | \_ \_ indicateurs de route \_ RTM \_ , sous-réseau \_ BC, RTM \_ indicateurs d’itinéraire \_ \_ zéros \_ SUBNETBC                                                                                                  | Spécifie les indicateurs de diffusion de sous-réseau.                    |
| \_indicateurs d’itinéraire RTM \_ \_ NET \_ BCAST    | \_indicateurs d’itinéraire RTM \_ \_ \_ NETBC, RTM \_ route \_ Flags \_ zéros \_ NETBC                                                                                                          | Spécifie des indicateurs de diffusion sur l’ensemble du réseau.                  |
| \_l’itinéraire RTM \_ signale \_ n’importe quel \_ BCAST    | indicateurs d’itinéraire RTM \_ \_ \_ limité \_ BC, \_ indicateurs de route RTM, \_ \_ \_ NETBCs, indicateurs de route RTM, \_ \_ \_ \_ sous-réseau \_ BC, version d’indicateur de l' \_ itinéraire RTM \_ \_ zéros \_ NETBC, RTM \_ route \_ Flags \_ zéros \_ SUBNETBC | Spécifie l’un des indicateurs de diffusion sous-réseau ou à l’ensemble du réseau. |



 

 

 




