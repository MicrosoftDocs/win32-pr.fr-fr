---
description: Lorsque le système d’exploitation, ou même une application, est configuré pour utiliser une langue et des paramètres régionaux particuliers, de nombreux paramètres sont affectés.
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: Paramètres des paramètres régionaux du Document et du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed43ae52d7626b759563069b05fe4ae03649feb63fd1af8dab1b80cfd4d558a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594779"
---
# <a name="document-and-system-locale-settings"></a>Paramètres des paramètres régionaux du Document et du système

Lorsque le système d’exploitation, ou même une application, est configuré pour utiliser une langue et des paramètres régionaux particuliers, de nombreux paramètres sont affectés. Ces paramètres incluent le format numérique, le format de date, le format monétaire, le mappage en majuscules et en minuscules, l’ordre de tri du dictionnaire, la création de jetons et d’autres. bien que ces paramètres aident Windows recherche à fournir une excellente prise en charge localisée, des résultats inattendus peuvent se produire lorsque des documents d’un paramètre régional sont recherchés à l’aide d’un système défini sur un autre paramètre régional.

Lorsque l’objet [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) traite les propriétés et le contenu de texte d’un document, il signale la langue de ce document à l’indexeur de contenu. à l’aide de ces informations, Windows recherche peut appliquer l’analyseur lexical approprié.

 

 
