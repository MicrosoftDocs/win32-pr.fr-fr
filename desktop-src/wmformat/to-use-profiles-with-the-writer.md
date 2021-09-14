---
title: Pour utiliser des profils avec l’auteur
description: Pour utiliser des profils avec l’auteur
ms.assetid: 8805bc57-5f19-4544-bcb8-5af880ba8ea0
keywords:
- Windows Media Format SDK, écriture de fichiers ASF
- Windows Media Format SDK, création de fichiers ASF
- Windows Media Format SDK, ASF (Advanced Systems Format)
- ASF (Advanced Systems Format), écriture de fichiers
- ASF (format de systèmes avancés), écriture de fichiers
- ASF (Advanced Systems Format), création de fichiers
- ASF (format des systèmes avancés), création de fichiers
- profils, création de fichiers ASF
- profils, écriture de fichiers ASF
- profils, création de fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d027e6ea0e669d2a5206901faefab1f5a9583153
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225828"
---
# <a name="to-use-profiles-with-the-writer"></a>Pour utiliser des profils avec l’auteur

Le writer utilise les données de profil pour créer des fichiers ASF. Vous devez spécifier un profil à utiliser avant d’effectuer toute autre opération avec le writer.

Vous pouvez définir un profil système à utiliser avec le writer en passant l’ID de profil à la méthode [**IWMWriter :: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid) .

Pour spécifier un profil personnalisé à utiliser avec le writer, vous devez obtenir une interface [**IWMProfile**](iwmprofile.md) pour un objet contenant les données de profil souhaitées. Pour ce faire, vous pouvez utiliser l’une des méthodes de chargement de l’interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . Une fois que vous disposez d’une interface **IWMProfile** valide, vous pouvez lui passer un pointeur vers la méthode [**IWMWriter :: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) . Pour plus d’informations sur les paramètres de profil, consultez [utilisation des profils](working-with-profiles.md).

Si vous apportez des modifications à l’objet de profil à l’aide de l’interface **IWMProfile** après avoir défini le profil dans le writer, vous devez rappeler **SetProfile** , sinon les modifications ne seront pas reflétées dans le writer. Toutefois, l’appel de **SetProfile** réinitialisera tous les attributs d’en-tête. par conséquent, veillez à définir les attributs d’en-tête requis après avoir appelé cette méthode.

l’exemple de fonction suivant définit le profil sur « Windows Media Video 8 pour les modems d’accès à distance (56 kbits/s) » :


```C++
#include <wmsysprf.h>

HRESULT SetProfileExample()
{
  HRESULT hr;
  IWMWriter *pWriter = NULL;
  hr = WMCreateWriter(NULL, &pWriter);
  if (FAILED(hr)) return hr;
  hr = pWriter->SetProfileByID(WMProfile_V80_56Video);
  return hr;
}

```



> [!Note]  
> il n’existe pas de profils système prédéfinis qui utilisent les codecs de série Windows Media Audio et Video 9. Pour plus d’informations, consultez [réutilisation des configurations de flux](reusing-stream-configurations.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)
</dt> <dt>

[**Utilisation des profils**](working-with-profiles.md)
</dt> <dt>

[**Écriture de fichiers ASF**](writing-asf-files.md)
</dt> </dl>

 

 




