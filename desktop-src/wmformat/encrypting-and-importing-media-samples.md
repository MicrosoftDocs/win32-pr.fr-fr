---
title: Chiffrement et importation d’exemples de médias
description: Chiffrement et importation d’exemples de médias
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- Windows Media Format SDK, importation DRM
- Windows Media Format SDK, importer
- Windows Media Format SDK, chiffrement des exemples de supports
- gestion des droits numériques (DRM), importation
- DRM (gestion des droits numériques), importation
- gestion des droits numériques (DRM), chiffrement des exemples de supports
- DRM (gestion des droits numériques), chiffrement des exemples de supports
- API étendues du client DRM, importation
- API étendues du client, importation
- API étendues du client DRM, chiffrement des exemples de médias
- API étendues du client, chiffrement des exemples de médias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed604fc114feed6bd308b9a89c6bde6d6c96abeb9e88a7b9ace19d553de1596
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658839"
---
# <a name="encrypting-and-importing-media-samples"></a>Chiffrement et importation d’exemples de médias

pour chaque échantillon multimédia que vous chiffrez à l’aide de Windows media DRM, vous devez générer une valeur salt qui est strictement supérieure à la précédente (ce qui augmente de façon monotone). Utilisez la nouvelle valeur salt pour créer une clé de chiffrement transitoire en appliquant l’algorithme de chiffrement SHA-1 au vecteur d’initialisation concaténé avec la valeur salt.

Ensuite, chiffrez l’exemple en fonction de l’algorithme RC4 à l’aide de la clé transitoire générée. Avant que l’exemple ne soit passé au kit de développement logiciel (SDK), votre application doit associer la valeur Salt à l’exemple en définissant un attribut d’extension.

Voici les étapes de chiffrement des exemples de média :

1.  Appelez la méthode **QueryInterface** de l’exemple d’objet pour accéder à l’interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .
2.  Incrémentez la valeur salt.
3.  Chiffrez l’exemple à l’aide d’un algorithme de chiffrement RC1. Pour le chiffrement, vous créez une clé en concaténant le vecteur d’initialisation et la valeur salt.
4.  Fournissez la valeur Salt au kit de développement logiciel (SDK) en appelant [**INSSBuffer :: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Importation DRM**](drm-import.md)
</dt> <dt>

[**Exemple de chiffrement d’échantillon de média**](media-sample-encryption-example.md)
</dt> </dl>

 

 




