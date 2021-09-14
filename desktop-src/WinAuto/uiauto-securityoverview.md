---
title: Considérations relatives à la sécurité pour les technologies d’assistance
description: les technologies d’assistance sont des applications qui s’exécutent sur le bureau Windows et aident les utilisateurs à interagir avec le système d’exploitation et d’autres applications qui s’exécutent sur l’ordinateur, y compris les applications dans la nouvelle interface utilisateur de Windows.
ms.assetid: 0c3689e1-2124-4142-b0bd-233e95ee1285
f1_keywords:
- vs.debug.error.launch_elevation_requirements
keywords:
- attribut uiAccess
- UI Automation, attribut uiAccess
- sécurité, attribut uiAccess
- requestedExecutionLevel (balise)
- UI Automation, balise requestedExecutionLevel
- UI Automation, considérations sur la sécurité
- UI Automation, fichiers manifeste
- fichiers manifeste
- contrôle de compte d’utilisateur
- sécurité, contrôle de compte d’utilisateur
- sécurité, fichiers manifeste
- sécurité, balise requestedExecutionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f2f5cf006c0adaf9b170a4ed11abd9afd52012
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292487"
---
# <a name="security-considerations-for-assistive-technologies"></a>Considérations relatives à la sécurité pour les technologies d’assistance

les technologies d’assistance sont des applications qui s’exécutent sur le bureau Windows et aident les utilisateurs à interagir avec le système d’exploitation et d’autres applications qui s’exécutent sur l’ordinateur, y compris les applications dans la nouvelle interface utilisateur de Windows. Les applications de technologie d’assistance fonctionnent en récupérant des informations du système d’exploitation et d’autres applications, puis en présentant les informations d’une manière accessible à l’utilisateur. Une application de technologie d’assistance peut également « piloter » par programmation le système d’exploitation et d’autres applications en fonction de l’entrée de l’utilisateur.

La nature des applications de technologie d’assistance exige qu’elles intertraitent les limites et qu’elles aient accès à des processus qui s’exécutent à un niveau d’intégrité plus élevé (IL). (Une application de technologie d’assistance s’exécute au moyen du langage intermédiaire.) par exemple, lorsque l’utilisateur tente d’effectuer une tâche qui requiert des privilèges d’administrateur, Windows présente une boîte de dialogue demandant à l’utilisateur de continuer. Cette boîte de dialogue s’exécute à un IL plus élevé pour le protéger de la communication entre processus, afin que les logiciels malveillants ne puissent pas simuler l’entrée utilisateur. De même, l’écran d’ouverture de session de bureau s’exécute à un IL plus élevé pour l’empêcher d’être accessible à d’autres processus.

Les applications de technologie d’assistance doivent généralement accéder aux éléments de l’interface utilisateur du système protégé, ou à d’autres processus qui peuvent s’exécuter à un niveau de privilège plus élevé. Par conséquent, les applications de technologie d’assistance doivent être approuvées par le système et doivent s’exécuter avec des privilèges spéciaux.

Pour obtenir l’accès à des processus IL plus élevés, une application de technologie d’assistance doit définir l’indicateur UIAccess dans le manifeste de l’application et être lancé par un utilisateur disposant de privilèges d’administrateur.

