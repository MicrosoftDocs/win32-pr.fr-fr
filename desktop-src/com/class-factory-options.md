---
title: Options de fabrique de classes
description: Options de fabrique de classes
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730429"
---
# <a name="class-factory-options"></a>Options de fabrique de classes

Un contrôle ActiveX, en vertu d’un objet COM, doit avoir un code serveur associé qui prend en charge la création de contrôles via [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) au minimum.

Il est facultatif, pas obligatoire, que cet objet de classe prenne également en charge [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) pour la gestion des licences. Seuls les fournisseurs concernés par les licences doivent prendre en charge le mécanisme de licence de COM. En d’autres termes, étant donné que **IClassFactory2** est le seul moyen d’obtenir une licence de niveau com, cette interface est requise sur l’objet de classe pour les contrôles qui souhaitent être sous licence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles](controls.md)
</dt> </dl>

 

 