---
title: Exemples de types d’extension
description: Exemples de types d’extension
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows Media Format SDK, exemples d’extensions
- ASF (Advanced Systems Format), exemples d’extensions
- ASF (Advanced Systems Format), exemples d’extensions
- Windows Media Format SDK, Data Unit extensions
- ASF (Advanced Systems Format), extensions d’unité de données
- ASF (format de systèmes avancés), extensions d’unité de données
- Windows Media Format SDK, propriétés de mémoire tampon
- ASF (Advanced Systems Format), propriétés de mémoire tampon
- ASF (format de systèmes avancés), propriétés de mémoire tampon
- exemples d’extensions, types
- extensions d’unité de données, types
- Propriétés de la mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1404dfee60c3de179df2bee0f7f123112002108
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479775"
---
# <a name="sample-extension-types"></a>Exemples de types d’extension

Des exemples d’extensions, également appelées « extensions d’unité de données » (cotisations) ou des propriétés de mémoire tampon, sont des éléments de données attachés aux exemples de média dans la section données du fichier ASF. plusieurs types d’exemples d’extensions sont définis dans le kit de développement logiciel (SDK) Format multimédia Windows. Vous pouvez également créer vos propres types d’extensions.

Pour utiliser des exemples d’extensions, vous devez identifier le type d’extension dans les données de configuration de flux du profil. Appelez la méthode [**IWMStreamConfig2 :: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) pour configurer un flux afin d’accepter des exemples avec des données étendues.

Des exemples d’extensions individuelles doivent être ajoutés aux exemples d’entrée en appelant la méthode [**INSSBuffer3 :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) . Lors de la lecture des exemples, vous pouvez appeler la méthode [**INSSBuffer3 :: GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) pour récupérer les données d’extension. Vous pouvez également utiliser les méthodes de l’interface [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) pour énumérer les extensions d’unité de données jointes à un exemple.

Le tableau suivant répertorie les identificateurs d’extension d’unité de données prédéfinis, et décrit les données jointes aux exemples pour chacune d’elles.




