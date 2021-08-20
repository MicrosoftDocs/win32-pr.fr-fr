---
title: Haute résolution pour les applications de bureau dans Windows 8.1
description: Haute résolution pour les applications de bureau dans Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbef80ce11de41ca50b7cf5ce4076b294b9331b62be417686f7ba0a3a63b98dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852425"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a>Haute résolution pour les applications de bureau dans Windows 8.1

## <a name="platforms"></a>Plateformes

<dl> Clients-Windows 8.1  
serveurs-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

dans Windows 8.1 les applications de bureau sont censées s’exécuter sur des affichages avec une mise à l’échelle de 200% en plus des 100%, 125% et 150% de mise à l’échelle pris en charge dans Windows 8. En outre, les applications de bureau sont mises à l’échelle sur une base par moniteur plutôt que sur un seul facteur d’échelle appliqué à tous les affichages. les développeurs peuvent également appeler de nouvelles api dans Windows 8.1 pour bénéficier de facteurs d’échelle par moniteur.

## <a name="manifestations"></a>Manifestations

les utilisateurs peuvent utiliser de nouveaux affichages à haute densité avec Windows 8.1 pour une expérience visuelle formidable qui tire parti des données de pixel supérieures. si les applications ne gèrent pas les résolutions élevées, Windows les met à l’échelle pour l’utilisateur. en outre, les utilisateurs peuvent utiliser un mélange d’affichages haute et faible densité sur le même ordinateur, et Windows mettra à l’échelle le contenu de manière appropriée pour chaque affichage. il s’agit d’une amélioration par rapport à Windows 8, où le contenu peut être trop volumineux sur certains affichages.

## <a name="mitigation"></a>Limitation des risques

étant donné que Windows mettra à l’échelle des applications qui ne sont pas mises à l’échelle, les développeurs n’ont généralement pas besoin d’effectuer des tâches supplémentaires, mais les développeurs qui investissent dans l’écriture d’applications prenant en charge la haute résolution auront un avantage concurrentiel, car ces applications seront mieux adaptées aux nouveaux ordinateurs portables haute résolution et moniteurs de bureau.

## <a name="solution"></a>Solution

La création d’une application qui peut tirer parti de la haute résolution est une tâche de conception et d’implémentation complexe. Consultez les liens ci-dessous pour obtenir des informations sur les didacticiels, créer du contenu de présentation et une prise en charge similaire.

## <a name="tests"></a>Tests

Même si les développeurs choisissent de faire en sorte que leurs applications tirent parti de la haute résolution, ils doivent tester leur application à 100%, 125%, 150% et 200% de mise à l’échelle pour s’assurer que l’expérience de l’utilisateur final est satisfaisante et concurrentielle.

## <a name="resources"></a>Ressources

-   [Livre blanc et didacticiel sur les résolutions élevées en Windows 8.1](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [exemples de programmes de bureau Windows](https://www.microsoft.com/?ref=go)
-   [GÉNÉRATION d’une session de disjoncteur 2013 sur des résolutions élevées en Windows 8.1](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 