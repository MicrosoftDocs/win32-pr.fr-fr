---
description: Les enregistrements splines représentent les courbes quadratiques (c’est-à-dire, les b-splines quadratiques) utilisées par TrueType.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Enregistrements spline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbaf3730f327501bd55b2e35b9410f03fd0559cbb5e36d87a3052901d26e5f0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613649"
---
# <a name="spline-records"></a>Enregistrements spline

Les enregistrements splines représentent les courbes quadratiques (c’est-à-dire, les b-splines quadratiques) utilisées par TrueType. Un enregistrement de spline commence par le dernier point de l’enregistrement précédent (ou pour le premier enregistrement du contour, avec le point de départ). Pour le premier enregistrement de spline, le point de départ et le dernier point de l’enregistrement se trouvent sur le contour du glyphe. Pour tous les autres enregistrements de spline, seul le dernier point se trouve sur le contour du glyphe. Tous les autres points des enregistrements spline sont en dehors du contour du glyphe et doivent être rendus comme des points de contrôle des b-splines.

Le dernier enregistrement de spline ou de polyligne d’un contour se termine toujours par le point de départ du contour. Cette organisation garantit que chaque contour est fermé.

Comme les b-splines nécessitent trois points (un point dépassant le contour du glyphe entre deux points du contour), vous devez effectuer des calculs quand un enregistrement de spline contient plusieurs points hors courbe.

Par exemple, si un enregistrement spline contient trois points (A, B et C) et qu’il ne s’agit pas du premier enregistrement, les points A et B sont déduits du contour du glyphe. Pour interpréter le point A, utilisez la position actuelle (qui est toujours sur le contour du glyphe) et le point sur le contour du glyphe entre les points A et B. Pour rechercher le point médian (M) entre A et B, vous pouvez effectuer le calcul suivant.

M = A + (B A)/2

Le point médian entre des points consécutifs hors plan dans un enregistrement de spline est un point sur le contour du glyphe, en fonction de la définition du format de spline utilisé dans les polices TrueType.

Si la position actuelle est désignée par P, les deux splines quadratiques définies par cet enregistrement spline sont (P, A, M) et (M, B, C).

 

 



