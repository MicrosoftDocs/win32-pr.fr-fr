---
description: .
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8-chaîne de l’agent utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aea44572f32e252a4e1d4dc2209e411834c12d4
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314792"
---
# <a name="internet-explorer-8---user-agent-string"></a>Internet Explorer 8-chaîne de l’agent utilisateur

## <a name="affected-platforms"></a>Plateformes affectées

 **Clients** -Windows XP, Windows Vista, Windows 7  
**Serveurs** -windows Server 2003, windows Server 2008, windows Server 2008 R2  










## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -moyenne  
**Fréquence** -élevée  











## <a name="description"></a>Description

La chaîne de l’agent utilisateur est l’identificateur Internet Explorer qui fournit des données sur sa version et d’autres attributs aux serveurs Web. De nombreuses applications Web s’appuient sur la chaîne de l’agent utilisateur d’IE. Celles qui le font et dépendent d’un numéro de version antérieure seront affectées. La chaîne de l’agent utilisateur comprend désormais la chaîne « Trident/4.0 » afin d’autoriser la différenciation entre la chaîne de l’agent utilisateur d’Internet Explorer 7 et la chaîne de l’agent utilisateur d’Internet Explorer 8 lors de l’exécution dans l’affichage de compatibilité d’Internet Explorer 7. Pour plus d’informations, consultez Description des chaînes de l’agent utilisateur.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

Il y a deux zones affectées :

-   Les pages Web qui vérifient explicitement la chaîne de l’agent utilisateur et ne prennent pas en charge la chaîne de l’agent utilisateur d’Internet Explorer 8 peuvent ne pas s’exécuter correctement. Dans la plupart des cas, cela signifie que les pages seront bloquées par les utilisateurs du contenu auquel ils tentent d’accéder ou affichent du contenu incorrect ou incorrect.
-   Les applications qui hébergent Trident (voir hébergement et réutilisation) utilisent par défaut Internet Explorer 7 en utilisant le composant Web facultatif, mais n’ont pas accès aux fonctionnalités d’Internet Explorer 8.

## <a name="solution"></a>Solution

Assurez-vous que vos applications gèrent correctement la nouvelle version « MSIE 8,0 » dans la chaîne de l’agent utilisateur. Vous pouvez également vous abonner à l’affichage de compatibilité d’Internet Explorer 7 pour ces applications basées sur Internet Explorer 7. Pour ce faire, vous pouvez utiliser des balises méta. Pour plus d’informations, consultez la rubrique Présentation des chaînes de l’agent utilisateur.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilité, performances, fiabilité et test d’utilisabilité

-   Exécutez vos applications et pages Web dans un environnement Internet Explorer 8 sous Windows Vista ou Windows XP pour vous assurer qu’elles se comportent de la manière souhaitée.
-   Vous pouvez également exécuter l’outil de test de compatibilité Internet Explorer (IECTT) fourni avec Application Compatibility Toolkit (ACT) pour localiser les problèmes potentiels liés aux mises à jour des fonctionnalités de sécurité.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Fonctionnement des chaînes de l’agent utilisateur](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))
-   [Chaîne de User-Agent d’Internet Explorer 8](/archive/blogs/ie/)
-   [Vecteur de version et de chaîne de l’agent utilisateur](https://archive.msdn.microsoft.com/ie8whitepapers)
-   [Hébergement et réutilisation](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))
-   [Téléchargement de l’outil Application Compatibility Toolkit](/windows-hardware/get-started/adk-install)
-   [Problèmes connus liés aux fonctionnalités de sécurité d’Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
