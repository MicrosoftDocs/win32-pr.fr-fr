---
description: Internet Explorer 8-protection de l’exécution des données/NX
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8-protection de l’exécution des données/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0208cc20e78c30f42b09af78460990be20b002
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221900"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a>Internet Explorer 8-protection de l’exécution des données/NX

## <a name="affected-platforms"></a>Plateformes affectées

 **Clients** -Windows XP, Windows Vista, Windows 7  
**serveurs** -Windows server 2003, Windows server 2008, Windows server 2008 R2  










> [!Note]  
> Internet Explorer 8 activera la protection DEP/NX lorsqu’elle sera exécutée sur un système d’exploitation avec la dernière Service Pack. Windows XP sp3, Windows server 2003 sp3, Windows Vista SP1 et Windows server 2008 ont tous la valeur DEP/NX activée par défaut dans Internet Explorer 8.

 

## <a name="feature-impact"></a>Impact sur les fonctionnalités

**Gravité** -moyenne  
**Fréquence** -faible  

> [!Note]  
> En règle générale, les applications qui s’exécutent dans Internet Explorer et qui ne sont pas compatibles avec DEP/NX se bloqueront au démarrage et ne fonctionneront pas. Internet Explorer peut se bloquer au démarrage si des modules complémentaires qui ne sont pas compatibles avec DEP/NX sont installés.

 

## <a name="description"></a>Description

DEP/NX est une fonctionnalité de sécurité qui permet d’atténuer les vulnérabilités liées à la mémoire. À compter d’Internet Explorer 8, tous les processus Internet Explorer activent la fonctionnalité DEP/NX par défaut.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

le noyau Windows surveille l’exécution d’un programme. Si le noyau détecte une tentative d’exécution du code à partir d’une page de mémoire qui n’est pas marquée comme exécutable, le noyau interrompt l’exécution du programme, ce qui provoque un « incident ». Il s’agit d’une mesure de sécurité qui permet de s’assurer que les vulnérabilités liées à la mémoire (par exemple, les débordements de mémoire tampon) de l’application ne peuvent pas être exploitées pour exécuter du code arbitraire.

## <a name="end-user-mitigation"></a>Atténuation des End-User

-   Installez une version ultérieure du module complémentaire ou de l’infrastructure compatible avec DEP/NX.
-   Exécutez Internet Explorer avec élévation de privilèges en tant qu’administrateur, puis désactivez la case à cocher DEP/NX à l’aide de la case à cocher **activer la protection de la mémoire pour atténuer les attaques en ligne** sous l’onglet **options**  /  **avancées** d’Internet.

## <a name="developer-solution"></a>Solution de développeur

Compilez les applications à l’aide des dernières versions des frameworks compatibles avec DEP.

## <a name="leveraging-feature-capabilities"></a>Exploitation des fonctionnalités de fonctionnalités

-   Utiliser l’option de l’éditeur de liens/NXCOMPAT pour indiquer la compatibilité DEP/NX
-   Choisir votre code dans d’autres défenses disponibles, telles que la protection de la pile (/GS), la gestion sécurisée des exceptions (/SafeSEH) et l’ASLR (/DynamicBase)

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilité, performances, fiabilité et test d’utilisabilité

-   testez votre code avec DEP/NX activé à l’aide de la dernière version publiée d’Internet Explorer sur Windows Vista SP1 ou version ultérieure.
-   testez avec Internet Explorer 7 sur Windows Vista après l’activation de l’option DEP/NX. Pour activer DEP/NX pour Internet Explorer 7, exécutez Internet Explorer en tant qu’administrateur, puis activez la case à cocher appropriée dans les outils > options Internet > onglet Avancé.
-   exécutez l’outil de Test de compatibilité Internet Explorer (IECTT), fourni avec le Shared Computer Toolkit de compatibilité des applications (ACT) pour localiser les problèmes potentiels en raison des modifications DEP/NX.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Sécurité d’Internet Explorer 8, partie I : protection de la mémoire DEP/NX](/archive/blogs/ie/)
-   [Prévention de l’exécution des données](../memory/data-execution-prevention.md)
-   [nouvelles api NX ajoutées à Windows Vista SP1, Windows XP SP3 et Windows Server 2008 R2](/archive/blogs/michael_howard/)
-   [compatibilité des applications Shared Computer Toolkit téléchargement](/windows-hardware/get-started/adk-install)
-   [Problèmes connus liés aux fonctionnalités de sécurité d’Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
