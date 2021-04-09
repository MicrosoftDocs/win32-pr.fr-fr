---
description: Cette rubrique explique comment afficher les données du programme à imprimer.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 'Comment : afficher les données d’un travail d’impression'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2d9f8cbf68394fd56ebcf31cfb37ee8f337f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868533"
---
# <a name="how-to-render-print-job-data"></a>Comment : afficher les données d’un travail d’impression

Cette rubrique explique comment afficher les données du programme à imprimer. Cette rubrique n’explique pas en détail comment restituer des graphiques ou des images de texte spécifiques. Au lieu de cela, il décrit comment gérer les données du programme et les afficher sous la forme d’un document XPS, qu’il envoie à une imprimante à l’aide de l' [API d’impression XPS](xps-printing.md).

## <a name="overview"></a>Vue d’ensemble

Le rendu des données de travail d’impression pour l’impression implique de placer les données spécifiques au programme, telles que le texte, les images et la mise en forme, et de les convertir dans un format compatible avec l’imprimante de destination. Le programme qui envoie les données à l’imprimante doit l’envoyer dans le format requis par le pilote d’imprimante.

Utilisez l' [API d’impression XPS](xps-printing.md) pour envoyer les données à l’imprimante et les données doivent être formatées en tant que document XPS. Pour produire le contenu du document XPS dont l’API d’impression XPS a besoin, l’exemple de programme utilise l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).

Si le contenu du programme est dans un format qui n’est pas compatible avec une imprimante, il doit être rendu avant d’être envoyé à l’imprimante. Si le programme utilise l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) pour gérer son contenu de programme, le contenu du programme sera dans un format qui peut être envoyé directement à l' [API d’impression XPS](xps-printing.md) et ne nécessitera pas de rendu supplémentaire avant de l’envoyer à l’imprimante.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[API d’impression XPS](xps-printing.md)
</dt> </dl>

 

 
