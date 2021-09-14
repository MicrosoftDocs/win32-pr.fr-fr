---
description: Attributs de nœud de topologie
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Attributs de nœud de topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904213752c0a3444bc4c9ea2b5cf2d5c21c8bd83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235865"
---
# <a name="topology-node-attributes"></a>Attributs de nœud de topologie

Les attributs suivants s’appliquent aux nœuds de topologie.

## <a name="general-topology-node-attributes"></a>Attributs généraux de nœud de topologie



| Attribut                                                                       | Description                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_méthode de \_ connexion MF TOPONODE \_**](mf-toponode-connect-method-attribute.md)   | Spécifie comment le chargeur de topologie connecte ce nœud de topologie et si ce nœud est facultatif.                                                        |
| [**\_DÉcodeur TOPONODE MF \_**](mf-toponode-decoder-attribute.md)                  | Spécifie si l’objet d’un nœud topologie est un décodeur.                                                                                                  |
| [**\_déchiffreur MF TOPONODE \_**](mf-toponode-decryptor-attribute.md)              | Spécifie si l’objet sous-jacent d’un nœud topologie est un déchiffreur.                                                                                     |
| [**TOPONODE MF à \_ \_ Ignorer**](mf-toponode-discardable-attribute.md)          | Spécifie si le pipeline peut supprimer des exemples d’un nœud de topologie.                                                                                    |
| [**\_erreur TOPONODE \_ MF \_ MAJORTYPE**](mf-toponode-error-majortype-attribute.md) | Contient le type de média principal pour un nœud de topologie. Cet attribut est défini lorsque le chargement de la topologie échoue car le décodeur approprié est introuvable. |
| [**\_sous- \_ type d’erreur TOPONODE MF \_**](mf-toponode-error-subtype-attribute.md)     | Contient le sous-type de média pour un nœud de topologie. Cet attribut est défini lorsque le chargement de la topologie échoue car le décodeur approprié est introuvable.    |
| [**MF \_ TOPONODE \_ ERRORCODE**](mf-toponode-errorcode-attribute.md)              | Contient le code d’erreur de l’échec de connexion le plus récent pour ce nœud de topologie.                                                                  |
| [**\_TOPONODE MF \_ verrouillé**](mf-toponode-locked-attribute.md)                    | Spécifie si les types de média peuvent être modifiés sur ce nœud de topologie.                                                                                  |
| [**\_Mark MF TOPONODE \_ \_ ici**](mf-toponode-markin-here-attribute.md)         | Spécifie si le pipeline applique la marque dans ce nœud.                                                                                             |
| [**\_MARKOUT TOPONODE \_ MF \_ ici**](mf-toponode-markout-here-attribute.md)       | Spécifie si le pipeline applique le marquage sur ce nœud.                                                                                            |



 

## <a name="source-node-attributes"></a>Attributs du nœud source



| Attribut                                                                                       | Description                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**\_MEDIASTART TOPONODE \_ MF**](mf-toponode-mediastart-attribute.md)                            | Spécifie l’heure de début d’une présentation, par rapport au démarrage du fichier source du média, en unités de 100 nanosecondes. |
| [**\_MEDIASTOP TOPONODE \_ MF**](mf-toponode-mediastop-attribute.md)                              | Spécifie l’heure d’arrêt d’une présentation, par rapport au démarrage du fichier source du média, en unités de 100 nanosecondes.  |
| [**\_descripteur de présentation TOPONODE MF \_ \_**](mf-toponode-presentation-descriptor-attribute.md) | Contient un pointeur vers le descripteur de présentation pour la source du média.                                           |
| [**\_séquence d’TOPONODE de \_ SÉQUENCEs MF \_**](mf-toponode-sequence-elementid-attribute.md)           | Spécifie l’élément qui contient un nœud source.                                                                |
| [**\_source TOPONODE \_ MF**](mf-toponode-source-attribute.md)                                    | Contient un pointeur vers la source du média associée à un nœud de topologie.                                           |
| [**\_descripteur de flux TOPONODE MF \_ \_**](mf-toponode-stream-descriptor-attribute.md)             | Contient un pointeur vers le descripteur de flux pour la source du média.                                                 |
| [**\_ID de \_ WORKQUEUE \_ TOPONODE MF**](mf-toponode-workqueue-id-attribute.md)                       | Spécifie une file d’attente de travail pour un nœud de topologie.                                                                       |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS, \_ classe**](mf-toponode-workqueue-mmcss-class-attribute.md)    | Spécifie une tâche du service Planificateur de classes multimédias (MMCSS) pour un nœud de topologie.                                  |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | Spécifie un identificateur de tâche MMCSS pour un nœud de topologie.                                                            |



 

## <a name="transform-node-attributes"></a>Attributs du nœud transformer



| Attribut                                                                             | Description                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**\_D3DAWARE TOPONODE \_ MF**](mf-toponode-d3daware-attribute.md)                      | Spécifie si la transformation associée à un nœud de topologie prend en charge l’accélération vidéo DirectX (DXVA) |
| [**\_drainage TOPONODE \_ MF**](mf-toponode-drain-attribute.md)                            | Spécifie quand une transformation est vidée.                                                                     |
| [**\_vidage TOPONODE \_ MF**](mf-toponode-flush-attribute.md)                            | Spécifie quand une transformation est vidée.                                                                     |
| [**\_ID d’TOPONODE de \_ transformation MF \_**](mf-toponode-transform-objectid-attribute.md) | Identificateur de classe (CLSID) de la transformation associée à ce nœud de topologie.                          |



 

## <a name="output-node-attributes"></a>Attributs du nœud de sortie



| Attribut                                                                                  | Description                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**\_TOPONODE de \_ désactiver le \_ préroll MF**](mf-toponode-disable-preroll-attribute.md)            | Spécifie si la session multimédia utilise le préroll sur le récepteur multimédia représenté par ce nœud de topologie.            |
| [**\_TOPONODE \_ de l’infermeture MF en cas \_ de \_ suppression**](mf-toponode-noshutdown-on-remove-attribute.md) | Spécifie si la session multimédia arrête le récepteur multimédia lorsque le nœud de sortie est supprimé de la topologie. |
| [**\_TOPONODE de \_ Vitesse MF**](mf-toponode-rateless-attribute.md)                           | Spécifie si le récepteur multimédia associé à ce nœud de topologie est sans débit.                                 |
| [**\_STREAMID TOPONODE \_ MF**](mf-toponode-streamid-attribute.md)                           | Identificateur de flux du récepteur de flux associé à ce nœud de topologie.                                     |



 

## <a name="tee-node-attributes"></a>Attributs du nœud tee



| Attribut                                                                  | Description                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [**\_PrimaryOutput, car TOPONODE \_ MF**](mf-toponode-primaryoutput-attribute.md) | Indique quelle sortie est la sortie principale sur un nœud tee. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Attributs de topologie](topology-attributes.md)
</dt> </dl>

 

 



