---
description: Windows GDI+ est une API basée sur une classe pour les programmeurs C/C++.
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0dac72d27ba52071797b51573141506d5b0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112951"
---
# <a name="gdi"></a>GDI+

## <a name="purpose"></a>Objectif

Windows GDI+ est une API basée sur une classe pour les programmeurs C/C++. Elle permet aux applications d’utiliser des graphiques et du texte mis en forme à la fois sur l’écran vidéo et sur l’imprimante. Les applications basées sur l'API Microsoft Win32 n'accèdent pas directement au matériel graphique. À la place, GDI+ interagit avec les pilotes de périphérique pour le compte des applications. GDI+ est également pris en charge par Microsoft Win64.

## <a name="where-applicable"></a>Le cas échéant

Les fonctions et les classes GDI+ ne sont pas prises en charge pour une utilisation dans un service Windows. Toute tentative d’utilisation de ces fonctions et classes à partir d’un service Windows peut entraîner des problèmes inattendus, tels que des performances de service réduites et des exceptions ou des erreurs d’exécution.

> [!Note]  
> Lorsque vous utilisez l’API GDI+, vous ne devez jamais autoriser votre application à télécharger des polices arbitraires à partir de sources non approuvées. Le système d’exploitation requiert des privilèges élevés pour s’assurer que toutes les polices installées sont approuvées.

## <a name="developer-audience"></a>Développeurs concernés

L’interface basée sur la classe C++ GDI+ est conçue pour être utilisée par les programmeurs C/C++. Vous devez vous familiariser avec l’interface utilisateur graphique de Windows et l’architecture pilotée par les messages.

## <a name="run-time-requirements"></a>Conditions d’exécution

GDI+ peut être utilisé dans toutes les applications Windows. GDI+ a été introduit dans Windows XP et Windows Server 2003. Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser une classe ou une méthode particulière, consultez la section plus d’informations de la documentation relative à la classe ou à la méthode.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique                                                    | Description                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [Vue d'ensemble](-gdiplus-about-gdi--about.md)<br/>     | Informations générales sur GDI+.<br/>            |
| [À](-gdiplus-using-gdi--use.md)<br/>          | Tâches et exemples utilisant GDI+.<br/>             |
| [Référence](-gdiplus-class-gdi-reference.md)<br/> | Documentation de l’API basée sur la classe C++ GDI+.<br/> |

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows GDI](../gdi/windows-gdi.md)
</dt> <dt>

[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> <dt>

[Acquisition d’image Windows](../wia/-wia-startpage.md)
</dt> <dt>

[Technologie](../opengl/opengl.md)
</dt> <dt>

[Multimédia Windows](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
