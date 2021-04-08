---
description: Découvrez comment utiliser l’outil d’analyse d’utilisateur standard (SUA) et l’Assistant SUA pour tester vos applications et détecter les problèmes de compatibilité potentiels.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Outil SUA (Standard User Analyzer) et Assistant SUA (Standard User Analyzer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc0e729c37ff1650f0dab7f3dd1c05ffb4b5f370
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104042906"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a>Outil SUA (Standard User Analyzer) et Assistant SUA (Standard User Analyzer)

## <a name="affected-platforms"></a>Plateformes affectées

**Clients :** Windows XP Windows \| Vista Windows \| 7  
**Serveurs :** Windows Server 2003 \| Windows server 2008 Windows server \| 2008 R2  

## <a name="description"></a>Description

Application Compatibility Toolkit comprend l’outil Analyseur utilisateur standard (SUA) et l’Assistant analyseur utilisateur standard (Assistant SUA). Ces outils vous permettent de tester vos applications et de surveiller les appels d’API afin de détecter les problèmes de compatibilité potentiels en raison de la fonctionnalité de contrôle de compte utilisateur (UAC) du système d’exploitation Windows 7.

Le contrôle de compte d’utilisateur, anciennement connu sous le nom de compte d’utilisateur limité, exige que tous les utilisateurs (y compris les membres du groupe administrateur) s’exécutent en tant qu’utilisateurs standard à l’aide de la boîte de dialogue d’invite de sécurité jusqu’à ce que l’application soit délibérément élevée. Toutefois, les applications qui requièrent l’accès et les privilèges pour les emplacements qui ne sont pas disponibles pour un utilisateur standard ne peuvent pas s’exécuter correctement avec le rôle d’utilisateur standard.

## <a name="usage"></a>Utilisation

Les sections suivantes fournissent des informations détaillées sur l’utilisation des outils de l’Assistant SUA et SUA.

**Outil SUA**

L’outil SUA vous permet d’analyser une application, de consulter un rapport détaillé sur les problèmes liés au contrôle de compte d’utilisateur, puis d’appliquer les solutions d’atténuation d’application suggérées et sélectionnées, comme indiqué dans l’organigramme suivant.

![Diagramme qui montre le déroulement du S U A Tool.](images/act-suaflowchart-appcookbook.gif)

*Outil et virtualisation SUA*

Seul l’outil SUA vous permet d’activer et de désactiver la fonctionnalité de virtualisation. En désactivant la fonctionnalité de virtualisation, l’application testée se comportera plus comme lorsqu’elle fonctionnera sur le système d’exploitation Windows XP.

*Outil SUA et privilèges élevés*

Seul l’outil SUA vous permet d’activer et de désactiver la fonctionnalité **lancer des élévations de privilèges** . La fonctionnalité lancer des élévations de privilèges permet à l’application sélectionnée de s’exécuter en tant qu’administrateur ou en tant qu’utilisateur standard. Selon votre sélection, vous trouverez différents types de problèmes liés au contrôle de compte d’utilisateur. Si vous désactivez la case à cocher lancer des privilèges **élevés** , votre application s’exécute avec des privilèges d’administrateur complets, ce qui permet à sua de prédire les problèmes susceptibles de se produire pour un utilisateur standard. Si vous activez la case à cocher lancer avec des privilèges élevés, vous verrez des erreurs qui résultent de l’exécution de l’application et de la génération d’erreurs.

**Assistant SUA**

L’Assistant SUA vous permet de suivre un processus étape par étape guidé qui vous permet d’analyser une application, puis d’appliquer les mesures d’atténuation d’application suggérées et sélectionnées, comme indiqué dans l’organigramme suivant. Contrairement à l’outil SUA, l’Assistant ne permet pas de passer en revue les problèmes détaillés relatifs au contrôle de compte d’utilisateur.

![Diagramme qui montre le déroulement du S U d’un Assistant.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Téléchargement de l’outil Application Compatibility Toolkit](/windows-hardware/get-started/adk-install)
-   [Fonctionnement des outils de l’analyseur d’utilisateurs standard](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))
-   [Informations techniques de référence sur l’analyseur utilisateur standard](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))
-   [Test et atténuation des problèmes à l’aide des outils de développement](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))
-   [Compatibilité des applications et contrôle de compte d’utilisateur](/previous-versions/windows/)

> [!Note]  
> Ces ressources peuvent ne pas être disponibles dans certaines langues et pays/régions.

 

 

 
