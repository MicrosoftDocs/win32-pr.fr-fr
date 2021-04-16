---
title: Présentation du client
description: Cette rubrique répertorie les façons dont un client affiche les données ADSI.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- les extensions ADSI, ce qu’un client voit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398c9fd2d603c1eebb18280c435bec7cb7cd8e14
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508129"
---
# <a name="what-does-a-client-see"></a>Qu’est-ce qu’un client ?

-   Un client voit ADSI et tous ses objets d’extension comme un seul objet.
-   Un client ADSI voit une interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) qui gère toutes les interfaces de dispatch et de double dans l’objet, que l’interface de dispatch ou double soit implémentée par l’agrégateur dans le fournisseur ou par une extension. Consultez la [résolution des conflits de noms de fonctions/propriétés dans Automation dans les extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).
-   ADSI n’expose aucune information de type par le biais des méthodes [**IDispatch :: GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) ou [**IDispatch :: GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) . ADSI fournit des informations de type par le biais de la bibliothèque de types.

 

 