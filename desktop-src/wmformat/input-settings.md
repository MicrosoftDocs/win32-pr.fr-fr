---
title: Paramètres d’entrée
description: Paramètres d’entrée
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- Windows Media Format SDK, constantes globales
- ASF (Advanced Systems Format), constantes globales
- ASF (format de systèmes avancés), constantes globales
- constantes globales, liste des
- Windows Media Format SDK, constantes
- ASF (Advanced Systems Format), constantes
- ASF (Advanced Systems Format), constantes
- constantes, liste
- Windows Media Format SDK, paramètres d’entrée
- ASF (Advanced Systems Format), paramètres d’entrée
- ASF (format des systèmes avancés), paramètres d’entrée
- paramètres d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030771"
---
# <a name="input-settings"></a>Paramètres d’entrée

Les constantes globales suivantes sont utilisées pour identifier les paramètres d’entrée pour le writer.



| Constante globale                        | \_type de \_ données attr WMT                                                                                                                       | Description de *pValue*                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_wszDeinterlaceMode g                  | **WMT \_ TAPEZ \_ DWORD** avec l’une des valeurs de la table mode dans la rubrique [pour désentrelacer la vidéo](to-deinterlace-video.md).            | Lorsque cette valeur est définie, spécifie le type de contenu entrelacé de l’entrée. Pour plus d’informations, consultez [pour libérer de la vidéo](to-deinterlace-video.md).                                                                                                                            |
| \_wszFixedFrameRate g                   | **\_type WMT \_ bool**                                                                                                                       | Lorsque la valeur est définie sur true, le codec ne supprime pas les frames pendant l’encodage. La [*fréquence d’images*](wmformat-glossary.md) du flux vidéo de sortie est alors constante. La fréquence d’images du flux d’entrée n’a pas besoin d’être constante. |
| \_wszInitialPatternForInverseTelecine g | **WMT \_ TAPEZ \_ DWORD** défini sur l’une des valeurs de la table de modèles initiale dans la rubrique [pour désentrelacer la vidéo](to-deinterlace-video.md). | Lorsque le mode de désentrelacement est défini sur WM \_ DM \_ désentrelacer \_ INVERSETELECINE, vous pouvez définir cette valeur pour spécifier le modèle de l’entrée [*Telecine*](wmformat-glossary.md) . Pour plus d’informations, consultez [pour libérer de la vidéo](to-deinterlace-video.md).        |
| \_wszInterlacedCoding g                 | **\_type WMT \_ bool**                                                                                                                       | Quand la valeur est true, spécifie que le codec doit encoder le flux en tant que contenu entrelacé. Pour plus d’informations, consultez [pour utiliser une vidéo entrelacée](to-use-interlaced-video.md).                                                                                       |
| \_wszJPEGCompressionQuality g           | **\_valeur DWORD de type WMT \_**                                                                                                                      | Spécifie le niveau de qualité JPEG (compris entre 1 et 100) à utiliser sur l’entrée.                                                                                                                                                                                               |
| \_wszWatermarkCLSID g                   | **\_GUID du type WMT \_**                                                                                                                       | La valeur est définie sur le GUID de filigrane.                                                                                                                                                                                                                                 |
| \_wszWatermarkConfig g                  | **\_chaîne de type WMT \_**                                                                                                                     | La valeur est définie sur la configuration du filigrane. Cette valeur varie en fonction du filigrane DMO. Pour plus d’informations, consultez la documentation du système de filigrane.                                                                                   |



 

> [!Note]  
> Les paramètres d’entrée configurés pour un flux ne sont pas conservés dans le fichier écrit. Si vous souhaitez que votre lecteur personnalisé ait accès à ces paramètres d’encodage, vous devez créer des attributs personnalisés pour les stocker dans l’en-tête de fichier.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




