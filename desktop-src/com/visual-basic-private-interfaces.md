---
title: Visual Basic Interfaces privées
description: Visual Basic Interfaces privées
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291843"
---
# <a name="visual-basic-private-interfaces"></a>Visual Basic Interfaces privées

deux interfaces implémentées par Visual Basic sont identifiées ici pour les catégories de composants. Il n’est pas prévu que les contrôles requièrent ces catégories, car il est possible que les contrôles offrent d’autres fonctionnalités lorsque celles-ci ne sont pas disponibles.

l’interface [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) permet aux contrôles de mieux s’intégrer à l’environnement de Visual Basic lors de la mise en forme des données.

CATID-{02496840-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBFormat

l’interface [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) permet à un contrôle d’énumérer d’autres contrôles sur le formulaire VB.

CATID-{02496841-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBGetControl

Deux interfaces privées supplémentaires, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) et [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), sont décrites ici, même si elles ne définissent pas les catégories de composants. L’utilisation de ces quatre interfaces n’est pas recommandée, car elles ne sont pas prises en charge par les conteneurs autres que Visual Basic.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Catégories de composant](component-categories.md)
</dt> </dl>

 

 




