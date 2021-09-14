---
title: Obtention et définition des métadonnées et des attributs
description: Obtention et définition des métadonnées et des attributs
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Windows Gestionnaire de périphériques de média, attributs
- Gestionnaire de périphériques, attributs
- applications de bureau, attributs
- fournisseurs de services, attributs
- Guide de programmation, attributs
- attributs
- Windows Gestionnaire de périphériques de média, métadonnées
- Gestionnaire de périphériques, métadonnées
- applications de bureau, métadonnées
- fournisseurs de services, métadonnées
- Guide de programmation, métadonnées
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8697f62dac44f5aab4b08aa4f6c516ac35a17e4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856414"
---
# <a name="getting-and-setting-metadata-and-attributes"></a>Obtention et définition des métadonnées et des attributs

Une application peut obtenir deux types d’informations sur un stockage ou un appareil : les attributs et les métadonnées. Les attributs sont des valeurs booléennes plus simples qui décrivent généralement les informations du système de fichiers, par exemple si un stockage a des objets enfants, s’il peut être renommé, lu ou supprimé, et ainsi de suite. Les attributs sont récupérés en tant que valeurs d’indicateurs en appelant [**IWMDMStorage :: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) ou [**IWMDMStorage2 :: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2). Les attributs sont définis en appelant [**IWMDMStorage3 :: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).

Une application peut également demander des données plus complexes (numériques, de chaîne ou d’autres types de données) en tant que *métadonnées*. Les valeurs de métadonnées sont identifiées par des noms de chaîne uniques. Windows Le Gestionnaire de périphériques de média définit une liste de constantes de chaîne qui peuvent être utilisées pour demander des valeurs. ces valeurs définies sont répertoriées dans [constantes de métadonnées](metadata-constants.md). Un fournisseur de services peut définir ses propres constantes, mais une application appelante doit être consciente de ces définitions pour pouvoir demander ou définir ces valeurs de métadonnées personnalisées. L’application demande des métadonnées en appelant [**IWMDMStorage3 :: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) ou [**IWMDMStorage4 :: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).

L’un des aspects importants de l’obtention et de la définition des métadonnées et des attributs est de savoir où proviennent les valeurs récupérées. Le fournisseur de services ou l’appareil peut récupérer ces valeurs à partir de différents emplacements, y compris les éléments suivants :

-   À partir de l’en-tête de fichier. Par exemple, dans un fichier ASF, la vitesse de transmission est stockée dans l’en-tête de fichier.
-   À partir de valeurs définies explicitement par l’application lors de l’appel d’une méthode. Ces valeurs peuvent être enregistrées dans un magasin de métadonnées externe dans le fournisseur de services ou l’appareil. Ce magasin peut ou non persister quand l’appareil se déconnecte ou s’éteint. Par exemple, les évaluations nombre de lecture et étoile de l’utilisateur sont généralement stockées dans des magasins externes sur l’ordinateur ou l’appareil.
-   En examinant les informations fournies par le système de fichiers. Par exemple, si un fichier est en lecture seule ou si un dossier a des enfants.
-   En ouvrant et en analysant les données de fichier.

Il est important de se rendre compte qu’une propriété peut être stockée dans plusieurs emplacements (dans l’en-tête de fichier et également dans un magasin local), et qu’elle peut être modifiable ou non. Par exemple, la modification d’une description de fichier peut ou non être persistante ; Si le fournisseur de services stocke la description localement, elle ne sera pas conservée sur l’appareil. De même, si la description de fichier est extraite de l’en-tête de fichier, sa modification est persistante uniquement si le fournisseur de services ou l’appareil ouvre et modifie les données d’en-tête. La plupart des applications font une meilleure tentative en modifiant les valeurs souhaitées, mais ne dépendent pas des propriétés qui doivent être modifiées de manière permanente.

Pour plus d’informations sur l’obtention et la définition des valeurs, reportez-vous aux sections appropriées pour les développeurs d’applications et les développeurs de fournisseurs de services, plus loin dans la documentation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Tâches communes aux applications et aux fournisseurs de services**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




