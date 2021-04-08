---
title: Pour utiliser la vidéo entrelacée
description: Pour utiliser la vidéo entrelacée
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- Windows Media Format SDK, vidéo entrelacée
- Windows Media Format SDK, encodage vidéo entrelacé
- Windows Media Format SDK, encodage vidéo entrelacée
- Windows Media Format SDK, décodage vidéo entrelacée
- Windows Media Format SDK, ordre des champs
- ASF (Advanced Systems Format), vidéo entrelacée
- ASF (format des systèmes avancés), vidéo entrelacée
- ASF (Advanced Systems Format), encodage vidéo entrelacé
- ASF (format des systèmes avancés), encodage vidéo entrelacé
- ASF (Advanced Systems Format), encodage vidéo entrelacée
- ASF (format avancé des systèmes), encodage d’une vidéo entrelacée
- ASF (Advanced Systems Format), décodage de vidéo entrelacée
- ASF (format de systèmes avancés), décodage de vidéo entrelacée
- ASF (Advanced Systems Format), ordre des champs
- ASF (format des systèmes avancés), ordre des champs
- vidéo entrelacée, à propos de
- vidéo entrelacée, encodage
- vidéo entrelacée, décodage
- vidéo entrelacée, ordre des champs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841901"
---
# <a name="to-use-interlaced-video"></a>Pour utiliser la vidéo entrelacée

Il existe deux types de codage vidéo de base : progressif et entrelacé. Dans l’encodage progressif, chaque frame est une représentation encodée d’un cadre de vidéo. Dans l’encodage entrelacé, chaque frame est une représentation encodée de toutes les lignes paires de pixels dans la vidéo, ou de toutes les lignes impaires. Chaque trame entrelacée étant appelée un *champ*, il y a des champs impairs et même des champs. Un affichage entrelacé (comme une télévision) restitue les champs un par un, en alternant les champs. Un affichage progressif affiche tous les frames à la fois.

Le codec de profil avancé Windows Media Video 9 assure la prise en charge de la gestion de l’entrelacement dans les flux compressés.

## <a name="when-to-use-interlaced-video"></a>Quand utiliser la vidéo entrelacée

L’encodage d’une vidéo entrelacée est utile uniquement lorsque le contenu est affiché sur un appareil entrelacé. Le contenu destiné à être affiché sur une télévision (par le biais d’un boîtier décodeur ou d’un autre périphérique) doit peut-être être entrelacé. Le contenu destiné à être affiché exclusivement sur un écran d’ordinateur ne doit pas être encodé comme entrelacé.

Pour encoder une vidéo entrelacée comme vidéo progressive, vous devez configurer les paramètres d’entrée. Pour plus d’informations, consultez [pour libérer de la vidéo](to-deinterlace-video.md).

## <a name="field-order"></a>Ordre des champs

La plupart des sources de vidéo entrelacées, telles que les cartes de capture vidéo, fournissent des exemples de vidéos qui incluent les deux champs entrelacés les uns avec les autres. Le résultat ressemble à une image complète de la vidéo, sauf que les lignes paires et impaires sont décalées légèrement dans le temps. Il n’existe pas de norme universelle quant au champ dans lequel l’exemple de vidéo entrelacée se produit pour la première fois.

Vous devez permettre aux utilisateurs de spécifier l’ordre des champs lors du passage d’échantillons entrelacés à votre application.

## <a name="encoding-interlaced-video"></a>Encodage d’une vidéo entrelacée

Pour utiliser l’encodage entrelacé, procédez comme suit :

1.  Configurez le flux vidéo dans le profil pour utiliser l’extension d’unité de données de type de contenu en appelant la méthode [**IWMStreamConfig2 :: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) . L’exemple de GUID d’extension pour l’extension de type de contenu est WM \_ SampleExtensionsGUID \_ ContentType.
2.  Définissez le flux dans le profil et configurez l’enregistreur avec le profil comme d’habitude.
3.  Avant de transmettre des échantillons entrelacés au writer, appelez la méthode [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) pour définir le \_ paramètre d’entrée g wszInterlacedCoding sur **true**.
4.  Pour chaque échantillon entrelacé que vous transmettez au writer, appelez la méthode [**INSSBuffer3 :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) pour définir le type de contenu. Les valeurs de type de contenu sont des combinaisons des indicateurs dans le tableau suivant.



| Indicateur                         | Description                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ CT \_ entrelacé           | Définissez toujours cet indicateur lors de l’encodage du contenu entrelacé. Si vous utilisez cet indicateur sans avoir à définir un indicateur d’ordre de champ (le champ WM WM en \_ \_ bas \_ \_ ou \_ \_ le champ supérieur WM CT en \_ \_ premier), le codec suppose que le champ supérieur est tout d’abord. Si le codec utilise un mauvais ordre des champs, il ne doit pas y avoir d’impact sur la qualité de l’image, mais l’efficacité de l’encodage sera affectée. |
| \_champ inférieur WM CT en \_ \_ \_ premier | Lorsqu’il est combiné avec l' \_ indicateur WM CT \_ entrelacé, cet indicateur indique que le champ du bas (le champ commençant par la deuxième ligne de l’exemple) se produit en premier dans le temps.                                                                                                                                                                                          |
| \_champ supérieur WM CT en \_ \_ \_ premier    | Lorsqu’il est combiné avec l' \_ indicateur WM CT \_ entrelacé, cet indicateur indique que le champ supérieur (le champ commençant par la première ligne de l’exemple) se produit en premier dans le temps.                                                                                                                                                                                              |
| WM \_ CT- \_ répéter le \_ premier \_ champ | Indique que le premier champ de l’échantillon doit être répété lors de la lecture. Cet indicateur est utilisé pour la vidéo qui a été créée à partir d’un film par le processus de télécinéma. Si aucun indicateur d’ordre de champ n’est défini conjointement avec cet indicateur, le champ supérieur est supposé se produire en premier dans le temps.<br/>                                                                             |



 

> [!Note]  
> Si l' \_ \_ indicateur de l’entrelacement WM CT n’est pas défini, l’échantillon est supposé contenir une image vidéo progressive.

 

## <a name="decoding-interlaced-video"></a>Décodage d’une vidéo entrelacée

Lors du décodage d’une vidéo entrelacée, vous devez affecter la \_ **valeur true** au paramètre g wszAllowInterlacedOutput à l’aide de la méthode [**IWMReaderAdvanced2 :: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) . Dans le cas contraire, le codec fournira des trames progressives.

L’extension d’unité de données de type de contenu est conservée dans les exemples de sortie. Vous devez passer l’orientation du champ à l’appareil de rendu pour garantir une lecture correcte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Rubriques avancées**](advanced-topics.md)
</dt> </dl>

 

 





