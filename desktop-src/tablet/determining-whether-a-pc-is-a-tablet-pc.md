---
description: Vous pouvez parfois être amené à déterminer si votre application s’exécute sur un Tablet PC, car vous souhaiterez peut-être que vos applications tirent parti des fonctionnalités d’encre, de reconnaissance et de stylet inhérentes.
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: Déterminer si un PC est un Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c793d5531d6091d4bce73d99bfa32d100c2b9304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545047"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a>Déterminer si un PC est un Tablet PC

Vous pouvez parfois être amené à déterminer si votre application s’exécute sur un Tablet PC, car vous souhaiterez peut-être que vos applications tirent parti des fonctionnalités d’encre, de reconnaissance et de stylet inhérentes. Pour vous aider à déterminer si votre application a accès aux fonctionnalités Tablet PC, vous pouvez utiliser l’appel d’API Windows GetSystemMetrics () comme décrit dans cette rubrique.

## <a name="client-side-applications"></a>Applications Client-Side

Vous pouvez utiliser les techniques suivantes pour déterminer si votre code s’exécute sur un Tablet PC.

-   [Utilisation de GetSystemMetrics (SM \_ TABLETPC)](/windows)
-   [Utilisation de la présence de fichiers binaires de plateforme de tablette](#using-the-presence-of-tablet-platform-binaries)
-   [Applications Web](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a>Utilisation de GetSystemMetrics (SM \_ TABLETPC)

### <a name="windows-xp-tablet-pc-edition"></a>Windows XP Édition Tablet PC

Dans Microsoft Windows XP Tablet PC Edition, utilisez la fonction GetSystemMetrics (SM \_ TABLETPC) pour déterminer si un ordinateur est un Tablet PC. GetSystemMetrics (SM \_ TABLETPC) est conçu pour retourner la valeur true sur un ordinateur exécutant Windows XP Édition Tablet PC.

### <a name="windows-vista"></a>Windows Vista

Dans Windows Vista, il n’existe plus de kit de développement logiciel (SDK) Tablet PC distinct. Le SDK Windows contient maintenant une section appelée « technologie Tablet PC et Touch », et la logique de GetSystemMetrics (SM \_ TABLETPC) a été modifiée pour en tenir compte. GetSystemMetrics (SM \_ TABLETPC) renvoie désormais la valeur true si toutes les conditions suivantes sont vraies :

-   Il existe un digitaliseur intégré, à savoir PEN ou Touch, sur le système.
-   Le composant facultatif Tablet PC est installé. Ce composant contient des fonctionnalités telles que le panneau de saisie Tablet PC et le journal Windows.
-   L’ordinateur est concédé sous licence pour utiliser le composant facultatif. Les versions Premium de Windows Vista, telles que Windows Vista Édition familiale Premium, Windows Vista petite entreprise, Windows Vista Professionnel, Windows Vista entreprise et Windows Vista Édition intégrale, sont concédées sous licence pour utiliser le composant facultatif.
-   Le service d’entrée du Tablet PC est en cours d’exécution. Tablet PC Input service est un nouveau service pour Windows Vista qui contrôle l’entrée Tablet PC.

Avec cette précision accrue, GetSystemMetrics (SM \_ TABLETPC) continue d’être la méthode recommandée pour déterminer si un ordinateur exécutant Windows Vista est un Tablet PC.

### <a name="using-the-presence-of-tablet-platform-binaries"></a>Utilisation de la présence de fichiers binaires de plateforme de tablette

Dans Windows XP Édition Tablet PC et Windows Vista, vous pouvez rechercher la présence des binaires manuscrits, tels que inkobj.dll et Microsoft.Ink.dll, et utiliser leurs fonctionnalités prises en charge si elles sont présentes.

Dans Windows Vista, les fichiers binaires de la plateforme Tablet PC sont installés par défaut sur toutes les versions du client. Les fonctionnalités d’entrée et d’entrée manuscrite sont disponibles sur ces versions. La reconnaissance n’est disponible que dans les versions Premium de Windows Vista.

### <a name="web-based-applications"></a>Applications Web-Based

Dans Windows Vista, la chaîne de l’agent utilisateur signalée par Internet Explorer comprend « Tablet PC 2,0 » si, selon GetSystemMetrics (SM \_ TABLETPC), l’appareil est un Tablet PC.

Dans Windows XP Édition Tablet PC 2005, la chaîne User-agent comprend Tablet PC 1,7. La chaîne User-agent ressemble à ce qui suit :

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

Utilisez cette valeur pour déterminer si l’ordinateur client est un Tablet PC et prend en charge les contrôles d’encrage basés sur le Web.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
