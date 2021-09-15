---
title: Objet d’exclusion mutuelle
description: Objet d’exclusion mutuelle
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- Windows Kit de développement logiciel (SDK) Media format, objets d’exclusion mutuelle
- ASF (Advanced Systems Format), objets d’exclusion mutuelle
- ASF (format des systèmes avancés), objets d’exclusion mutuelle
- objets, objets d’exclusion mutuelle
- exclusion mutuelle, objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8522b66f82bd88479b8c7b1d0d0b45bd038fdab3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294427"
---
# <a name="mutual-exclusion-object"></a>Objet d’exclusion mutuelle

Un objet d’exclusion mutuelle est utilisé pour spécifier un certain nombre de flux, dont un seul peut être remis à la fois. Cela peut être utilisé de plusieurs façons, par exemple en fournissant un flux audio dans plusieurs langues en tant que piste audio pour un flux vidéo.

L’exclusion mutuelle est une partie facultative d’un profil. Des objets d’exclusion mutuelle peuvent être créés pour des informations d’exclusion mutuelle existantes dans un profil ou peuvent être créés vides, prêts à recevoir de nouvelles données. Les objets d’exclusion mutuelle ne peuvent pas exister indépendamment d’un objet de profil. Pour enregistrer le contenu d’un objet d’exclusion mutuelle, vous devez appeler [**IWMProfile :: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).

Pour créer un objet d’exclusion mutuelle, utilisez l’une des méthodes suivantes.



| Méthode                                                                              | Description                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Crée un objet d’exclusion mutuelle sans aucune donnée.                                                                                                         |
| [**IWMProfile::GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Crée un objet d’exclusion mutuelle rempli avec les données d’un profil. Utilise l’index d’exclusion mutuelle pour identifier les informations d’exclusion mutuelle souhaitées. |



 

Les deux méthodes du tableau précédent définissent un pointeur vers une interface **IWMMutualExclusion** . L’interface **IWMStreamList** est héritée par **IWMMutualExclusion** et n’a jamais besoin d’être accessible directement. L’autre interface de l’objet d’exclusion mutuelle peut être obtenue en appelant la méthode **QueryInterface** .

Les interfaces suivantes sont prises en charge par chaque objet d’exclusion mutuelle.



| Interface                                          | Description                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | Définit et récupère le type d’exclusion mutuelle à utiliser.                                                                                            |
| [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | Organise les flux en enregistrements, qui peuvent être utilisés pour créer des scénarios d’exclusion mutuelle complexes. Hérite de toutes les méthodes de **IWMMutualExclusion**. |
| [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | Gère la liste des flux qui s’excluent mutuellement.                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exclusion mutuelle**](mutual-exclusion.md)
</dt> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Gestionnaire de profils, objet**](profile-manager-object.md)
</dt> </dl>

 

 




