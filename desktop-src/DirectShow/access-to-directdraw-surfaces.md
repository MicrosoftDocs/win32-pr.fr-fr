---
description: Accès aux surfaces DirectDraw
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: Accès aux surfaces DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff443550cb6a922a3361b6d75b880eb427edf79e3a3232c21ab6aad0c06ec483
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873569"
---
# <a name="access-to-directdraw-surfaces"></a>Accès aux surfaces DirectDraw

Les exemples d’objets multimédias fournis par VMR aux filtres en amont prennent en charge l’interface [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) . Pour obtenir l’interface, appelez QueryInterface sur l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) et spécifiez IID \_ IVMRSurface. Les filtres en amont peuvent ensuite utiliser les méthodes IVMRSurface pour accéder et manipuler la surface créée par VMR.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[utilisation de VMR pour les développeurs de filtre DirectShow](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



