---
description: Vue d’ensemble de la journalisation des erreurs
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Vue d’ensemble de la journalisation des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af82c35cdb34a238e280641015407c7a5d6f837
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312330"
---
# <a name="overview-of-error-logging"></a>Vue d’ensemble de la journalisation des erreurs

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

pour offrir aux applications une flexibilité maximale pour la gestion des erreurs, [DirectShow Services d’édition](directshow-editing-services.md) utilise un mécanisme de rappel. Votre application implémente une méthode de journalisation d’une erreur. Au moment de l’exécution, si une erreur se produit, l’algorithme DES appelle la méthode que vous avez fournie. La méthode accepte des paramètres qui décrivent l’erreur. Ce que fait la méthode avec ces informations vous revient. (Toutefois, il doit retourner aussi rapidement que possible, mais peut interférer avec l’exécution du programme.)

La méthode de rappel d’enregistrement des erreurs est contenue dans une interface COM, [**IAMErrorLog**](iamerrorlog.md). Votre application doit implémenter cette interface. Comme toutes les interfaces COM, **IAMErrorLog** hérite de l’interface **IUnknown** , donc votre application doit également l’implémenter.

Vous avez le choix entre plusieurs options pour implémenter ces interfaces COM. Vous pouvez utiliser la Active Template Library (ATL), qui fournit des implémentations de stock des méthodes **IUnknown** . DirectShow fournit également une classe de base C++, [**CUnknown**](cunknown.md), qui permet d’implémenter facilement une interface COM. Pour plus d’informations sur l’utilisation de **CUnknown**, consultez [How to implement IUnknown](how-to-implement-iunknown.md).

L’exemple de code de cet article définit une classe C++ autonome qui implémente à la fois **IUnknown** et **IAMErrorLog**. Le résultat n’est pas un vrai objet COM, car il ne prend pas en charge **CoCreateInstance**. Toutefois, cette approche est adaptée à l’objectif de l’exemple.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Journalisation des erreurs](logging-errors.md)
</dt> </dl>

 

 



