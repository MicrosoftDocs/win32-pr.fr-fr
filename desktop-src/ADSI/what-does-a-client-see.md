---
title: Présentation du client
description: Cette rubrique répertorie les façons dont un client affiche les données ADSI.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- les extensions ADSI, ce qu’un client voit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d38563de47cfc80bdcf265249bf3e4cf10bc46471e18672221fed8c3047efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082173"
---
# <a name="what-does-a-client-see"></a>Qu’est-ce qu’un client ?

-   Un client voit ADSI et tous ses objets d’extension comme un seul objet.
-   Un client ADSI voit une interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui gère toutes les interfaces de dispatch et de double dans l’objet, que l’interface de dispatch ou double soit implémentée par l’agrégateur dans le fournisseur ou par une extension. Consultez la [résolution des conflits de noms de fonctions/propriétés dans Automation dans les extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).
-   ADSI n’expose aucune information de type par le biais des méthodes [**IDispatch :: GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) ou [**IDispatch :: GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) . ADSI fournit des informations de type par le biais de la bibliothèque de types.

 

 