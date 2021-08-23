---
description: l’appareil de scanneur d’images Windows (WIA) est implémenté sous la forme d’une arborescence hiérarchique d’objets IWiaItem.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: Appareils de scanneur WIA dans WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd22cc9fe330a3acf231034b61c72178f3b282cb9e66a1f455d4b6939a1c3cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592667"
---
# <a name="wia-scanner-devices-in-wia-10"></a>Appareils de scanneur WIA dans WIA 1,0

> [!Note]  
> cette rubrique décrit l’arborescence des appareils du scanneur pour les applications qui utilisent le service WIA (Windows Image Acquisition) 1,0 (prise en charge sur Windows XP ou version antérieure). pour plus d’informations sur l’arborescence d’appareils des éléments WIA (Windows Image Acquisition) 2,0 (qui sont pris en charge sur Windows Vista ou version ultérieure), consultez [à propos de l’arborescence des éléments IWiaItem2](-wia-about-item-tree.md).

 

l’appareil de scanneur d’images Windows (WIA) est implémenté sous la forme d’une arborescence hiérarchique d’objets [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . À partir de l’élément racine, une application peut :

-   Fonctionnalités de l’analyseur de requêtes
-   Définir les propriétés d’un périphérique de scanneur
-   Contrôler le chargeur de documents

Un périphérique de scanneur WIA est différent d’un appareil photo WIA, car, en général, il ne stocke pas plusieurs images en mémoire.

Sous l’élément racine, un objet scanneur type possède un objet [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) unique qui représente la fonctionnalité de collecte des données de l’appareil, l’élément d’analyse. L’indicateur [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) est défini pour cet élément pour indiquer que les transferts de données sur cet élément sont possibles. Une application configure une analyse en définissant les propriétés de l’élément d’analyse, puis effectue l’analyse et transfère les données à l’aide d’une interface de transfert de données.

Le diagramme suivant illustre l’implémentation WIA pour un scanneur classique :

![implémentation WIA d’un scanneur classique](images/wiscantr.gif)

Un scanneur duplex standard est représenté dans WIA en présence d’un objet [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . Les données de page frontale et de page principale sont accessibles séquentiellement un transfert de données par page. Par conséquent, la représentation d’un scanneur duplex est identique à la représentation d’un scanneur classique.

Un scanneur de diapositives permettant d’analyser plusieurs diapositives en une seule opération représente chaque image distincte sous la forme d’un objet [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) distinct.

Le diagramme suivant illustre la représentation WIA d’un scanneur de diapositive :

![Scanner de diapositive](images/wislscan.gif)

 

 



