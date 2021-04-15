---
description: CPersistStream est la classe de base pour les propriétés persistantes des filtres (c’est-à-dire les propriétés de filtre dans les graphiques enregistrés).
ms.assetid: 8073e2be-aaf9-4b01-a7d5-bab5c1dcc19b
title: CPersistStream, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream
api_type:
- COM
api_location: ''
ms.openlocfilehash: 690a0f45fab7c3612d215a859798460abc81728e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520783"
---
# <a name="cpersiststream-class"></a>CPersistStream, classe

![hiérarchie de la classe cpersiststream](images/pstrm01.png)

`CPersistStream` est la classe de base pour les propriétés persistantes des filtres (c’est-à-dire les propriétés de filtre dans les graphiques enregistrés).

La façon la plus simple d’utiliser `CPersistStream` consiste à :

1.  Organisez votre filtre pour qu’il hérite de cette classe.
2.  Implémentez [**WriteToStream**](cpersiststream-writetostream.md) et [**readFromStream**](cpersiststream-readfromstream.md) dans votre classe. Celles-ci remplacent les fonctions ici, qui ne font rien, mais agissent comme des espaces réservés.
3.  Modifiez votre **NonDelegatingQueryInterface** pour gérer **IPersistStream**.
4.  Implémentez [**SizeMax**](cpersiststream-sizemax.md) pour retourner une limite supérieure au nombre d’octets de données que vous enregistrez.

    Si vous enregistrez des données Unicode™, n’oubliez pas qu’un WCHAR est de 2 octets.

5.  Lorsque vos données changent, appelez [**SetDirty**](cpersiststream-setdirty.md).

## <a name="version-numbers"></a>Numéros de versions

À un moment donné, vous pouvez décider de modifier ou d’étendre le format de vos données. Vous souhaiterez alors avoir un numéro de version dans tous les anciens flux enregistrés, ce qui vous permettra de savoir, quand vous les lisez, s’ils représentent l’ancien ou le nouveau formulaire. Pour vous aider, cette classe écrit et lit un numéro de version. Lorsqu’il écrit, il appelle [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) pour se renseigner sur la version du logiciel actuellement utilisée. (En fait, il s’agit d’un numéro de version de la disposition des données dans le fichier.) Il écrit ceci comme première chose dans les données. Si vous souhaitez modifier la version, implémentez (override) **GetSoftwareVersion**. Il lit le numéro de version du fichier dans **MPS \_ dwFileVersion** avant d’appeler [**readFromStream**](cpersiststream-readfromstream.md). ainsi, dans **readFromStream** , vous pouvez vérifier les **\_ dwFileVersion MPS** pour voir si vous lisez un ancien fichier de version. En général, vous devez accepter les fichiers dont la version n’est pas plus récente que la version du logiciel qui les lit.

**CPersistStream** implémente [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream). Pour plus d’informations sur l’implémentation, consultez la référence COM dans le kit de développement logiciel (SDK) Microsoft Platform.



| Membres de données protégés                                          | Description                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| \_DwFileVersion mPS                                              | Numéro de version du fichier.                                                   |
| \_FDirty mPS                                                     | Les données de ce flux doivent être enregistrées.                                           |
| Fonctions de membre                                                | Description                                                                   |
| [**CPersistStream**](cpersiststream-cpersiststream.md)         | Construit un objet **CPersistStream** .                                       |
| [**SetDirty**](cpersiststream-setdirty.md)                     | Indique que l’objet doit être enregistré dans le flux.                        |
| Fonctions membres substituables                                    | Description                                                                   |
| [**GetClassID**](cpersiststream-getclassid.md)                 | Récupère l’identificateur de classe de ce flux.                                |
| [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) | Récupère le numéro de version pour ce format de fichier.                            |
| [**ReadFromStream**](cpersiststream-readfromstream.md)         | Lit les données du filtre à partir du flux.                                      |
| [**SizeMax**](cpersiststream-sizemax.md)                       | Récupère le nombre d’octets nécessaires pour les données (à l’exclusion du numéro de version). |
| [**WriteToStream**](cpersiststream-writetostream.md)           | Écrit les données du filtre dans le flux.                                       |
| IPersistStream, méthodes                                          | Description                                                                   |
| [**GetSizeMax**](cpersiststream-getsizemax.md)                 | Récupère le nombre d’octets nécessaires pour les données (y compris le numéro de version).     |
| [**IsDirty**](cpersiststream-isdirty.md)                       | Vérifie si l’objet doit être enregistré.                                           |
| [**Load**](cpersiststream-load.md)                             | Charge les données du flux en mémoire.                                   |
| [**Enregistrer**](cpersiststream-save.md)                             | Enregistre les données de la mémoire dans le flux.                                     |



 

 

 
