---
description: 'il y a quatre couches dans la bibliothèque d’analyse d’encre : Windows Forms, WPF, COM et la couche de base. Cette section explique quand utiliser chaque couche.'
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Utilisation de l’API analyse de l’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdfada58868c7fe959f832e0c1243bc91a373fb0186d8deee2f9481d78a95714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032347"
---
# <a name="ink-analysis-api-usage"></a>Utilisation de l’API analyse de l’encre

il y a quatre couches dans la bibliothèque d’analyse d’encre : Windows Forms, WPF, COM et la couche de base. Cette section explique quand utiliser chaque couche.

## <a name="ink-analysis-api-overview"></a>Vue d’ensemble de l’API d’analyse d’encre

Les bibliothèques d’analyse de l’encre sont conçues pour être utilisées dans un large éventail d’environnements de programmation pris en charge. Il existe quatre couches de base par lesquelles votre application peut utiliser l’analyse de l’encre. Ces couches sont les suivantes :

-   couche Windows Forms
-   Couche WPF
-   Couche COM
-   Couche de base

### <a name="windows-forms-applications"></a>Applications Windows Forms

Vous pouvez utiliser l’API d’analyse d’encre dans votre projet managé en ajoutant une référence aux bibliothèques suivantes :

-   Microsoft. Ink. Analysis (Microsoft.Ink.Analysis.dll)
-   Bibliothèque d’analyse de documents manuscrits (IACore.dll)

dans Windows Forms applications, vous utiliserez très probablement les bibliothèques conjointement avec les objets de plateforme tablet pc standard qui se trouvent dans l’assembly v 1.7 de l’API Microsoft tablet pc. Vérifiez que vous avez également une référence à :

-   API Microsoft Tablet PC v 1.7.2600.2180 (Microsoft.Ink.dll)

### <a name="windows-presentation-framework-applications"></a>Windows Applications de l’infrastructure de présentation

Vous pouvez utiliser l’API d’analyse d’encre dans votre projet WPF en ajoutant une référence aux membres de l’analyse d’encre qui sont définis dans le système. Windows. Espace de noms Ink dans l’assembly IAWinFX.dll. Cet assembly est installé par le kit de développement logiciel (SDK).

### <a name="com-applications"></a>Applications COM

Les applications COM non-Automation doivent utiliser la couche COM des API d’analyse de l’encre.

Les objets [ContextNode](/previous-versions/ms551996(v=vs.100)) spécifiques de type, tels que [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100))et others, ne sont pas utilisés dans la couche com. Au lieu de cela, vous devez utiliser [**IContextNode :: AddPropertyData**](icontextnode-addpropertydata.md) sur l’interface [**IContextNode**](icontextnode.md) standard.

Vous devez \# inclure « IACom. h ». Vous utiliserez très probablement les bibliothèques dans le cadre de l’objet Ink de plateforme Tablet PC. par conséquent, vous devez également \# inclure « msinkaut. h ».

### <a name="rts-and-other-applications"></a>RTS et d’autres applications

La couche de base de l’analyse d’encre fonctionne différemment des autres en ce sens qu’elle prend des données de point pour l’analyse plutôt que des objets [Stroke](/previous-versions/ms552692(v=vs.100)) . des exemples d’utilisation directe de la couche de Base plutôt que d’utiliser les Windows des formes ou des couches COM sont des applications qui n’utilisent pas d’objets ink de plateforme tablet pc de première génération, ou des applications qui utilisent les api [**RealTimeStylus**](realtimestylus-class.md) pour gérer l’entrée de stylet au lieu d’utiliser les objets [ink](/previous-versions/ms583670(v=vs.100)) de plateforme tablet pc.

## <a name="32-bit-support-only"></a>32 bits pris en charge uniquement

Notez que les bibliothèques d’analyse de l’encre sont uniquement prises en charge dans les processus 32 bits.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Présentation de l’analyse de l’encre](ink-analysis-overview.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 
