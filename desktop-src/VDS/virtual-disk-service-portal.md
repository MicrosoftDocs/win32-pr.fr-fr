---
description: Le service de disque virtuel (VDS) gère un large éventail de configurations de stockage, des postes de travail à disque unique aux groupes de stockage externes. Le service expose une interface de programmation d’applications (API).
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Service Disque virtuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c84217b1ca63debe3e117e33b2358e4b0e55697c02ce8e00ce7f764c1fbf692
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137132"
---
# <a name="virtual-disk-service"></a>Service Disque virtuel

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du Service de disque virtuel est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

## <a name="purpose"></a>Objectif

Le service de disque virtuel (VDS) gère un large éventail de configurations de stockage, des postes de travail à disque unique aux groupes de stockage externes. Le service expose une interface de programmation d’applications (API).

## <a name="where-applicable"></a>Le cas échéant

à partir de Windows 8 et Windows Server 8, l’interface COM du Service de disque virtuel est remplacée par l’API de gestion des Stockage, une interface de programmation basée sur WMI. pour la gestion des sous-systèmes de stockage, (Windows) des disques, des partitions et des volumes, nous vous recommandons fortement d’utiliser l’API de gestion des Stockage. pour plus d’informations, consultez [Windows Stockage API de gestion](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).

Pour toutes les utilisations, à l’exception des volumes de démarrage miroir (à l’aide d’un volume miroir pour héberger le système d’exploitation), les disques dynamiques sont déconseillés. pour les données qui nécessitent une résilience contre les défaillances de disque, utilisez espaces de stockage, une solution de virtualisation de stockage résiliente. pour plus d’informations, consultez [espaces de stockage Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).

Les développeurs d’applications qui utilisent les interfaces décrites dans ce guide peuvent interroger et configurer un ensemble hétérogène de stockage géré en interne et fourni par le fournisseur. VDS masque les applications complexes associées au stockage, ce qui rend le service indépendant des fournisseurs et des technologies.

## <a name="developer-audience"></a>Développeurs concernés

cette documentation est destinée aux développeurs d’applications qui connaissent les capacités de stockage des plates-formes Microsoft Windows et qui connaissent le développement COM.

Ce guide est également destiné aux fabricants de matériel sous-système qui développent et prennent en charge les programmes fournisseurs de matériel VDS.

## <a name="run-time-requirements"></a>Conditions d’exécution

VDS est pris en charge sur Windows Server 2003, Windows Vista et versions ultérieures. Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la documentation relative à cet élément.

l’exécution d’applications vds 32 bits sous WOW64 est prise en charge, mais les fournisseurs vds 64 bits doivent s’exécuter en tant qu’applications natives sur les versions de Windows 64 bits.

VDS est disponible dans le kit de développement logiciel (SDK) de Microsoft Windows. vous pouvez installer le kit de développement logiciel (SDK) pour Windows 7 et Windows Server 2008 R2 à partir du [centre de téléchargement Windows](https://www.microsoft.com/download/details.aspx?id=8279). cette version de la SDK Windows peut être utilisée pour développer des applications VDS pour Windows Server 2003, Windows Vista et versions ultérieures. vous pouvez également télécharger la [version ISO](https://www.microsoft.com/download/details.aspx?id=8442) du kit de développement logiciel (SDK) à partir du centre de téléchargement Windows.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                         | Description                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [À propos de VDS](about-vds.md)<br/>         | Décrit le modèle d’objet VDS, les stratégies de configuration de stockage et les notifications VDS.<br/>    |
| [Utilisation de VDS](using-vds.md)<br/>         | Décrit comment utiliser VDS pour interroger et configurer des périphériques de stockage.<br/>                            |
| [Référence VDS](vds-reference.md)<br/> | Décrit les constantes, les types de données, les énumérations, les interfaces, les structures et les codes d’erreur VDS.<br/> |



 

 

