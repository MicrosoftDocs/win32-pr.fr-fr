---
title: Pour désentrelacer une vidéo
description: Pour désentrelacer une vidéo
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- Windows Media Format SDK, vidéo désentrelacée
- Windows Media Format SDK, inversement Telecine
- Windows Media Format SDK, Telecine
- ASF (Advanced Systems Format), vidéo désentrelacée
- ASF (format des systèmes avancés), vidéo désentrelacée
- ASF (Advanced Systems Format), inversement
- ASF (format avancé des systèmes), inversement
- ASF (Advanced Systems Format), télécinéma
- ASF (format avancé des systèmes), télécinéma
- vidéo désentrelacée
- inverser Telecine, à propos de
- télécinéma, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ef1d1a6fcee3bf43d2fb4451d4ef129e595471e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475765"
---
# <a name="to-deinterlace-video"></a>Pour désentrelacer une vidéo

Certaines sources de vidéo, telles que les cartes de capture vidéo, fournissent des données vidéo pour l’affichage entrelacé. Chaque image de vidéo entrelacée est composée de deux champs. Le champ du haut contient la première ligne de vidéo et chaque ligne suivante. Le champ du bas contient la deuxième ligne de vidéo et chaque ligne suivante. Par conséquent, un champ contient toutes les lignes paires numérotées et l’autre contient toutes les lignes impaires. Les champs qui composent un cadre représentent des temps de présentation légèrement différents afin que, lorsqu’ils sont entrelacés, ils ne forment pas une image statique.

Lorsque vous souhaitez afficher une vidéo sur un moniteur d’ordinateur, chaque image de la vidéo doit être affichée sous la forme d’une image (cette méthode d’affichage de la vidéo d’une image complète à la fois est appelée vidéo *progressive* .) Si vous affichez des vidéos entrelacées de façon progressive, les frames peuvent ne pas s’afficher correctement, en raison de la différence de temps entre les deux champs. le codec Windows Media Video et le codec de profil avancé Windows Media Video prennent tous deux en charge une fonctionnalité de prétraitement qui convertit le contenu entrelacé en images progressives.

Pour que le codec désentrelace la vidéo d’entrée, appelez la méthode [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) . Le paramètre à utiliser est g \_ wszDeinterlaceMode. Définissez le mode de désentrelacement sur l’une des valeurs suivantes.




| Valeur | Description | 
|-------|-------------|
| WM_DM_NOTINTERLACED | L’entrée est progressive. Utilisez ce paramètre pour arrêter l’entrelacement lorsque vous avez précédemment défini le mode de désentrelacement sur une autre valeur. | 
| WM_DM_DEINTERLACE_NORMAL | Sélectionnez ce mode pour fusionner les champs pairs et impairs d’un cadre entrelacé (à l’aide d’un mécanisme de compensation de mouvement). Avantageuse<br /><ul><li>Les artefacts entrelacés de l’affichage progressif sont considérablement réduits.</li><li>le codec Windows Media Video produit une vidéo compressée de qualité supérieure.</li></ul> | 
| WM_DM_DEINTERLACE_HALFSIZE | Sélectionnez ce mode lorsque la résolution de sortie est inférieure ou égale à la résolution d’entrée. Par exemple, utilisez ce mode lorsque la résolution vidéo d’entrée est de 640 x 480 pixels et que la résolution vidéo de sortie est de 320 x 240 pixels. Avantageuse<br /><ul><li>Les artefacts entrelacés de l’affichage progressif sont considérablement réduits.</li></ul> | 
| WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE | Sélectionnez ce mode lorsque la résolution de sortie est inférieure ou égale à la moitié de la résolution d’entrée et que la <a href="wmformat-glossary.md"><em>fréquence d’images</em></a> de sortie est deux fois supérieure. Par exemple, utilisez ce mode lorsque la résolution vidéo d’entrée est de 640 x 480 pixels à 30 images entrelacées/s et que la résolution vidéo en sortie est de 320 x 240 pixels à 60 images/s. Avantageuse<br /><ul><li>Cela produit des images progressives de haute qualité, car chaque champ est converti en cadre et il n’est donc pas nécessaire de fusionner les informations.</li><li>Le mouvement complet des champs entrelacés est capturé.</li></ul> | 
| WM_DM_DEINTERLACE_INVERSETELECINE | Sélectionnez ce mode pour convertir la vidéo télécinéma 30 images/s en 24 images/s du film d’origine. Avantageuse<br /><ul><li>La qualité de compression s’améliore de manière significative, car seules 24 images/s au lieu de 30 images/s doivent être encodées.</li><li>Étant donné que le résultat est progressif, la même compression et l’affichage des avantages de l’entrelacement sont réalisés.</li></ul> | 
| WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE | Sélectionnez ce mode lorsque la résolution de sortie verticale est inférieure ou égale à la moitié de la résolution verticale d’entrée et que la <a href="wmformat-glossary.md"><em>fréquence d’images</em></a> de sortie est deux fois supérieure. Par exemple, la résolution vidéo verticale d’entrée est de 640 x 480 pixels à 30 images entrelacées/s et la résolution vidéo verticale de sortie est de 320 x 240 pixels à 60 images/s. Avantageuse<br /><ul><li>Cela produit des images progressives de haute qualité, car chaque champ est converti en cadre et il n’est donc pas nécessaire de fusionner les informations.</li><li>Le mouvement complet des champs entrelacés est capturé.</li></ul> | 




 

