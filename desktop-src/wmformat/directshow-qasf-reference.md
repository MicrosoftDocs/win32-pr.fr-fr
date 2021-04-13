---
title: Informations de référence sur DirectShow QASF
description: Informations de référence sur DirectShow QASF
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- Windows Media Format SDK, QASF
- Windows Media Format SDK, DirectShow
- DirectShow, référence QASF
- Filtres QASF, référence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c509030f676b83a84f67590a242aea623656a514
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382275"
---
# <a name="directshow-qasf-reference"></a>Informations de référence sur DirectShow QASF

Cette section contient des références de programmation pour les filtres, interfaces et énumérations QASF DirectShow suivants. La documentation du kit de développement logiciel (SDK) DirectShow contient des documents de guide de référence et de programmation pour les interfaces génériques supplémentaires exposées par ces filtres, tels que **IBaseFilter** et **IPIN**, ainsi que pour les versions antérieures des composants qasf.

Pour obtenir une explication du nom de QASF, consultez [à propos de DirectShow](about-directshow.md).

Les filtres suivants sont inclus avec les composants DirectShow QASF.



| Filtrer                                           | Description                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [Filtre de lecteur ASF WM](wm-asf-reader-filter.md) | Lit et analyse les fichiers ASF locaux ou distants.                      |
| [Filtre d’enregistreur ASF WM](wm-asf-writer-filter.md) | Crée des fichiers ASF à partir de flux d’entrée compressés ou non compressés. |



 

Les interfaces suivantes sont définies pour une utilisation avec les composants DirectShow QASF.



| Interface                                                  | Description                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | Fournit une méthode qui permet aux applications de s’inscrire pour les rappels à partir des broches d’entrée de l' [enregistreur ASF WM](wm-asf-writer-filter.md) ou des broches de sortie du filtre de [lecteur ASF WM](wm-asf-reader-filter.md) . Utilisé dans l’indexation et lors de l’ajout d’extensions d’unité de données. |
| [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | Implémentée par les applications et appelée par les filtres. Les applications utilisent la méthode une sur cette interface pour obtenir des informations sur des échantillons individuels dans le flux. Utilisé dans l’indexation et lors de l’ajout d’extensions d’unité de données.                                                 |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))               | Implémenté sur le writer WM ASF. Utilisé par les applications pour spécifier des profils et des paramètres d’indexation pour le fichier.                                                                                                                                                              |
| [**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))             | Fournit des fonctions de configuration supplémentaires sur le writer WM ASF.                                                                                                                                                                                                             |



 

L’énumération, la structure et les événements suivants sont définis pour être utilisés avec les composants DirectShow QASF.



| Énumération                                                               | Description                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_\_paramètre am ASFWRITERCONFIG \_](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) | Définit les paramètres de configuration de filtre utilisés dans les méthodes [**IConfigAsfWriter2 :: GetParam**](iconfigasfwriter2-getparam.md) et [**setParam**](iconfigasfwriter2-setparam.md) . |



 



| Structure                                         | Description                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_données d' \_ événement \_ WMT AM**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | Contient des informations relatives à un événement d' [**\_ État WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) et au code d’état associé renvoyé par le kit de développement logiciel (SDK) du format Windows Media. |



 



| Événement                                           | Description                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [\_événement EC WMT \_](ec-wmt-event.md)              | Événement transféré à partir du kit de développement logiciel (SDK) du format Windows Media.                                                              |
| [événement d’index de l’WMT de la EC \_ \_ \_](ec-wmt-index-event.md) | Envoyé lorsqu’une application utilise le [writer ASF](wm-asf-writer-filter.md) pour indexer les fichiers Windows Media Video. |



 

 

 