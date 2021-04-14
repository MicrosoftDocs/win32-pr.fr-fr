---
title: Spécification des actions à effectuer
description: Spécification des actions à effectuer
ms.assetid: b6b094b1-276d-4f90-adc7-0f3507fdfe27
keywords:
- ASF (Advanced Systems Format), spécification des actions
- ASF (format des systèmes avancés), spécification des actions
- gestion des droits numériques (DRM), spécification des actions
- DRM (gestion des droits numériques), spécification des actions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2bd39a04d9ac87c4492749ca5e250d587c0e25
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381539"
---
# <a name="specifying-the-actions-to-be-performed"></a>Spécification des actions à effectuer

Quand vous appelez [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) pour la première fois pour créer l’objet lecteur, le deuxième paramètre est **un opérateur de bits or de** valeurs de [**\_ droits WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) . Utilisez ce paramètre pour spécifier la ou les actions que l’application doit effectuer sur le premier fichier à ouvrir. Ces actions correspondent directement aux droits qui peuvent être spécifiés dans la licence. Lors des appels suivants à [**IWMReader :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), vous pouvez modifier les droits que vous demandez en appelant [**IWMDRMReader :: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty), en spécifiant la constante définie pour la propriété des [**\_ droits DRM**](drm-rights.md) et en utilisant des littéraux de chaîne (de type **WCHAR**) séparés par des points-virgules pour identifier les droits. L’extrait de code suivant demande quatre droits : lire le fichier, le copier sur un appareil et le lire dans le cadre d’une sélection collaborative.


```C++
WCHAR wszRights[] = L"Play;Copy;CollaborativePlay";
p_WMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
                              (BYTE*)wszRights, sizeof(wszRights));
```



> [!Note]  
> Ne confondez pas la propriété [**\_ droits DRM**](drm-rights.md) avec la propriété [**\_ indicateurs DRM**](drm-flags.md) , qui est un **DWORD** utilisé pour spécifier les droits à appliquer à une licence locale DRM version 1 lors de la copie du contenu à partir d’un CD.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecture des fichiers protégés**](reading-protected-files.md)
</dt> </dl>

 

 




