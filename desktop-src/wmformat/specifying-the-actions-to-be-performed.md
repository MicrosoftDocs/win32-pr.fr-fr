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
ms.openlocfilehash: b2d27df2904aee061deb252e08b59e1e88e4d1cd9e151290cd940fc48a650404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807799"
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

 

 




