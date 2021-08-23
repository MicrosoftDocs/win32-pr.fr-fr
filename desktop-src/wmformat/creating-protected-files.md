---
title: Création de fichiers protégés
description: Création de fichiers protégés
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows Media Format SDK, création de fichiers protégés
- Windows Media Format SDK, fichiers protégés
- ASF (Advanced Systems Format), création de fichiers protégés
- ASF (format des systèmes avancés), création de fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), WMStubDRM. lib
- ASF (format avancé des systèmes), WMStubDRM. lib
- WMStubDRM. lib, création de fichiers protégés
- WMStubDRM. lib, fichiers protégés
- gestion des droits numériques (DRM), WMStubDRM. lib
- DRM (gestion des droits numériques), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5be729f04f67e1a2e4319bcc8d267c798942293c2df2ee97dcc6a559af612aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809469"
---
# <a name="creating-protected-files"></a>Création de fichiers protégés

Pour créer des fichiers multimédias numériques protégés à l’aide de DRM version 1 ou DRM 7 et versions ultérieures, créez un lien vers le fichier WMStubDRM. lib que vous avez obtenu auprès de Microsoft et créez l’objet enregistreur. Pour la protection de la version 1, utilisez l’interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) pour définir les attributs DRM que vous souhaitez appliquer. Pour les versions 7 et ultérieures, utilisez les méthodes de l’interface [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) .

Les rubriques suivantes décrivent en détail comment protéger des fichiers.

-   [Protection des fichiers avec DRM version 1](protecting-files-with-drm-version-1.md)
-   [Protection des fichiers avec DRM version 7 ou ultérieure](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Liste des attributs DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> <dt>

[**Versions DRM**](drm-versions.md)
</dt> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> <dt>

[**Obtention de la bibliothèque DRM requise**](obtaining-the-required-drm-library.md)
</dt> <dt>

[**Lecture des fichiers protégés**](reading-protected-files.md)
</dt> </dl>

 

 




