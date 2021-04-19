---
description: .
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: Interface utilisateur-mises à jour de la boîte de dialogue contrôle de compte d’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5711f8bbed029102bea81e0f4cfcbd4649b5a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535071"
---
# <a name="user-interface---user-account-control-dialog-updates"></a>Interface utilisateur-mises à jour de la boîte de dialogue contrôle de compte d’utilisateur

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**Serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -faible  
**Fréquence** -moyenne  











## <a name="description"></a>Description

Dans Windows 7, nous avons standardisé les options de la boîte de dialogue UAC. Auparavant, les utilisateurs devaient sélectionner plusieurs options, par exemple « continuer », « annuler », et ainsi de suite. Désormais, toutes les boîtes de dialogue donnent aux utilisateurs un simple « oui » ou « non ». La disposition de la boîte de dialogue affiche maintenant également clairement le nom du programme, l’éditeur et l’origine.

## <a name="leveraging-feature-capabilities"></a>Exploitation des fonctionnalités de fonctionnalités

Les exigences en matière de développement d’applications dans Windows 7 pour la compatibilité avec le contrôle de compte d’utilisateur sont les mêmes que dans Windows Vista. Les applications compatibles Windows Vista interagissent avec le contrôle de compte d’utilisateur dans Windows 7 sans aucune modification. Pour plus d’informations sur la façon de faire fonctionner correctement les applications Windows XP sur Windows 7, consultez les rubriques relatives au contrôle de compte d’utilisateur dans le Guide de *compatibilité des applications Windows Vista* . Alors que les améliorations du contrôle de compte d’utilisateur pour Windows 7 ont un impact sur l’expérience de l’utilisateur, elles n’ont pas d’impact sur l’interface de l’application. Toutefois, si un contenu d’aide est lié aux boîtes de dialogue UAC, vous devrez peut-être mettre à jour les captures d’écran.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Guide de compatibilité des applications Windows Vista](/previous-versions/bb757005(v=msdn.10))
-   [Téléchargement de l’outil Application Compatibility Toolkit](/windows-hardware/get-started/adk-install)
-   [Standard User Analyzer (Analyseur pour utilisateur standard)](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))

> [!Note]  
> Ces ressources peuvent ne pas être disponibles dans certaines langues et pays/régions.

 

 

 
