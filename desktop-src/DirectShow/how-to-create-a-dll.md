---
description: Comment créer une DLL de filtre DirectShow
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Comment créer une DLL de filtre DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514301"
---
# <a name="how-to-create-a-directshow-filter-dll"></a>Comment créer une DLL de filtre DirectShow

Cet article explique comment implémenter un composant en tant que bibliothèque de liens dynamiques (DLL) dans Microsoft DirectShow. Cet article est une suite de la [procédure d’implémentation de IUnknown](how-to-implement-iunknown.md), qui décrit comment implémenter l’interface **IUnknown** en dérivant votre composant de la classe de base [**CUnknown**](cunknown.md) .

Cet article contient les sections suivantes.

-   [Fabriques de classes et modèles de fabrique](class-factories-and-factory-templates.md)
-   [Tableau de modèles de fabrique](factory-template-array.md)
-   [Fonctions DLL](dll-functions.md)

L’inscription d’un filtre DirectShow (par opposition à un objet COM générique) requiert des étapes supplémentaires qui ne sont pas traitées dans cet article. Pour plus d’informations sur l’enregistrement des filtres, voir [How to Register DirectShow Filters](how-to-register-directshow-filters.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow et COM](directshow-and-com.md)
</dt> </dl>

 

 



