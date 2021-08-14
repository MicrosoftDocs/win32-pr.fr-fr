---
title: Hiérarchisation des flux
description: Hiérarchisation des flux
ms.assetid: 6b3e9b03-62ef-422b-97ab-197d1cd15beb
keywords:
- Windows Media Format SDK, hiérarchisation des flux
- ASF (Advanced Systems Format), hiérarchisation des flux
- ASF (format des systèmes avancés), hiérarchisation des flux
- Windows Media Format SDK, ordre de priorité pour les flux
- ASF (Advanced Systems Format), ordre de priorité pour les flux
- ASF (format des systèmes avancés), ordre de priorité pour les flux
- flux, hiérarchisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd34bab6a7957d7cbcdf97a78fc3d8be1f663d43ef1eb1ec8d4c575571ad0a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197275"
---
# <a name="stream-prioritization"></a>Hiérarchisation des flux

Lorsque vous créez un fichier ASF, vous pouvez spécifier un ordre de priorité pour ses flux constitutifs. Si vous diffusez un fichier classé par ordre de priorité et que la bande passante disponible n’est pas suffisante pour remettre tous les flux, le lecteur supprimera les flux dans l’ordre de priorité inverse. De cette façon, vous pouvez vous assurer que les flux les plus importants dans votre fichier ne seront pas supprimés en raison de problèmes réseau.

La hiérarchisation des flux est configurée avec un objet de priorité de flux et ajoutée au profil. Un profil ne peut contenir qu’un seul objet de définition de priorités de flux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization)
</dt> <dt>

[**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)
</dt> <dt>

[**IWMProfile3::RemoveStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization)
</dt> <dt>

[**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization)
</dt> <dt>

[**Interface IWMStreamPrioritization**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization)
</dt> <dt>

[**Utilisation de la hiérarchisation des flux**](using-stream-prioritization.md)
</dt> </dl>

 

 




