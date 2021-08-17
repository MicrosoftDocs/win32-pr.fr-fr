---
description: Définition des droits d’administration pour une partition
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Définition des droits d’administration pour une partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33431c5beff76e015d28b6a7e886823620126f2ed9b84db68af9a8f3b8ac1d28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915822"
---
# <a name="setting-administrative-rights-for-a-partition"></a>Définition des droits d’administration pour une partition

Les utilisateurs disposant du rôle administrateur de l’application système COM+ sont autorisés à créer, modifier et supprimer des partitions COM+. Dans l’outil d’administration Services de composants, les rôles administratifs peuvent être attribués aux utilisateurs en développant le dossier **rôles** de l’application système com+.

à partir de Windows Server 2003, la fonctionnalité d’authentification de l’Application système COM+ comprend la valeur EOAC \_ DISABLE \_ AAA. Cette valeur, qui désactive les activations AAA (Activate-As-Activator), est utilisée dans l’appel de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) lors du lancement de l’application système. La définition de la fonctionnalité d’authentification sur EOAC \_ Disable \_ AAA permet à une application qui s’exécute sous un compte privilégié (tel que LocalSystem) d’empêcher son identité d’être utilisée pour lancer des composants non fiables.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Collecte des métriques de partition](collecting-partition-metrics.md)
</dt> <dt>

[Configuration du cache de partition](configuring-the-partition-cache.md)
</dt> <dt>

[Regroupement d’applications en partitions](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestion des partitions locales](managing-local-partitions.md)
</dt> <dt>

[Gestion des partitions dans Active Directory](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
