---
title: Interfaces doubles (COM)
description: Interfaces doubles
ms.assetid: 6e4dc529-8a25-4ae5-b868-28cb17e0db52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da95c77a307c40721b909eceb1e6d29bab23bc14
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031968"
---
# <a name="dual-interfaces"></a>Interfaces doubles

OLE Automation permet à un objet d’exposer un ensemble de méthodes de deux façons : via l’interface **IDispatch** et via une liaison directe OLE vtable. **IDispatch** est utilisé par la plupart des outils disponibles aujourd’hui et prend en charge la liaison tardive à des propriétés et des méthodes.

La liaison VTable offre des performances nettement supérieures, car cette méthode est appelée directement plutôt que par le biais de **IDispatch :: Invoke**. **IDispatch** offre une prise en charge à liaison tardive, où la liaison vtable directe offre un gain de performances significatif ; les deux techniques sont utiles et importantes dans différents scénarios. En attribuant une étiquette à une interface \[ [**double**](/windows/desktop/Midl/dual) \] dans la bibliothèque de types, une interface OLE Automation peut être utilisée via **IDispatch**, ou elle peut être liée directement à. Les conteneurs peuvent donc choisir la technique la plus appropriée. La prise en charge des interfaces doubles est fortement recommandée pour les contrôles et les conteneurs.

 

 