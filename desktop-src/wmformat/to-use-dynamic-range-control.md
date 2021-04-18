---
title: Pour utiliser le contrôle de plage dynamique
description: Pour utiliser le contrôle de plage dynamique
ms.assetid: 719658c1-952f-4e8f-a3ea-bdf89a0a7268
keywords:
- Kit de développement logiciel (SDK) Windows Media format, contrôle de plage dynamique
- SDK du format Windows Media, codec Windows Media Audio 9 professionnel
- Windows Media Format SDK, Windows Media Audio 9 codec sans perte
- Format ASF (Advanced Systems Format), codec Windows Media Audio 9 professionnel
- ASF (format des systèmes avancés), codec Windows Media Audio 9 professionnel
- ASF (Advanced Systems Format), codec Windows Media Audio 9 sans perte
- ASF (format des systèmes avancés), codec Windows Media Audio 9 sans perte
- ASF (Advanced Systems Format), contrôle de plage dynamique
- ASF (format de systèmes avancés), contrôle de plage dynamique
- contrôle de plage dynamique
- codecs, codec Windows Media Audio 9 sans perte
- codecs, codec Windows Media Audio 9 professionnel
- Codec Windows Media Audio 9 sans perte, contrôle de plage dynamique
- Codec Windows Media Audio 9 Professional, contrôle de plage dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077ebc0052d0154aec395f371a5c2dc3ffd46c67
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511874"
---
# <a name="to-use-dynamic-range-control"></a>Pour utiliser le contrôle de plage dynamique

La plage dynamique d’une partie du contenu audio correspond fondamentalement à la différence entre le volume le plus bas et le volume maximal. Si la plage dynamique du contenu est trop élevée, les utilisateurs peuvent être amenés à ajuster le volume à plusieurs reprises lors de la lecture. Par exemple, les films ont souvent une plage dynamique élevée. Souvent, lorsque le volume est ajusté pour que la boîte de dialogue puisse être comprise pendant les scènes calmes, d’autres parties du film avec des effets sonores ou musicaux sont plus intenses que nécessaire.

Les codecs Windows Media Audio 9 Professional et Windows Media Audio 9 Lossless prennent en charge une fonctionnalité appelée contrôle de plage dynamique. Au moment de l’encodage, le codec calcule le pic et les valeurs d’amplitude moyennes dans le contenu, et l’objet enregistreur stocke ces valeurs dans les métadonnées du flux lorsque l’encodage est terminé. Éventuellement, une application peut également écrire des valeurs « cibles » en tant que métadonnées que les applications de lecteur et le décodeur peuvent utiliser comme indications lors de la lecture du fichier. Au moment de la lecture, une application peut spécifier le niveau de contrôle de plage dynamique à appliquer au flux audio.

Le lecteur Windows Media implémente le contrôle de plage dynamique comme fonctionnalité en mode silencieux.

## <a name="when-to-use-dynamic-range-control"></a>Quand utiliser le contrôle de plage dynamique

Le contrôle de plage dynamique peut altérer le son du contenu. Pour cette raison, vous ne devez pas configurer votre application pour qu’elle utilise automatiquement le contrôle de plage dynamique. Au lieu de cela, fournissez aux utilisateurs la possibilité d’activer ou de désactiver le contrôle de plage dynamique selon les besoins.

## <a name="using-dynamic-range-control"></a>Utilisation du contrôle de plage dynamique

Au moment de la lecture, le contrôle de plage dynamique est activé à l’aide du paramètre de sortie g \_ wszDynamicRangeControl. Utilisez [**IWMReaderAdvanced2 :: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) pour configurer le paramètre. La valeur zéro (valeur par défaut) indique que la plage dynamique ne doit pas être modifiée. La valeur 1 ou 2 indique au codec d’effectuer un contrôle de plage dynamique, où 1 est un niveau modéré de compression de plage dynamique, et 2 un niveau élevé de compression de plage dynamique.

Au moment de l’encodage ou de l’heure de lecture, vous pouvez définir les valeurs PCM de la cible du codec pour les niveaux PIC et moyenne en définissant respectivement les attributs [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md) et [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md) . Ces valeurs sont stockées sous la forme d’attributs de métadonnées et doivent être accessibles à l’aide des méthodes de l’interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) . Lorsque vous encodez un flux audio à l’aide du codec Professional ou Lossless, les attributs [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md) et [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md) sont définis automatiquement sur les niveaux PIC et moyenne du contenu d’origine. Les valeurs cibles sont définies sur les mêmes valeurs que les références par défaut.

Le décodeur au moment de la lecture calcule la plage dynamique en fonction du niveau sélectionné du contrôle de plage dynamique et des valeurs cibles (si elles sont spécifiées). Les plages possibles sont indiquées dans le tableau suivant.



| Paramètres                                                                | Plage de données audio livrées                                                                                                     |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDynamicRangeControl = 0 (toutes les valeurs cibles)                       | Même plage que le contenu d’origine.                                                                                          |
| g \_ wszDynamicRangeControl = 1 (valeurs cibles égales aux valeurs de référence) | Le niveau moyen est conservé et les pics sont limités à la moyenne + 12 dB.                                                    |
| g \_ wszDynamicRangeControl = 2 (valeurs cibles égales aux valeurs de référence) | Le niveau moyen est maintenu et les pics sont limités à la moyenne + 6 dB.                                                     |
| g \_ wszDynamicRangeControl = 1 (valeurs cibles spécifiées)                 | Niveau moyen défini sur la valeur moyenne cible et les pics limités à la valeur de pic cible.                                   |
| g \_ wszDynamicRangeControl = 2 (valeurs cibles spécifiées)                 | Niveau moyen défini sur la valeur moyenne cible et les pics limités à la valeur médiane de la moyenne cible et des valeurs maximales cibles. |



 

Notez que le contrôle de plage dynamique est une fonctionnalité de décodage uniquement et qui existe uniquement en tant que métadonnées dans le fichier lui-même. Ces paramètres n’ont aucun effet sur le contenu stocké dans le fichier, sauf si vous indiquez spécifiquement au décodeur de les utiliser. Le kit de développement logiciel (SDK) du format Windows Media ne fournit aucune méthode de modification de la plage dynamique des données audio au moment de l’encodage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Rubriques avancées**](advanced-topics.md)
</dt> </dl>

 

 