| Exemple de GUID d’extension | Description | 
|-----------------------|-------------|
| WM_SampleExtensionGUID_OutputCleanPoint | Les données indiquent si l’échantillon est un <a href="wmformat-glossary.md"><em>Cleanpoint</em></a>. La valeur zéro indique que l’exemple n’est pas un Cleanpoint. Une valeur différente de zéro indique qu’il s’agit d’un Cleanpoint. Cet exemple de type d’extension d’unité de données (DUE) est utilisé pour effectuer le suivi des cleanpoints lors de l’écriture de flux de données multimédias précompressés qui ont été encodés avec des codecs tiers. | 
| WM_SampleExtensionGUID_Timecode | Les données sont une structure <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> contenant les données de code horaire SMPTE associées à l’exemple. La taille de cet échéance est toujours WM_SampleExtension_Timecode_Size, soit 14 octets.<br /> | 
| WM_SampleExtensionGUID_FileName | Ce type d’exemple d’extension est utilisé pour les flux de fichiers. Les données d’un exemple de flux de fichier sont une partie d’un fichier de données. Les données de l’exemple d’extension spécifient le nom du fichier à partir duquel le contenu de l’échantillon a été pris. Le nom de fichier est une chaîne de caractères larges contenant le nom de fichier au format name. extension sans aucune information de chemin d’accès.<br /> | 
| WM_SampleExtensionGUID_ContentType | Les données identifient le type de contenu que l’exemple contient. Ce type d’exemple d’extension est utilisé avec les flux vidéo entrelacés. Tout le contenu entrelacé utilise l’indicateur WM_CT_INTERLACED combiné par <strong>une opération or au niveau</strong> du bit avec WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST ou WM_CT_REPEAT_FIRST_FIELD.<br /> L’ordre des champs n’est pas utilisé dans le processus d’encodage, mais est conservé avec les exemples compressés pour pouvoir être transmis au matériel de rendu. La diffusion de contenu entrelacé avec un ordre de champ incorrect présente des artefacts tels que le bougé de mouvement dans la vidéo.<br /> La taille de cet échéance est toujours WM_SampleExtension_ContentType_Size.<br /> | 
| WM_SampleExtensionGUID_PixelAspectRatio | Les données indiquent les proportions de pixels du contenu de l’échantillon. Cela s’applique uniquement à la vidéo. Ce type d’extension est utilisé pour identifier les proportions des pixels non carrés. pour plus d’informations, consultez <a href="to-read-and-write-video-streams-with-non-square-pixels.md">pour lire et écrire des Flux vidéo avec des Pixels Non carrés</a>.<br /> Les valeurs de proportions sont stockées sous la forme d’un mot dont l’octet de poids faible est l’aspect X et dont l’octet de poids fort est l’aspect Y. Par exemple, 16:9 est stocké en tant que 0x0910.<br /> La taille de cet échéance est toujours WM_SampleExtension_PixelAspectRatio_Size, soit 2 octets.<br /> | 
| WM_SampleExtensionGUID_SampleDuration | Les données indiquent la durée, en millisecondes, de l’échantillon contenu dans l’objet buffer. Lors de la lecture, si cette raison est définie, l’objet lecteur l’utilise pour remplacer la valeur de durée d’exemple existante. Cette échéance est définie automatiquement par les composants d’exécution du kit de développement logiciel (SDK) sur les flux vidéo avec des vitesses de transmission de 100 Kbits/s ou plus, où la surcharge des informations en attente n’est pas significative. Elle n’est pas définie pour les flux avec des vitesses de transmission inférieures à 100 Kbits/s. Les applications ne doivent pas définir cette raison manuellement, car le rédacteur (sur des flux à débit élevé) remplacera la valeur par ses propres données.<br /> La taille de cet échéance est toujours WM_SampleExtension_SampleDuration_Size, soit 2 octets.<br /> | 
| WM_SampleExtensionGUID_ChromaLocation | Les données indiquent le type de sous-échantillonnage de chrominance utilisé dans le format vidéo I420. La valeur de cette extension est définie sur l’une des valeurs suivantes :<br /><ul><li>WM_CL_INTERLACED420</li><li>WM_CL_PROGRESSIVE420</li></ul>Cette extension d’unité de données n’est pas configurée dans le profil. Elle est incluse dans les exemples de sortie du décodeur.<br /> La taille de cet échéance est toujours WM_SampleExtension_ChromaLocation_Size, soit 1 octet.<br /> | 
| WM_SampleExtensionGUID_ColorSpaceInfo | Les données fournissent des informations sur l’espace colorimétrique utilisé pour la trame vidéo actuelle. La valeur de cette extension est une structure <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> .<br /> Cette extension d’unité de données n’est pas configurée dans le profil. Elle est incluse dans les exemples de sortie du décodeur.<br /> La taille de cet échéance est toujours WM_SampleExtension_ColorSpaceInfo_Size, soit 3 octets.<br /> | 
| WM_SampleExtensionGUID_UserDataInfo | Les données sont des données utilisateur personnalisées. Les quatre premiers octets des données contiennent la taille des données personnalisées.<br /> L’octet suivant contient le type de données utilisateur fourni dans l’exemple d’extension. Les types suivants sont pris en charge :<br /><ul><li>0x1F-données utilisateur au niveau de la séquence</li><li>0x1E-données utilisateur de niveau de point d’entrée</li><li>0x1D-données utilisateur au niveau de la trame</li><li>0x1C-données utilisateur au niveau du champ</li><li>0x1B-données utilisateur au niveau de la tranche</li></ul>Le sixième octets et les suivants contiennent les données utilisateur. Il y a autant d’octets de données utilisateur que ceux spécifiés par le nombre dans les quatre premiers octets.<br /> Cette extension d’unité de données n’est pas configurée dans le profil. Il est inclus dans les exemples qui sont générés par le décodeur.<br /> | 
| WM_SampleExtensionGUID_SampleProtectionSalt | Les données sont chiffrées par exemple. cet exemple de type d’extension est utilisé pour le contenu importé à partir d’un format de fichier non ASF et d’un schéma de protection des droits autre que Windows Media DRM. Lorsque vous importez du contenu protégé, chaque exemple doit inclure un Salt unique. En général, cette valeur est un compteur à croissance monotone.<br /> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 





