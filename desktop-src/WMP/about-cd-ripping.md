---
title: À propos de l’extraction de CD
description: À propos de l’extraction de CD
ms.assetid: 1a179284-2909-4fc0-82be-996794ee4f31
keywords:
- Lecteur Windows Media, extraction de CD
- modèle d’objet Lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- contrôle de ActiveX Lecteur Windows Media, extraction de CD
- contrôle de ActiveX, extraction de CD
- Lecteur Windows Media contrôle de ActiveX Mobile, extraction de CD
- Lecteur Windows Media Mobile, extraction de CD
- Extraction de CD, à propos de
- extraction de CD, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efab14a97f9cc24c4137e5d939bc9562b1fc073cd551bd83388de4ba1de0b65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903599"
---
# <a name="about-cd-ripping"></a>À propos de l’extraction de CD

le kit de développement logiciel (SDK) Lecteur Windows Media 11 introduit de nouvelles fonctionnalités pour copier les pistes audio des cd sur l’ordinateur de l’utilisateur. Ce processus est appelé *extraction*.

lorsque vous extrayez des pistes audio à l’aide des interfaces du kit de développement logiciel (SDK) Lecteur Windows Media, les pistes de musique qui en résultent sont créées à l’aide des paramètres définis par l’utilisateur dans la boîte de dialogue **Options** de Lecteur Windows Media.

Pour énumérer les lecteurs de CD sur l’ordinateur de l’utilisateur, utilisez l’interface **IWMPCdromCollection** . Vous récupérez un pointeur vers cette interface en appelant [IWMPCore :: obtenir \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). En utilisant les méthodes **Count** et **Item** , vous pouvez effectuer une itération de la collection pour récupérer un pointeur d’interface **IWMPCDROM** pour chaque lecteur de CD sur l’ordinateur de l’utilisateur. L’interface **IWMPCdrom** représente un lecteur de CD individuel. Avant de commencer l’extraction d’un CD, vous devez d’abord appeler **QueryInterface** à l’aide d’un pointeur **IWMPCdrom** pour récupérer un pointeur vers l’interface **IWMPCdromRip** .

Pour démarrer l’opération d’extraction, appelez simplement [IWMPCdromRip :: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip). Vous pouvez surveiller la progression de l’opération d’extraction en appelant périodiquement [IWMPCdromRip :: obten \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Cette méthode récupère une valeur de progression pour l’opération d’extraction entière. La valeur récupérée est un nombre qui représente le pourcentage d’extraction terminée. Vous pouvez surveiller l’état de l’opération d’extraction en appelant périodiquement [IWMPCdromRip :: obten \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Cette méthode récupère une valeur d’énumération [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) qui indique si l’opération est en cours ou arrêtée. Vous pouvez également surveiller l’état de l’opération d’extraction en gérant l’événement [IWMPEvents3 :: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) . Veillez à comparer le pointeur **IWMPCdromRip** (fourni par l’événement) au pointeur qui représente votre opération d’extraction pour vous assurer que l’événement a été déclenché par votre opération. Vous pouvez arrêter l’opération d’extraction en appelant [IWMPCdromRip :: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).

Pour recevoir des notifications d’erreur relatives à une opération d’extraction, vous pouvez gérer l’événement [IWMPEvents3 :: CdromRipMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) . Comme **CdromRipStateChange**, cet événement fournit un pointeur d’interface **IWMPCdromRip** qui représente l’opération d’extraction qui a déclenché l’événement. L’événement fournit également un pointeur **IDispatch** qui représente l’élément multimédia qui a déclenché l’événement. Vous pouvez appeler **QueryInterface** via ce pointeur pour récupérer un pointeur **IWMPMedia** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du modèle objet Player**](about-the-player-object-model.md)
</dt> </dl>

 

 




