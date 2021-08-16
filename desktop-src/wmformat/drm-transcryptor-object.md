---
title: Objet de transcrypteur DRM
description: Objet de transcrypteur DRM
ms.assetid: 50c041b3-6621-4618-843f-6ef9b8e741ab
keywords:
- Windows Kit de développement logiciel (SDK) Media format, objets de transcrypteur DRM
- ASF (Advanced Systems Format), objets de transchiffrement DRM
- ASF (format des systèmes avancés), objets de transchiffrement DRM
- objets, objets de transcrypteur DRM
- Objets de transcrypteur DRM
- Windows Media Format SDK, transcryptor Objects
- ASF (Advanced Systems Format), objets de transcrypteur
- ASF (format des systèmes avancés), objets de transchiffreur
- objets, transchiffrer des objets
- objets de transchiffreur
- gestion des droits numériques (DRM), objets de transchiffreur
- DRM (gestion des droits numériques), objets de transchiffreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5a6503a4ae95f44cac512966b0fe1612828d4d44d1db34d7724b1f764ba4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119085891"
---
# <a name="drm-transcryptor-object"></a>Objet de transcrypteur DRM

l’objet de conversion drm convertit les fichiers ASF protégés par drm en flux de données prêts à être envoyés aux périphériques réseau qui utilisent Windows Media drm 10 pour les périphériques réseau.

L’objet de transcrypteur DRM est créé par la fonction [**WMCreateDRMTranscryptor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor) , qui définit un pointeur vers l’interface [**IWMDRMTranscryptor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor) . **IUnknown** et **IWMDRMTranscryptor** sont les seules interfaces prises en charge par cet objet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> </dl>

 

 




