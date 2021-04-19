---
title: Haute résolution pour les applications de bureau dans Windows 8.1
description: Haute résolution pour les applications de bureau dans Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6c223e9dc39cda9a109280926a5eb47a8fffcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509860"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a>Haute résolution pour les applications de bureau dans Windows 8.1

## <a name="platforms"></a>Plateformes

<dl> Clients-Windows 8.1  
Serveurs-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

Dans Windows 8.1 les applications de bureau sont censées s’exécuter sur des affichages avec une mise à l’échelle de 200% en plus des 100%, 125% et 150% de mise à l’échelle pris en charge dans Windows 8. En outre, les applications de bureau sont mises à l’échelle sur une base par moniteur plutôt que sur un seul facteur d’échelle appliqué à tous les affichages. Les développeurs peuvent également appeler de nouvelles API dans Windows 8.1 pour bénéficier de facteurs d’échelle par moniteur.

## <a name="manifestations"></a>Manifestations

Les utilisateurs peuvent utiliser de nouveaux affichages à haute densité avec Windows 8.1 pour une expérience visuelle formidable qui tire parti des données de pixel supérieures. Si les applications ne gèrent pas les résolutions élevées, Windows les met à l’échelle pour l’utilisateur. En outre, les utilisateurs peuvent utiliser un mélange d’affichages haute densité et à faible densité sur le même ordinateur, et Windows met à l’échelle le contenu de manière appropriée pour chaque affichage. Il s’agit d’une amélioration par rapport à Windows 8, où le contenu peut être trop volumineux sur certains affichages.

## <a name="mitigation"></a>Limitation des risques

Étant donné que Windows mettra à l’échelle les applications qui ne sont pas mises à l’échelle, les développeurs n’ont généralement pas à effectuer d’autres tâches, mais les développeurs qui investissent dans l’écriture d’applications prenant en charge la haute résolution auront un avantage concurrentiel, car ces applications s’apprendront mieux sur les nouveaux ordinateurs portables haute résolution et les moniteurs de bureau.

## <a name="solution"></a>Solution

La création d’une application qui peut tirer parti de la haute résolution est une tâche de conception et d’implémentation complexe. Consultez les liens ci-dessous pour obtenir des informations sur les didacticiels, créer du contenu de présentation et une prise en charge similaire.

## <a name="tests"></a>Tests

Même si les développeurs choisissent de faire en sorte que leurs applications tirent parti de la haute résolution, ils doivent tester leur application à 100%, 125%, 150% et 200% de mise à l’échelle pour s’assurer que l’expérience de l’utilisateur final est satisfaisante et concurrentielle.

## <a name="resources"></a>Ressources

-   [Livre blanc et didacticiel sur les résolutions élevées en Windows 8.1](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [Exemples de programmes de bureau Windows](https://www.microsoft.com/?ref=go)
-   [GÉNÉRATION d’une session de disjoncteur 2013 sur des résolutions élevées en Windows 8.1](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 