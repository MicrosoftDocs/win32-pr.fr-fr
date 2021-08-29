---
description: Vous pouvez parfois être amené à déterminer si votre application s’exécute sur un Tablet PC, car vous souhaiterez peut-être que vos applications tirent parti des fonctionnalités d’encre, de reconnaissance et de stylet inhérentes.
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: Déterminer si un PC est un Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4672f450f23fd3ed6a6ad45df0c74ca23328b0b3735e66fceef6713a4c96a3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940909"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a>Déterminer si un PC est un Tablet PC

Vous pouvez parfois être amené à déterminer si votre application s’exécute sur un Tablet PC, car vous souhaiterez peut-être que vos applications tirent parti des fonctionnalités d’encre, de reconnaissance et de stylet inhérentes. pour vous aider à déterminer si votre application a accès aux fonctionnalités Tablet PC, vous pouvez utiliser l’appel d’API GetSystemMetrics () Windows comme décrit dans cette rubrique.

## <a name="client-side-applications"></a>Applications Client-Side

Vous pouvez utiliser les techniques suivantes pour déterminer si votre code s’exécute sur un Tablet PC.

-   [Utilisation de GetSystemMetrics (SM \_ TABLETPC)](/windows)
-   [Utilisation de la présence de fichiers binaires de plateforme de tablette](#using-the-presence-of-tablet-platform-binaries)
-   [Applications Web](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a>Utilisation de GetSystemMetrics (SM \_ TABLETPC)

### <a name="windows-xp-tablet-pc-edition"></a>Windows XP Édition Tablet PC

dans Microsoft Windows XP édition Tablet pc, utilisez la fonction GetSystemMetrics (SM \_ TABLETPC) pour déterminer si un ordinateur est un Tablet pc. GetSystemMetrics (SM \_ TABLETPC) est conçu pour retourner la valeur TRUE sur un ordinateur exécutant Windows XP édition Tablet PC.

### <a name="windows-vista"></a>Windows Vista

dans Windows Vista, il n’existe plus de kit de développement logiciel (SDK) Tablet PC distinct. le SDK Windows contient maintenant une section appelée « technologie Tablet pc et Touch », et la logique de GetSystemMetrics (SM \_ TABLETPC) a été modifiée pour en tenir compte. GetSystemMetrics (SM \_ TABLETPC) renvoie désormais la valeur true si toutes les conditions suivantes sont vraies :

-   Il existe un digitaliseur intégré, à savoir PEN ou Touch, sur le système.
-   Le composant facultatif Tablet PC est installé. ce composant contient des fonctionnalités telles que le panneau de saisie Tablet PC et le Journal Windows.
-   L’ordinateur est concédé sous licence pour utiliser le composant facultatif. Premium versions de Windows vista, telles que Windows vista édition Premium, Windows vista Small Business, Windows vista Professional, Windows vista Enterprise et Windows vista Ultimate, sont concédées sous licence pour utiliser le composant facultatif.
-   Le service d’entrée du Tablet PC est en cours d’exécution. le service d’entrée tablet pc est un nouveau service pour Windows Vista qui contrôle l’entrée tablet pc.

avec cette précision accrue, GetSystemMetrics (SM \_ TABLETPC) continue d’être la méthode recommandée pour déterminer si un ordinateur exécutant Windows Vista est un Tablet PC.

### <a name="using-the-presence-of-tablet-platform-binaries"></a>Utilisation de la présence de fichiers binaires de plateforme de tablette

dans Windows XP édition Tablet PC et Windows Vista, vous pouvez rechercher la présence des binaires manuscrits, tels que inkobj.dll et Microsoft.Ink.dll, et utiliser leurs fonctionnalités prises en charge si elles sont présentes.

dans Windows Vista, les fichiers binaires de la plateforme Tablet PC sont installés par défaut sur toutes les versions du client. Les fonctionnalités d’entrée et d’entrée manuscrite sont disponibles sur ces versions. la reconnaissance n’est disponible que dans les versions premium de Windows Vista.

### <a name="web-based-applications"></a>Applications Web-Based

dans Windows Vista, la chaîne de l’agent utilisateur signalée par Internet Explorer comprend « tablet pc 2,0 » si, selon GetSystemMetrics (SM \_ TABLETPC), l’appareil est un tablet pc.

dans Windows XP édition Tablet pc 2005, la chaîne user-agent comprend Tablet pc 1,7. La chaîne User-agent ressemble à ce qui suit :

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

Utilisez cette valeur pour déterminer si l’ordinateur client est un Tablet PC et prend en charge les contrôles d’encrage basés sur le Web.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
