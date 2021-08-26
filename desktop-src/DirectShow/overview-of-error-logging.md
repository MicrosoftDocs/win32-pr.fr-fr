---
description: Vue d’ensemble de la journalisation des erreurs
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Vue d’ensemble de la journalisation des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcde3e0366ffca12dfcb5674259273ba1bbf25c1feed9be3ead57fa64cc42dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904629"
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

 

 



