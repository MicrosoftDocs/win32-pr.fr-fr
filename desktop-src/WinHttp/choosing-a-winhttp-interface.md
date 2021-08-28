---
description: avant de commencer à développer une application Microsoft Windows HTTP Services (WinHTTP), vous devez d’abord déterminer s’il faut utiliser l’API C/C++ ou l’interface COM.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Choix d’une interface WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7772959bd76dc7a257abc180c915f99df988a7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472355"
---
# <a name="choosing-a-winhttp-interface"></a>Choix d’une interface WinHTTP

avant de commencer à développer une application Microsoft Windows HTTP Services (WinHTTP), vous devez d’abord déterminer s’il faut utiliser l’API C/C++ ou l’interface COM. Le tableau suivant récapitule les avantages et les inconvénients associés à chacune de ces approches.




|  | API C/C++ | Interface COM | 
|--|-----------|---------------|
| Avantages | <ul><li>Les réponses peuvent être traitées par segments, ce qui est plus efficace.</li><li>Les opérations de publication peuvent également être traitées par segments, accélérant ainsi le temps de traitement.</li><li>Prise en charge d’AutoProxy.</li><li>Accès à l’ensemble complet des fonctionnalités de WinHTTP.</li><li>Les données binaires peuvent être facilement gérées.</li></ul> | <ul><li>La création d’une application est simple et requiert moins de lignes de code que l’API C/C++.</li><li>L’interface peut être utilisée par les langages de script.</li></ul> | 
| Inconvénients | <ul><li>Le traitement est plus complexe.</li><li>L’API C/C++ requiert davantage d’étapes que l’interface COM pour effectuer les mêmes actions.</li><li>La configuration d’une demande nécessite davantage de code.</li></ul> | <ul><li>L’interface COM ne permet pas d’accéder à l’ensemble complet des fonctionnalités de WinHTTP.</li><li>Il est difficile de gérer les types de données binaires dans certains langages de script, tels que VBScript et JScript.</li><li>L’interface COM ne prend pas en charge le proxy AutoProxy.</li><li>Les applications doivent utiliser le modèle de APARTMENT_THREADED COM.</li><li>Avant qu’une réponse puisse commencer à être traitée, toute la réponse doit d’abord être reçue et mise en mémoire tampon.</li></ul> | 




 

 

 



