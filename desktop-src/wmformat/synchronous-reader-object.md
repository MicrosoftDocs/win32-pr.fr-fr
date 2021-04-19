---
title: Lecteur synchrone, objet
description: Lecteur synchrone, objet
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- Windows Media Format SDK, objets lecteur synchrones
- ASF (Advanced Systems Format), objets lecteur synchrones
- ASF (format des systèmes avancés), objets lecteur synchrones
- objets, lecteurs synchrones
- lecteurs synchrones, objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491fed915a049dbfc52acc24d06a0344d8e3109c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "106510671"
---
# <a name="synchronous-reader-object"></a>Lecteur synchrone, objet

L’objet lecteur synchrone est utilisé pour lire des fichiers multimédias numériques à l’aide d’appels synchrones.

L’objet lecteur synchrone est créé par la fonction [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), qui définit un pointeur vers une interface **IWMSyncReader** . Les autres interfaces prises en charge par l’interface de lecture synchrone peuvent être obtenues en appelant la méthode **QueryInterface** .

Les interfaces suivantes sont prises en charge par l’objet lecteur synchrone.



| Interface                                | Description                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | Définit et récupère les informations d’en-tête, telles que les métadonnées, les [*marqueurs*](wmformat-glossary.md), etc.                                            |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | Énumère les informations de codec disponibles. Hérite de toutes les méthodes de **IWMHeaderInfo**.                                                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | Prend en charge des tailles d’attribut volumineuses, des noms d’attributs dupliqués et la prise en charge de plusieurs langues. Hérite de toutes les méthodes de **IWMHeaderInfo** et **IWMHeaderInfo2**. |
| [**IWMProfile**](iwmprofile.md)         | Fournit l’accès aux informations de profil du fichier Windows Media chargé dans le lecteur.                                                                       |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | Récupère l’identificateur global unique (GUID), le cas échéant, associé au profil. Hérite de toutes les méthodes de **IWMProfile**.                               |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | Prend en charge le partage de bande passante et les informations de hiérarchisation des flux dans le profil. Hérite de toutes les méthodes de **IWMProfile** et **IWMProfile2**.                |
| [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | Fournit des fonctionnalités de lecture synchrones pour les fichiers multimédias numériques.                                                                                                 |
| [**IWMSyncReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | Prend en charge la recherche de codes temporels SMPTE et l’allocation manuelle des exemples. Hérite de toutes les méthodes de **IWMSyncReader**.                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Lecteur, objet**](reader-object.md)
</dt> <dt>

[**Lecture des fichiers avec le lecteur synchrone**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