> [!NOTE]
> Les privilèges d’accès sont limités comme suit :
>
> - Une application qui n’a pas de UIAccess dans le manifeste commence par le langage intermédiaire moyen et ne peut pas accéder à l’interface utilisateur du processus avec élévation de privilèges (IL est de taille moyenne + « IL ».
> - Une application qui possède l’UIAccess dans le manifeste et qui est lancée par un utilisateur qui ne se trouve pas dans le groupe administrateurs, commence par le langage intermédiaire « moyen + » et ne peut pas accéder à l’interface utilisateur avec élévation de privilèges (rien ne s’exécute en langage intermédiaire « élevé », comme les applications lancées par un **clic droit > exécuter en tant qu’administrateur**).
> - Une application dispose d’un accès à l’interface utilisateur et elle est lancée par un utilisateur administrateur qui démarre en tant qu’il « High » et peut accéder à l’interface utilisateur avec élévation de privilèges, car elle a le même il.
>
> L’UIAccess n’est pas suffisant pour qu’un processus se déplace jusqu’à la limite IL.

En plus d’avoir accès à des processus IL plus élevés, une application de technologie d’assistance avec ces privilèges peut s’exécuter en tant qu’application de niveau supérieur dans l’ordre de plan à tout moment, ce qui signifie qu’une application de technologie d’assistance peut être visible et disponible chaque fois que l’utilisateur en a besoin.

> [!Important]
> Aucun des scénarios ci-dessus ne permet d’accéder à l’interface utilisateur qui s’exécute sous le système IL. Cela est possible uniquement si le processus est lancé dans le Bureau de contrôle de compte d’utilisateur (UAC) sous système (et IL système). Dans ce cas, la définition de l’UIAccess n’a aucun effet.

## <a name="uiaccess-requirements-for-assistive-technology-applications"></a>Exigences UIAccess pour les applications de technologie d’assistance

une application de technologie d’assistance est une application de bureau Windows Windows qui interagit avec d’autres processus en cours d’exécution sur le bureau et dans la nouvelle interface utilisateur de Windows pour obtenir des informations à partir du système et des applications. L’application de technologie d’assistance peut ensuite fournir les informations aux utilisateurs d’accessibilité.

Une application de technologie d’assistance obtient l’accès à d’autres processus en définissant l’indicateur UIAccess dans le manifeste de l’application. Pour utiliser l’indicateur UIAccess, une application de technologie d’assistance doit remplir les conditions suivantes.

-   Exigez l’affichage, l’interaction ou la prise en compte des informations provenant d’une autre application pour fournir des informations pour un scénario d’accessibilité, et/ou
-   Pour obtenir ou afficher ces informations, exigez l’exécution en tant que fenêtre supérieure.

Pour utiliser l’UIAccess, une application de technologie d’assistance doit :

-   Être signé avec un certificat pour interagir avec les applications qui s’exécutent à un niveau de privilège supérieur.
-   Être approuvé par le système. L’application doit être installée dans un emplacement sécurisé nécessitant l’accès à une invite de contrôle de compte d’utilisateur (UAC). Par exemple, le dossier Program Files.
-   Être généré avec un fichier manifeste qui comprend l’indicateur uiAccess.

L’UIAccess ne doit pas être utilisé :

-   Par les applications qui ne sont pas des technologies d’assistance.
-   Par les applications de technologie d’assistance qui affichent des informations ou une interface utilisateur qui ne s’applique pas au scénario d’accessibilité qu’ils ciblent.
-   par les applications qui souhaitent juste apparaître au-dessus d’autres applications dans la nouvelle interface utilisateur du Windows.
    > [!Note]  
    > les Applications développées pour la nouvelle Windows UI n’ont pas UIAccess comme option disponible.

     

## <a name="setting-uiaccess-in-the-application-manifest-file"></a>Définition de l’UIAccess dans le fichier manifeste de l’application

Pour accéder à l’interface utilisateur du système protégé, les applications doivent être générées avec un fichier manifeste qui comprend un attribut spécial dans le fichier manifeste. Cet attribut **UIAccess** est inclus dans la balise **requestedExecutionLevel** , comme illustré dans l’exemple de code suivant.


```XML
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"> 
    <security> 
        <requestedPrivileges> 
        <requestedExecutionLevel 
            level="highestAvailable" 
            uiAccess="true" /> 
        </requestedPrivileges> 
    </security> 
</trustInfo> 
```



La valeur de l’attribut **Level** dans ce code est un exemple uniquement.

L' **UIAccess** est « false » par défaut. Si l’attribut est omis ou s’il n’existe aucun manifeste, l’application ne peut pas accéder à l’interface utilisateur protégée.

pour plus d’informations sur la sécurité des Windows, sur la signature des applications et sur la création de manifestes, consultez [les Windows vista et Windows Server 2008 developer Story : Windows vista Application Development requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)) sur MSDN.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Notions de base d’UI Automation](entry-uiautocore-overview.md)
</dt> </dl>

 

 