---
title: Vérification de la version de Windows
description: la version du système d’exploitation a été incrémentée avec la version du système d’exploitation Windows 10.
ms.assetid: 55BB7B44-1AFD-456D-9380-38B4D26E5EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710f59313f05dac95e5953c6013108987dc9bf8ad84d7eb7d8bca67a5391996b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007879"
---
# <a name="windows-version-check"></a>Vérification de la version de Windows

la version du système d’exploitation a été incrémentée avec la version du système d’exploitation Windows 10. cela signifie que le numéro de version interne de Windows 10 a également été remplacé par 10,0. Comme précédemment, nous faisons le maximum pour maintenir la compatibilité entre les applications et les appareils après un changement de version du système d’exploitation. Pour la plupart des catégories d’applications (sans dépendances de noyau), la modification n’aura pas d’impact négatif sur les fonctionnalités de l’application, et les applications existantes continueront à fonctionner correctement sur Windows 10.

## <a name="manifestations"></a>Manifestations

La manifestation de cette modification est propre à l’application. En d’autres termes, une application qui vérifie spécifiquement la version du système d’exploitation obtient un numéro de version supérieur, ce qui peut conduire aux situations suivantes :

-   Les programmes d’installation des applications peuvent ne pas être en mesure d’installer les applications, ou les applications peuvent être dans l’impossibilité de démarrer.
-   Les applications peuvent devenir instables ou se planter.
-   Les applications peuvent générer des messages d’erreur, tout en continuant de fonctionner correctement.

Certaines applications effectuent une vérification de version et transmettent simplement un avertissement aux utilisateurs. Cependant, certaines d’entre elles sont liées très étroitement à une vérification de la version (dans les pilotes ou en mode noyau pour éviter la détection). Dans ce cas, les applications échouent si une version incorrecte est détectée. Au lieu d’une vérification de la version, nous vous recommandons une des approches suivantes :

-   Si l’application dépend de fonctionnalités d’API spécifiques, veillez à cibler la version d’API correcte.
-   Le numéro de version de NTDDI (interface de pilote de périphérique NT) est incrémenté uniquement si la fonctionnalité cible de l’API change. Veillez à détecter la modification via APISet ou une autre API exposée telle qu’elle a été créée par l’équipe des fonctionnalités, et n’utilisez pas la version en tant que proxy pour une fonctionnalité ou un correctif. En cas de changements cassants, et si une vérification correcte n’est pas exposée, il s’agit d’un bogue.
-   Assurez-vous que l’application ne vérifie pas la version de manière étrange, par exemple par le biais du Registre, des versions de fichiers, des décalages, du mode noyau, des pilotes ou d’autres moyens. Si l’application doit absolument vérifier la version, utilisez les API GetVersion, qui doivent retourner le numéro principal, le numéro secondaire et le numéro de Build.
-   Si vous utilisez l’API GetVersion ou d’autres fonctions d’assistance de version, telles que [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), n’oubliez pas que le comportement de cette API a été modifié à partir de Windows 8.1. Pour plus d’informations, reportez-vous à [la documentation de l’API](../SysInfo/version-helper-apis.md) .
-   si vous possédez des applications telles qu’un logiciel anti-programme malveillant ou un pare-feu, vous devez utiliser vos canaux de commentaires habituels et via le programme Windows insider.

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a>déclaration de la compatibilité Windows 10 avec un manifeste d’application

si votre application est compatible avec Windows 10, elle peut déclarer ce fait dans le [manifeste de l’application (exécutable)](/windows/compatibility/application-executable-manifest) pour l’exécutable de l’application. cela indique au système que votre application comprend le numéro de version 10,0 du système de Windows 10 (par conséquent, l’API GetVersion ne retourne pas de version antérieure) et permet également au système de désactiver d’autres comportements de compatibilité appliqués aux applications qui ne déclarent pas Windows 10 compatibilité.

pour déclarer la compatibilité Windows 10 dans un manifeste d’application, vous devez ajouter une [section de **&lt; &gt; compatibilité**](../SbsCs/application-manifests.md#compatibility) du manifeste si aucune n’existe déjà, puis ajouter des éléments **&lt; pris en &gt; charge** pour Windows 10 et toutes les autres versions de Windows que vous souhaitez déclarer que votre application prend en charge.

l’exemple suivant montre un fichier manifeste d’application pour une application qui prend en charge toutes les versions de Windows de Windows Vista à Windows 10 :

```XML
<!-- example.exe.manifest -->
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
    <assemblyIdentity
        type="win32"
        name="Contoso.ExampleApplication.ExampleBinary"
        version="1.2.3.4"
        processorArchitecture="x86"
    />
    <description>Contoso Example Application</description>
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!-- Windows 10 -->
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
</assembly>
```

La ligne ci-dessus indiquée `* ADD THIS LINE *` indique comment cibler avec précision votre application pour Windows 10.

la déclaration de la prise en charge des Windows 10 dans le manifeste de votre application n’aura aucun effet lors de l’exécution de votre application sur les systèmes d’exploitation précédents.

## <a name="resources"></a>Ressources

-   [Shared Computer Toolkit de la compatibilité des applications téléchargement : télécharger le Windows ADK pour Windows 10](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   [Correctifs de compatibilité connus, modes de compatibilité et messages AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [API d’assistance de version](../sysinfo/version-helper-apis.md)