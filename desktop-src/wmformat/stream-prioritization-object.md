---
title: Objet de priorité de flux
description: Objet de priorité de flux
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- Windows Media Format SDK, objets de priorité de flux
- ASF (Advanced Systems Format), objets de définition de priorités de flux
- ASF (format des systèmes avancés), objets de priorité de flux
- objets, objets de priorité de flux
- objets de priorité de flux
- flux, objets de priorité de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce4189f64e85cca4e0d649dbc00409cf9d7c06
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511274"
---
# <a name="stream-prioritization-object"></a>Objet de priorité de flux

Un objet de priorité de flux est utilisé pour spécifier un ordre d’importance pour les flux dans un profil. Lorsque la lecture complète n’est pas possible en raison de limitations de la vitesse de transmission, les flux de priorité les plus faibles sont les premiers à être supprimés.

Vous pouvez créer des objets de définition de priorités de flux pour les données de priorité de flux existantes dans un profil ou vous pouvez les créer vides, prêts à recevoir de nouvelles données. Les objets de définition de priorités de flux ne peuvent pas exister indépendamment d’un objet de profil. Pour enregistrer le contenu d’un objet de priorité de flux, vous devez appeler [**IWMProfile3 :: SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization). Pour créer un objet de définition de priorités de flux, utilisez l’une des méthodes suivantes.



| Méthode                                                                                          | Description                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | Crée un objet de priorité de flux sans aucune donnée.                     |
| [**IWMProfile3::GetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | Crée un objet de priorité de flux rempli avec les données du profil. |



 

Les deux méthodes du tableau précédent définissent un pointeur vers une interface **IWMStreamPrioritization** . Il s’agit de la seule interface prise en charge par l’objet de définition de priorités des flux.



| Interface                                                  | Description                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWMStreamPrioritization**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | Gère la liste des flux au sein de l’objet de définition de priorités des flux. |



 

## <a name="remarks"></a>Notes

Une seule priorité de flux de données peut exister pour un profil donné. Si vous créez une nouvelle définition de priorités de flux pour un profil qui contient déjà une priorité de flux, l’ancienne est supprimée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Profile (objet)**](profile-object.md)
</dt> <dt>

[**Utilisation de la hiérarchisation des flux**](using-stream-prioritization.md)
</dt> </dl>

 

 




