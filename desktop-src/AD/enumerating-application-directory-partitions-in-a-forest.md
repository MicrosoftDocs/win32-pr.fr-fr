---
title: Énumération des partitions d’annuaire d’applications dans une forêt
description: À l’instar des partitions de domaine, chaque partition d’annuaire d’applications est représentée par un objet crossRef dans le conteneur partitions de la partition de configuration.
ms.assetid: dd1ff72d-ed19-4e8c-a401-a5b1b3d577e8
ms.tgt_platform: multiple
keywords:
- Énumération des partitions de l’annuaire d’applications dans une forêt Active Directory
- Partitions de l’annuaire d’applications Active Directory, énumération dans une forêt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d42bbe28ef37932394721d0c234ba3970ac263b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031011"
---
# <a name="enumerating-application-directory-partitions-in-a-forest"></a>Énumération des partitions d’annuaire d’applications dans une forêt

À l’instar des partitions de domaine, chaque partition d’annuaire d’applications est représentée par un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) dans le conteneur partitions de la partition de configuration. Chaque objet **crossRef** stocke des données sur sa partition correspondante.

Un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) qui représente une partition de domaine est distingué d’un objet **crossRef** qui représente une partition de l’annuaire d’applications par le contenu de l’attribut [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) . L’objet **crossRef** qui représente une partition de domaine aura à la fois les indicateurs de domaine [**ADS \_ systemFlags \_ CR \_ NTDS \_ NC**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) et **ADS \_ systemFlags \_ CR \_ NTDS \_** définis dans l’attribut **systemFlags** . L’objet **crossRef** qui représente une partition d’annuaire d’applications aura l’indicateur de contexte de nommage de domaine **ad \_ systemFlags \_ CR \_ NTDS \_** défini et l’indicateur de **\_ domaine ADS systemFlags \_ CR \_ NTDS \_** ne sera pas défini dans l’attribut **systemFlags** .

Les objets [**crossRef**](/windows/desktop/ADSchema/c-crossref) qui représentent les partitions de schéma et de configuration comporteront également l’indicateur [**\_ \_ NC systemFlags CR \_ NTDS NTDS \_ de ADS**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) et l’indicateur de **\_ domaine AD systemFlags \_ CR \_ NTDS \_** ne sera pas défini dans l’attribut [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) . Cela requiert que ces deux objets **crossRef** soient distingués par le contenu de l’attribut [**NCName**](/windows/desktop/ADSchema/a-ncname) . L’attribut **NCName** pour l’objet **crossRef** qui représente le conteneur de schéma sera identique à l’attribut **schemaNamingContext** de l’objet rootDSE. De même, l’attribut **NCName** pour l’objet **crossRef** qui représente le conteneur de configuration est identique à l’attribut **configurationNamingContext** de l’objet rootDSE.

**Pour identifier toutes les partitions d’annuaire d’applications dans une forêt, procédez comme suit :**

1.  Dans le conteneur partitions de la partition de configuration, recherchez ou Énumérez tous les objets [**crossRef**](/windows/desktop/ADSchema/c-crossref) .
2.  Si l’indicateur de domaine ADS [**\_ systemFlags \_ CR \_ NTDS \_**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) de l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) n’est pas défini ou que l’indicateur de **\_ \_ \_ \_ domaine ADS systemFlags CR** est défini dans la valeur de l’attribut [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , excluez l’objet du jeu de résultats.
3.  Excluez la partition de schéma du jeu de résultats en comparant l’attribut [**NCName**](/windows/desktop/ADSchema/a-ncname) de l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) à l’attribut **schemaNamingContext** de l’objet rootDSE.
4.  Excluez la partition de configuration du jeu de résultats en comparant l’attribut [**NCName**](/windows/desktop/ADSchema/a-ncname) de l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) à l’attribut **configurationNamingContext** de l’objet rootDSE.
5.  Les autres objets [**crossRef**](/windows/desktop/ADSchema/c-crossref) dans le jeu de résultats représentent tous des partitions d’annuaire d’applications.

 

 