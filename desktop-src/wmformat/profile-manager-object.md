---
title: Gestionnaire de profils, objet
description: Gestionnaire de profils, objet
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- Windows Media Format SDK, objets du gestionnaire de profils
- ASF (Advanced Systems Format), objets du gestionnaire de profils
- ASF (format des systèmes avancés), objets du gestionnaire de profils
- objets, objets du gestionnaire de profils
- profils, objets
- profils, objets du gestionnaire de profils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce3d77598f52e43a840c1b6b3ef58baa47f77bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525165"
---
# <a name="profile-manager-object"></a>Gestionnaire de profils, objet

Un profil est un ensemble de paramètres multimédias utilisés pour créer un fichier ASF. L’objet gestionnaire de profils crée des objets de profil pour la modification. Les objets de profil peuvent être créés sans aucune donnée ni être généré à partir de données de profil existantes. L’objet gestionnaire de profils fournit également des méthodes pour l’énumération des codecs pris en charge et l’interrogation de ces codecs pour obtenir des informations.

L’objet gestionnaire de profils est créé par la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) , qui définit un pointeur vers une interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . Les autres interfaces de l’objet gestionnaire de profils peuvent être obtenues en appelant la méthode **QueryInterface** .

Les interfaces suivantes sont prises en charge par l’objet gestionnaire de profils.



| Interface                                                      | Description                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | Récupère des informations sur les codecs pris en charge et leurs formats.                                                                              |
| [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | Récupère les noms des codecs pris en charge et les descriptions de leurs formats. Hérite de toutes les méthodes de **IWMCodecInfo**.          |
| [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | Récupère les codecs et les propriétés de codec pour les fonctionnalités prises en charge. Hérite de toutes les méthodes de **IWMCodecInfo** et **IWMCodecInfo2**. |
| [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | Crée de nouveaux profils, charge des profils existants et enregistre les profils personnalisés.                                                                    |
| [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | Contrôle la version des profils système énumérés par le gestionnaire de profils. Hérite de toutes les méthodes de **IWMProfileManager**.             |
| [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | Contrôle la langue des profils système analysés par le gestionnaire de profils.                                                                  |



 

## <a name="remarks"></a>Notes

Lorsqu’un objet gestionnaire de profils est créé, il analyse tous les profils système, ce qui peut prendre plusieurs secondes. La création et la libération d’un gestionnaire de profils chaque fois que vous devez l’utiliser, nuire aux performances. Vous devez créer un gestionnaire de profils une fois dans votre application et le libérer uniquement lorsque vous n’avez plus besoin de l’utiliser.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Profile (objet)**](profile-object.md)
</dt> <dt>

[**Profils**](profiles.md)
</dt> </dl>

 

 




