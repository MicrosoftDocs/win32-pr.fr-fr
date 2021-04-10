---
description: Correspondance opérationnelle avec le pilote de périphérique de compensation de mouvement
ms.assetid: bd92a0f4-98d9-497a-99b9-0cf432347daf
title: Correspondance opérationnelle avec le pilote de périphérique de compensation de mouvement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cca960ed8cbdae212bbe5e9f3b25316125a7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200706"
---
# <a name="operational-correspondence-with-motion-compensation-device-driver"></a>Correspondance opérationnelle avec le pilote de périphérique de compensation de mouvement

Cette section contient une description du côté pilote de périphérique de compensation de mouvement de l’interface DirectX VA. (Référence : Windows 2000 DDK-pilotes graphiques-Guide de conception-3,0 DirectDraw DDI-3,12 Motion compensation. Consultez le kit DDK Windows pour obtenir de la documentation sur les structures en caractères gras.)

Les éléments suivants font référence aux entrées accessibles via la structure **DD \_ MOTIONCOMPCALLBACKS** :

1.  Au début du traitement concerné, le **DdMoCompCreate** du pilote de périphérique est utilisé pour notifier au pilote que le décodeur logiciel va démarrer à l’aide d’un objet d’accélération vidéo.
2.  Les GUID reçus à partir de [**IAMVideoAccelerator :: GetVideoAcceleratorGUIDs**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) proviennent du **DdMoCompGetGUIDs** du pilote de périphérique.
3.  Un appel à la méthode [**IAMVideoAccelerator :: GetUncompFormatsSupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) du pin d’entrée en aval retourne les données du **DdMoCompGetFormats** du pilote de périphérique.
4.  La \_ structure de données DXVA connectMode du décodeur [**IAMVideoAcceleratorNotify :: GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) est transmise au **DdMoCompCreate** du pilote de périphérique.
5.  Les données retournées par [**IAMVideoAccelerator :: GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo) proviennent du **DdMoCompGetBuffInfo** du pilote de périphérique.
6.  Les mémoires tampons envoyées à l’aide de [**IAMVideoAccelerator :: Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) sont reçues par le **DdMoCompRender** du pilote de périphérique.
7.  L’utilisation de [**IAMVideoAccelerator :: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) appelle le **DdMoCompQueryStatus** du pilote de périphérique. Un code de retour de DDERR \_ WASSTILLDRAWING de DdMoCompQueryStatus sera vu par le décodeur hôte comme un code de retour E \_ en attente à partir de **IAMVideoAccelerator :: QueryRenderStatus**.
8.  Les données envoyées à [**IAMVideoAccelerator :: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) sont reçues par le **DdMoCompBeginFrame** du pilote de périphérique. Un code de retour de E \_ en attente est nécessaire à partir de DdMoCompBeginFrame pour \_ que e soit visible par le décodeur hôte en réponse à **IAMVideoAccelerator :: BeginFrame**.
9.  Les données envoyées à [**IAMVideoAccelerator :: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) sont reçues par le **DdMoCompEndFrame** du pilote de périphérique.
10. À la fin du traitement approprié, le **DdMoCompDestroy** du pilote de périphérique est utilisé pour notifier au pilote que l’objet d’accélération vidéo actuel n’est plus utilisé, afin que le pilote puisse effectuer tout nettoyage nécessaire.

 

 



