---
description: utilisation de .NET Framework 4 avec des Applications basées sur des Versions antérieures
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: utilisation de .NET Framework 4 avec des Applications basées sur des Versions antérieures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12eb34b00cfe14a18e83e7726f1ffa962ba03f8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884750"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>utilisation de .NET Framework 4 avec des Applications basées sur des Versions antérieures

## <a name="platform"></a>Plateforme

 **Clients** -Windows XP, Windows Vista, Windows 7  
**serveurs** -Windows server 2003, Windows server 2008, Windows server 2008 R2  


## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -élevée  






## <a name="description"></a>Description

le .NET Framework 4 est hautement compatible avec les applications générées à l’aide des versions de .NET Framework antérieures. les principales modifications apportées à .NET Framework 4 sont l’amélioration de la sécurité, de la conformité aux normes, de l’exactitude, de la fiabilité et des performances.

toutefois, .NET Framework 4 n’utilise pas automatiquement sa version du common language runtime (CLR) pour exécuter des applications générées à l’aide de versions antérieures du .NET Framework.

## <a name="manifestation"></a>Manifestation

si vous avez créé une application à l’aide d’un .NET Framework antérieur et qu’un utilisateur ouvre cette application sur un ordinateur qui a à la fois .NET Framework 4 et la version antérieure du .NET Framework installée, l’application utilise la version CLR antérieure.

toutefois, si le .NET Framework 4 est la seule version du runtime qui est installée sur l’ordinateur, l’application lève une exception et invite l’utilisateur à installer la version du runtime par rapport à laquelle vous avez créé l’application.

## <a name="solution"></a>Solution

pour exécuter des applications générées avec des versions antérieures de .NET Framework avec .NET Framework 4, vous devez compiler votre application pour cibler la version de .NET Framework 4 en la spécifiant dans les propriétés de votre projet dans Microsoft Visual Studio, ou vous pouvez spécifier .NET Framework 4 dans l' [**&lt; &gt; élément supportedRuntime**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) dans un fichier de configuration de l’application.

pour plus d’informations sur la migration vers le .NET Framework 4, consultez [Guide de Migration vers le .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) et [compatibilité des versions dans le .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).

## <a name="compatibility-tests"></a>Tests de compatibilité

Après avoir apporté les modifications, testez votre application pour vous assurer qu’elle s’exécute correctement. vous pouvez tester la compatibilité comme décrit dans la rubrique [compatibilité des applications .NET Framework 4](/previous-versions/dd889541(v=msdn.10)) .

si votre application ou composant ne fonctionne pas après l’installation de .NET Framework 4, envoyez un bogue sur le site web de [Microsoft Connecter](https://connect.microsoft.com/visualstudio) .

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [**&lt;supportedRuntime, &gt; élément**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Guide de migration vers .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Compatibilité de versions dans le .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **procédure pas à pas de compatibilité des applications .NET Framework 4 RTM :**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
