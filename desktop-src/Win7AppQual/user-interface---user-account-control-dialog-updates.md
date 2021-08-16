---
description: Interface utilisateur-mises à jour de la boîte de dialogue contrôle de compte d’utilisateur
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: Interface utilisateur-mises à jour de la boîte de dialogue contrôle de compte d’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7a7337c93410056b871a5893188fffc74ec759f8bebb0c1ef8392e17ba6409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328625"
---
# <a name="user-interface---user-account-control-dialog-updates"></a>Interface utilisateur-mises à jour de la boîte de dialogue contrôle de compte d’utilisateur

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -faible  
**Fréquence** -moyenne  











## <a name="description"></a>Description

dans Windows 7, nous avons standardisé les options de la boîte de dialogue UAC. Auparavant, les utilisateurs devaient sélectionner plusieurs options, par exemple « continuer », « annuler », et ainsi de suite. Désormais, toutes les boîtes de dialogue donnent aux utilisateurs un simple « oui » ou « non ». La disposition de la boîte de dialogue affiche maintenant également clairement le nom du programme, l’éditeur et l’origine.

## <a name="leveraging-feature-capabilities"></a>Exploitation des fonctionnalités de fonctionnalités

les exigences en matière de développement d’applications dans Windows 7 pour la compatibilité avec le contrôle de compte d’utilisateur sont les mêmes que dans Windows Vista. Windows les applications compatibles Vista interagissent avec le contrôle de compte d’utilisateur dans Windows 7 sans aucune modification. consultez les rubriques sur le contrôle de compte d’utilisateur dans le guide de *compatibilité des applications Windows Vista* pour plus d’informations sur la façon de faire fonctionner les applications Windows XP correctement sur Windows 7. tandis que les améliorations du contrôle de compte d’utilisateur pour Windows 7 auront un impact sur l’expérience de l’utilisateur, elles n’auront pas d’impact sur l’interface de l’application. Toutefois, si un contenu d’aide est lié aux boîtes de dialogue UAC, vous devrez peut-être mettre à jour les captures d’écran.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Windows Guide de compatibilité des applications Vista](/previous-versions/bb757005(v=msdn.10))
-   [compatibilité des applications Shared Computer Toolkit téléchargement](/windows-hardware/get-started/adk-install)
-   [Standard User Analyzer (Analyseur pour utilisateur standard)](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))

> [!Note]  
> Ces ressources peuvent ne pas être disponibles dans certaines langues et pays/régions.

 

 

 
