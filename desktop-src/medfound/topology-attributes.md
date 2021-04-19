---
description: Attributs de topologie
ms.assetid: 50102096-a29f-4c00-a685-179ba5d71089
title: Attributs de topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 286b6dbfe922461083b49d77ad2351e98d562d3b
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106535786"
---
# <a name="topology-attributes"></a>Attributs de topologie

Les attributs suivants s’appliquent aux topologies.



| Attribut                                                                                                | Description                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_ \_ mode DXVA de topologie \_ MF](mf-topology-dxva-mode.md)                                                    | Spécifie si le chargeur de topologie Active l’accélération vidéo Microsoft DirectX (DXVA) dans la topologie.                                                                                                                         |
| [\_modification dynamique de la topologie MF \_ \_ \_ non \_ autorisée](mf-topology-dynamic-change-not-allowed.md)                | Spécifie si la session multimédia tente de modifier la topologie lorsque le format d’un flux de contenu change.                                                                                                                           |
| [\_la topologie MF \_ active \_ XVP \_ pour \_ la lecture](mf-topology-enable-xvp-for-playback.md)                | Spécifie si le chargeur de topologie Active le processeur vidéo de transcodage (XVP). pour les conversions, activation de la conversion des couleurs à accélération matérielle.                                                                                        |
| [\_topologie MF \_ énumérer les \_ types de sources \_](mf-topology-enumerate-source-types.md)                         | Spécifie si le chargeur de topologie énumère les types de médias fournis par la source du média.                                                                                                                                     |
| [\_ \_ mode matériel de la topologie MF \_](mf-topology-hardware-mode.md)                                            | Spécifie s’il faut inclure des transformations basées sur le matériel dans la topologie.                                                                                                                                                            |
| [**\_topologie MF \_ aucune \_ marque \_ MARKOUT**](mf-topology-no-markin-markout-attribute.md)                     | Spécifie si le pipeline tronque les exemples.                                                                                                                                                                                      |
| [\_fréquence de lecture de \_ la topologie MF \_](mf-topology-playback-framerate.md)                                  | Spécifie la fréquence d’actualisation du moniteur.                                                                                                                                                                                                |
| [\_ \_ nombre maximal de lectures de la topologie \_ MF \_](mf-topology-playback-max-dims.md)                                   | Spécifie la taille de la fenêtre de destination pour la lecture vidéo.                                                                                                                                                                   |
| [**\_PROJECTSTART de topologie \_ MF**](mf-topology-projectstart-attribute.md)                                 | Spécifie l’heure de début de la topologie dans le segment actuel, en unités de 100 nanosecondes.                                                                                                                                             |
| [**\_PROJECTSTOP de topologie \_ MF**](mf-topology-projectstop-attribute.md)                                   | Spécifie l’heure d’arrêt de la topologie dans le segment actuel, en unités de 100 nanosecondes.                                                                                                                                              |
| [**État de résolution de la \_ topologie MF \_ \_**](mf-topology-resolution-status-attribute.md)                      | Spécifie l’état d’une tentative de résolution d’une topologie.                                                                                                                                                                          |
| [\_ \_ heure de début de la topologie MF \_ \_ sur le \_ commutateur de présentation \_](mf-topology-start-time-on-presentation-switch.md) | Spécifie l’heure de début des présentations mises en file d’attente après la première présentation.                                                                                                                                           |
| [\_ \_ \_ optimisations de la lecture statique de la topologie MF \_](mf-topology-static-playback-optimizations.md)           | Active les optimisations statiques dans le pipeline vidéo.                                                                                                                                                                                |
| [\_Attribut de \_ déverrouillage MFT FIELDOFUSE \_](mft-fieldofuse-unlock-attribute.md)                                | Contient un pointeur [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , utilisé pour déverrouiller une table MFT avec des restrictions de champ d’utilisation. Pour plus d’informations, consultez [restrictions relatives au champ d’utilisation](field-of-use-restrictions.md). |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> </dl>

 

 



