---
description: Définition des droits d’administration pour une partition
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Définition des droits d’administration pour une partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748277"
---
# <a name="setting-administrative-rights-for-a-partition"></a>Définition des droits d’administration pour une partition

Les utilisateurs disposant du rôle administrateur de l’application système COM+ sont autorisés à créer, modifier et supprimer des partitions COM+. Dans l’outil d’administration Services de composants, les rôles administratifs peuvent être attribués aux utilisateurs en développant le dossier **rôles** de l’application système com+.

À compter de Windows Server 2003, la fonctionnalité d’authentification de l’application système COM+ comprend la valeur EOAC \_ Disable \_ AAA. Cette valeur, qui désactive les activations AAA (Activate-As-Activator), est utilisée dans l’appel de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) lors du lancement de l’application système. La définition de la fonctionnalité d’authentification sur EOAC \_ Disable \_ AAA permet à une application qui s’exécute sous un compte privilégié (tel que LocalSystem) d’empêcher son identité d’être utilisée pour lancer des composants non fiables.

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

 

 
