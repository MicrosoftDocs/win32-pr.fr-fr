---
description: L’API d’impression GDI fournit des applications avec une interface d’impression indépendante du périphérique.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: API d’impression GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc2a872b3a310ea44ddfc84103ddbd11cff61998d4884dca5f490e88c3d73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949193"
---
# <a name="gdi-print-api"></a>API d’impression GDI

L’API d’impression GDI fournit des applications avec une interface d’impression indépendante du périphérique. Utilisez cette interface si l’application utilise GDI pour afficher du texte et des graphiques.

si vous écrivez des applications pour Windows Vista ou des versions ultérieures de Windows, envisagez d’utiliser l' [api de Document xps](/previous-versions/windows/desktop/dd316976(v=vs.85)) et l' [api d’impression xps](xps-printing.md) pour utiliser les interfaces graphiques de performances supérieures prises en charge par les pilotes d’impression XPSDrv.

Cette section fournit des informations sur les rubriques suivantes.



| Rubrique                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos de l’API d’impression GDI](about-the-gdi-print-api.md)<br/>                                 | Vue d’ensemble de la fonctionnalité d’impression GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Utilisation de l’API d’impression GDI](using-the-printing-functions.md)<br/>                            | Informations sur l’utilisation de l’API d’impression GDI dans une application.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Référence de l’API d’impression GDI](gdi-print-api-reference.md)<br/>                                 | Description détaillée des fonctions, structures et autres éléments de l’API d’impression GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md)<br/> | [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) est un composant qui permet aux applications d’utiliser l’API d’impression GDI avec les imprimantes qui ont un pilote d’impression XPSDrv.<br/>                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS document Writer (MXDW)](microsoft-xps-document-writer.md)<br/>              | [Microsoft XPS document Writer (MXDW)](microsoft-xps-document-writer.md) fournit des applications avec la fonctionnalité « enregistrer en tant que XPS » ou « exporter vers XPS ». Les applications qui ne créent pas de contenu de document XPS en mode natif peuvent utiliser le MXDW pour créer des fichiers de document XPS sans utiliser l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)). Toutefois, l’API de document XPS offre à une application la possibilité d’utiliser les interfaces graphiques de performances supérieures prises en charge par les pilotes d’impression XPSDrv.<br/> |



 

Le diagramme suivant montre la relation entre l’API d’impression GDI et les autres API d’impression qu’une application peut utiliser.

![diagramme qui montre la relation entre l’API d’impression GDI et les autres API d’impression qu’une application Win32 peut utiliser](images/print-apis-gdi.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[API d’impression XPS](xps-printing.md)
</dt> <dt>

[API du spouleur d’impression](print-spooler-api.md)
</dt> <dt>

[API ticket d’impression](print-ticket-api.md)
</dt> </dl>

 