Pour le contenu mixte, définissez le mode de désentrelacement en fonction des besoins avant de passer des exemples d’un nouveau type. Par exemple, pour démarrer l’encodage avec une entrée progressive, vous n’avez pas besoin de définir de mode de désentrelacement. Si certains exemples requièrent alors une désentrelacement normal, vous devez définir le mode de désentrelacement sur WM \_ DM \_ subentrelacer \_ normal. Pour traiter ensuite d’autres exemples progressifs, vous devez définir le mode de désentrelacement sur WM \_ DM \_ NOTINTERLACED.

## <a name="inverse-telecine-settings"></a>Paramètres Inverse telecine

Pour obtenir une description de télécinéma inverse, consultez [pour utiliser l’inverse de télécinéma](to-use-inverse-telecine.md).

Si vous définissez le mode de désentrelacement sur WM \_ DM \_ désentrelacer \_ INVERSETELECINE, vous pouvez spécifier le modèle de télécinéma de la première trame d’entrée en appelant [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). Le paramètre à utiliser est g \_ wszInitialPatternForInverseTelecine. Définissez le modèle initial sur l’une des valeurs suivantes.



| Valeur                                              | Description                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WM \_ DM \_ \_ désactive le \_ mode de cohérence \_                | Spécifie que le média d’entrée est passé par le processus de télécinéma, mais que les images ne sont plus dans un modèle prévisible. Cela indique généralement que le support a été modifié après le traitement de télécinéma. Lorsque vous utilisez ce paramètre, le codec tente de reconstruire les frames d’origine de manière autonome. |
| WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ AA en \_ haut    | Spécifie que le champ supérieur du cadre AA est le premier échantillon.                                                                                                                                                                                                                                             |
| WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ BB \_ Top    | Spécifie que le champ supérieur du cadre BB est le premier échantillon.                                                                                                                                                                                                                                             |
| WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ BC \_ Top    | Spécifie que le champ supérieur de la trame BC est le premier échantillon.                                                                                                                                                                                                                                             |
| WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est le \_ CD \_ haut    | Spécifie que le champ supérieur du cadre CD est le premier exemple.                                                                                                                                                                                                                                             |
| WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ DD en \_ haut    | Spécifie que le champ supérieur du frame DD est le premier exemple.                                                                                                                                                                                                                                             |
| WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ AA en \_ bas | Spécifie que le champ inférieur du cadre AA est le premier échantillon.                                                                                                                                                                                                                                          |
| WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ BB en \_ bas | Spécifie que le champ inférieur du cadre BB est le premier échantillon.                                                                                                                                                                                                                                          |
| WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ BC \_ Bottom | Spécifie que le champ inférieur de la trame BC est le premier échantillon.                                                                                                                                                                                                                                          |
| WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est le \_ CD- \_ bas | Spécifie que le champ inférieur du cadre CD est le premier exemple.                                                                                                                                                                                                                                          |
| WM \_ DM \_ la \_ première \_ image \_ du \_ clip \_ est \_ DD en \_ bas | Spécifie que le champ inférieur du frame DD est le premier exemple.                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Rubriques avancées**](advanced-topics.md)
</dt> </dl>

 

 





