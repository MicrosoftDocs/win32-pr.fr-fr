---
description: L’une des nouvelles fonctionnalités intéressantes de Tablet PC est le système d’entrée de stylet.
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: Entrée, encre et reconnaissance du stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d865e40d1779edaa2607b1754c45659609b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558270"
---
# <a name="pen-input-ink-and-recognition"></a>Entrée, encre et reconnaissance du stylet

L’une des nouvelles fonctionnalités intéressantes de Tablet PC est le système d’entrée de stylet. Tous les ordinateurs Tablet PC ont un digitaliseur sous l’écran qui accepte les entrées de stylet. Ce nouveau mécanisme d’entrée vous oblige à réfléchir à la création d’applications spécifiquement pour Tablet PC. L’interface de programmation d’applications (API) Tablet PC Platform vous aide à effectuer cette opération.

## <a name="collection-data-management-and-recognition"></a>Collection, Gestion des données et reconnaissance

La plateforme Tablet PC peut être divisée en trois zones distinctes :

-   Collection d’encres (objets utilisés pour collecter l’encre du digitaliseur).
-   Gestion des données d’encre (objets utilisés pour gérer l’encre collectée).
-   Reconnaissance de l’encre (objets utilisés pour convertir l’encre collectée en d’autres types de données, tels que du texte).

L’illustration suivante montre, à un niveau élevé, comment l’API de collection d’encres (API Pen), l’API Ink Gestion des données (API Ink) et l’API de reconnaissance d’encre (API de reconnaissance) fonctionnent ensemble dans la plateforme Tablet PC.

![illustraton illustrant le fonctionnement conjoint des API de stylet, de l’API Ink et de la reconnaissance](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

L’API de plateforme Tablet PC est disponible dans les API gérées, ainsi que dans une bibliothèque COM. Les rubriques suivantes décrivent les objets de l’API et illustrent comment les applications utilisent ces objets :

-   [Collection d’encres](ink-collection.md)
-   [Données manuscrites](ink-data.md)
-   [Reconnaissance de l’encre](ink-recognition.md)
-   [Analyse de l’encre](ink-analysis.md)
-   [Reconnaissance de l’écriture manuscrite dans Windows Server 2008 R2](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



