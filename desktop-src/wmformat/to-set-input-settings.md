---
title: pour définir les Paramètres d’entrée
description: pour définir les Paramètres d’entrée
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- ASF (Advanced Systems Format), paramètres d’entrée
- ASF (format des systèmes avancés), paramètres d’entrée
- profils, paramètres d’entrée
- codecs, paramètres d’entrée
- flux, paramètres d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df5b10ea6bd15ad083b26a61af037527f00576eaa6b7e1fa795ea1591417ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447019"
---
# <a name="to-set-input-settings"></a>pour définir les Paramètres d’entrée

Les propriétés de base des médias d’entrée et de flux de données sont définies par la structure du [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Pour les formats d’entrée, les informations sur le type de média sont définies par votre application. Pour les formats de flux, les informations sur le type de média sont définies dans le profil que vous attribuez au writer. Certaines propriétés sont indépendantes du type de média et doivent être définies pour une entrée avant le début de l’écriture. Ces propriétés sont des fonctionnalités de codec et d’écriture indépendantes du type de flux. elles doivent être définies une fois que le profil a été affecté dans le writer, mais avant le début de l’écriture.

La définition d’un paramètre d’entrée requiert un appel à [**IWMWriterAdvanced2 :: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). Vous pouvez également vérifier la valeur actuelle d’un paramètre à l’aide d’un appel à [**IWMWriterAdvanced2 :: GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Pour utiliser des profils avec l’auteur**](to-use-profiles-with-the-writer.md)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> <dt>

[**Écriture d’une image Flux**](writing-image-streams.md)
</dt> </dl>

 

 




