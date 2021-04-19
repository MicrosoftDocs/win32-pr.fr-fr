---
description: Utilisation de .NET Framework 4 avec des applications basées sur des versions antérieures
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Utilisation de .NET Framework 4 avec des applications basées sur des versions antérieures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30eb8f4be1c50904b8d5760f456f3fe20bdd3da
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314942"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>Utilisation de .NET Framework 4 avec des applications basées sur des versions antérieures

## <a name="platform"></a>Plate-forme

 **Clients** -Windows XP, Windows Vista, Windows 7  
**Serveurs** -windows Server 2003, windows Server 2008, windows Server 2008 R2  


## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -élevée  






## <a name="description"></a>Description

Le .NET Framework 4 est hautement compatible avec les applications générées à l’aide des versions de .NET Framework antérieures. Les principales modifications apportées à .NET Framework 4 sont l’amélioration de la sécurité, de la conformité aux normes, de l’exactitude, de la fiabilité et des performances.

Toutefois, .NET Framework 4 n’utilise pas automatiquement sa version du common language runtime (CLR) pour exécuter des applications générées à l’aide de versions antérieures du .NET Framework.

## <a name="manifestation"></a>Manifestation

Si vous avez créé une application à l’aide d’un .NET Framework antérieur et qu’un utilisateur ouvre cette application sur un ordinateur qui a à la fois .NET Framework 4 et la version antérieure du .NET Framework installée, l’application utilise la version CLR antérieure.

Toutefois, si le .NET Framework 4 est la seule version du runtime qui est installée sur l’ordinateur, l’application lève une exception et invite l’utilisateur à installer la version du Runtime par rapport à laquelle vous avez créé l’application.

## <a name="solution"></a>Solution

Pour exécuter des applications générées avec des versions antérieures de .NET Framework avec .NET Framework 4, vous devez compiler votre application pour cibler la version de .NET Framework 4 en la spécifiant dans les propriétés de votre projet dans Microsoft Visual Studio, ou vous pouvez spécifier .NET Framework 4 dans l' [**<supportedRuntime> élément**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) dans un fichier de configuration de l’application.

Pour plus d’informations sur la migration vers le .NET Framework 4, consultez [Guide de migration vers le .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) et [compatibilité des versions dans le .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).

## <a name="compatibility-tests"></a>Tests de compatibilité

Après avoir apporté les modifications, testez votre application pour vous assurer qu’elle s’exécute correctement. Vous pouvez tester la compatibilité comme décrit dans la rubrique [compatibilité des applications .NET Framework 4](/previous-versions/dd889541(v=msdn.10)) .

Si votre application ou composant ne fonctionne pas après l’installation de .NET Framework 4, envoyez un bogue sur le site Web [Microsoft Connect](https://connect.microsoft.com/visualstudio) .

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [**<supportedRuntime> appartient**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Guide de migration vers .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Compatibilité de versions dans le .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **Procédure pas à pas de compatibilité des applications .NET Framework 4 RTM :**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
