---
title: Listes d’autorisations et d’inclusion explicites
description: Listes d’autorisations et d’inclusion explicites
ms.assetid: b2e1cdd4-ea3c-4b05-a53a-2cdc12440645
keywords:
- Windows Media Format SDK, exportation DRM
- Windows Media Format SDK, exporter
- Windows Media Format SDK, liste d’autorisations et d’inclusion explicites
- Windows Media Format SDK, listes d’autorisations
- Windows Media Format SDK, listes d’inclusion
- gestion des droits numériques (DRM), exportation
- DRM (gestion des droits numériques), exportation
- gestion des droits numériques (DRM), listes d’autorisation et d’inclusion explicites
- DRM (gestion des droits numériques), listes d’autorisation et d’inclusion explicites
- gestion des droits numériques (DRM), listes d’autorisations
- DRM (gestion des droits numériques), listes d’autorisations
- gestion des droits numériques (DRM), listes d’inclusion
- DRM (gestion des droits numériques), listes d’inclusion
- API étendues du client DRM, listes d’autorisations et d’inclusion explicites
- API étendues clientes, listes d’autorisations et d’inclusion explicites
- API étendues du client DRM, listes d’autorisations
- API étendues clientes, listes d’autorisations
- API étendues du client DRM, listes d’inclusion
- API étendues clientes, listes d’inclusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2309bed28ffd3add2a75c1cd90488b9ef454659b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381489"
---
# <a name="explicit-authorization-and-inclusion-lists"></a>Listes d’autorisations et d’inclusion explicites

Les licences peuvent contenir une liste d’inclusion pour autoriser explicitement l’exportation de contenu protégé par Windows Media DRM vers d’autres schémas de protection de contenu (CPS). Conformément aux termes du contrat de licence que vous entrez avec Microsoft pour activer l’exportation DRM, vous pouvez exporter uniquement vers un CPS valide identifié dans la liste d’inclusion d’une licence.

Une liste d’inclusion est un tableau limité d’identificateurs globaux uniques (GUID) qui représente chacun un CPS autorisé spécifique sur lequel le contenu peut être exporté. Les GUID répertoriés dans une liste d’inclusion sont indépendants des niveaux de protection de sortie (OPL) et des niveaux de protection de contenu (CPL). L’application de ces restrictions est la responsabilité de votre application.

> [!Note]  
> Lorsque vous effectuez l’exportation DRM Windows Media sur du contenu compressé, vous accédez à la liste d’inclusion par le biais de la méthode [**IWMDRMLicense :: GetInclusionList**](iwmdrmlicense-getinclusionlist.md) . Lorsque vous effectuez l’exportation DRM Windows Media sur du contenu non compressé, utilisez la méthode [**IWMDRMReader3 :: GetInclusionList**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader3-getinclusionlist) .

 

Pour inscrire un nouveau système de protection de contenu comme une exportation autorisée Windows Media DRM dans les règles de conformité d’exportation DRM Windows Media, contactez wmla@microsoft.com .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exportation DRM**](drm-export.md)
</dt> </dl>

 

 




