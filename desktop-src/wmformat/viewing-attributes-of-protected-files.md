---
title: Affichage des attributs des fichiers protégés
description: Affichage des attributs des fichiers protégés
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- Windows Media Format SDK, affichage des attributs des fichiers protégés
- Windows Media Format SDK, attributs des fichiers protégés
- Windows Media Format SDK, fichiers protégés
- ASF (Advanced Systems Format), affichage des attributs des fichiers protégés
- ASF (format des systèmes avancés), affichage des attributs des fichiers protégés
- ASF (Advanced Systems Format), attributs des fichiers protégés
- ASF (format des systèmes avancés), attributs des fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- ASF (Advanced Systems Format), fichiers protégés
- gestion des droits numériques (DRM), affichage des attributs des fichiers protégés
- DRM (Digital Rights Management), affichage des attributs des fichiers protégés
- gestion des droits numériques (DRM), attributs des fichiers protégés
- DRM (gestion des droits numériques), attributs des fichiers protégés
- gestion des droits numériques (DRM), fichiers protégés
- DRM (gestion des droits numériques), fichiers protégés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723395"
---
# <a name="viewing-attributes-of-protected-files"></a>Affichage des attributs des fichiers protégés

Dans certains scénarios, vous devrez peut-être récupérer certains attributs DRM dans un fichier sans avoir à accéder au contenu du fichier. Cette fonctionnalité est utile, par exemple, dans les applications qui traitent des lots de fichiers de différentes manières en fonction des informations contenues dans l’en-tête de fichier. Dans les versions précédentes du kit de développement logiciel (SDK) du format Windows Media, les applications devaient être liées à la bibliothèque statique DRM afin d’ouvrir n’importe quel fichier protégé. Les applications qui ne disposent pas de la bibliothèque DRM peuvent utiliser l’interface [**IWMDRMEditor :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) sur l’objet de l’éditeur de métadonnées pour examiner certains attributs DRM.

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Liste des attributs DRM**](drm-attribute-list.md)
</dt> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interface IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




