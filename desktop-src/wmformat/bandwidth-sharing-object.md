---
title: Objet de partage de bande passante
description: Objet de partage de bande passante
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- Windows Media Format SDK, objets de partage de bande passante
- ASF (Advanced Systems Format), objets de partage de bande passante
- ASF (format de systèmes avancés), objets de partage de bande passante
- objets, objets de partage de bande passante
- partage de bande passante, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29048e3094f1a12775dfbec7422baf349c18be7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381531"
---
# <a name="bandwidth-sharing-object"></a>Objet de partage de bande passante

Un objet de partage de bande passante est utilisé pour indiquer que deux flux ou plus, indépendamment de leurs vitesses de transmission individuelles, n’utiliseront jamais plus d’une quantité de bande passante spécifiée entre eux. Il s’agit d’un objet purement informatif. les vitesses de transmission définies dans cet ensemble ne sont pas appliquées par programmation par un objet de ce kit de développement logiciel (SDK).

Les informations de partage de bande passante sont une partie facultative d’un profil. Les objets de partage de bande passante peuvent être créés pour les informations de partage de bande passante existantes dans un profil ou peuvent être créés vides, prêts à recevoir de nouvelles données. Les objets de partage de bande passante ne peuvent pas exister indépendamment d’un objet de profil. Pour enregistrer le contenu d’un objet de partage de bande passante, vous devez appeler [**IWMProfile3 :: AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).

Pour créer un objet de partage de bande passante, appelez l’une des méthodes suivantes.



| Méthode                                                                                  | Description                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | Crée un objet de partage de bande passante sans aucune donnée.                                                                                                           |
| [**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | Crée un objet de partage de bande passante rempli avec les données d’un profil. Utilise l’index de partage de bande passante pour identifier les informations de partage de bande passante souhaitées. |



 

Les deux méthodes du tableau précédent définissent un pointeur vers une interface **IWMBandwidthSharing** . L’interface **IWMStreamList** est héritée par **IWMBandwidthSharing**. il n’est donc pas nécessaire d’appeler **QueryInterface** avec cet objet.

Les interfaces suivantes sont prises en charge par chaque objet de partage de bande passante.



| Interface                                          | Description                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | Gère les propriétés d’un groupe de flux qui partageront la bande passante. |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Gère la liste des flux qui partageront la bande passante.                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Partage de bande passante**](bandwidth-sharing.md)
</dt> <dt>

[**Gestionnaire de profils, objet**](profile-manager-object.md)
</dt> <dt>

[**Profile (objet)**](profile-object.md)
</dt> </dl>

 

 




