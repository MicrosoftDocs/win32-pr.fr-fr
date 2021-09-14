---
description: Cette section décrit comment écrire une transformation de Media Foundation personnalisée (MFT).
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Écriture d’une table MFT personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c113867c719fc9c8512b5b0e1172ee0694e3905
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313513"
---
# <a name="writing-a-custom-mft"></a>Écriture d’une table MFT personnalisée

Cette section décrit comment écrire une transformation de Media Foundation personnalisée (MFT).

## <a name="mft-checklist"></a>Liste de contrôle MFT

Lorsque vous implémentez une table MFT personnalisée, utilisez la liste de vérification suivante pour déterminer les conditions requises :




| | | Toutes les MFTs | Toutes les MFTs doivent implémenter <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.<br /> Les rubriques suivantes fournissent plus d’informations sur l’implémentation de cette interface :<ul><li><a href="basic-mft-processing-model.md">Modèle de traitement MFT de base</a></li><li><a href="time-stamps-and-durations.md">Horodatages et durées</a></li><li><a href="handling-stream-changes.md">Gestion des modifications de flux</a></li></ul><br /> | | Encodeurs et décodeurs | Configuration requise : consultez <a href="implementing-a-codec-mft.md">implémentation d’une table MFT de codec</a>.<br /> Recommandé : implémentez <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> ou <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>pour prendre en charge les notifications de qualité de service (QoS).<br /> | | Décodeurs vidéo et processeurs vidéo | Facultatif : prendre en charge l’accélération vidéo DirectX.<br /><ul><li><a href="direct3d-aware-mfts.md">MFTs compatible Direct3D</a></li><li><a href="supporting-dxva-2-0-in-media-foundation.md">Prise en charge de DXVA 2,0 dans Media Foundation</a></li></ul> | | Codecs matériels | Voir <a href="hardware-mfts.md">matériel MFTS</a>. | | Pour rendre votre MFT détectable par les applications... | Consultez la page <a href="registering-and-enumerating-mfts.md">inscription et énumération de MFTS</a>. | | Traitement asynchrone des données | Le modèle MFT par défaut utilise des appels synchrones (bloquant) pour traiter les données. Pour certains MFTs, le traitement asynchrone peut être plus efficace. Toutefois, il est également plus complexe à implémenter.<br /> Pour plus d’informations, consultez <a href="asynchronous-mfts.md">MFTS asynchrone</a>.<br /> | | Contrôle de la fréquence, mode de pli ou lecture inversée | Consultez <a href="implementing-rate-control.md">Implementing Rate Control</a>. | | Si votre MFT crée des threads... | Implémentez l’interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> . | | Si votre MFT a des restrictions de licence... | Envisagez d’utiliser le mécanisme de champ d’utilisation. Consultez <a href="field-of-use-restrictions.md">restrictions relatives au champ d’utilisation</a>. | | Si vous portez un objet multimédia DirectX existant (DMO)... | Consultez <a href="comparison-of-mfts-and-dmos.md">comparaison entre MFTS et DMOs</a>. | 




 

Cette section contient les rubriques suivantes :

-   [Horodatages et durées](time-stamps-and-durations.md)
-   [Gestion des modifications de flux](handling-stream-changes.md)
-   [Implémentation d’une table MFT de codec](implementing-a-codec-mft.md)
-   [MFTs compatible Direct3D](direct3d-aware-mfts.md)
-   [Matériel MFTs](hardware-mfts.md)
-   [Mérite du codec](codec-merit.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




