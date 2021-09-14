---
title: Stockage asynchrone et synchrone
description: Stockage asynchrone et synchrone
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295759"
---
# <a name="asynchronous-and-synchronous-storage"></a>Stockage asynchrone et synchrone

les monikers asynchrones peuvent également retourner un objet [Stockage asynchrone](/windows/desktop/Stg/asynchronous-storage) dans la notification [**IBindStatusCallback :: OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) . Cet objet de stockage peut autoriser l’accès à certaines données persistantes de l’objet pendant que la liaison est toujours en cours. Un client peut choisir entre deux modes de stockage : blocage et non-blocage.

En mode blocage, qui est compatible avec les implémentations actuelles des objets de stockage, si les données ne sont pas disponibles, l’appel est bloqué jusqu’à l’arrivée des données. En mode non bloquant, au lieu de bloquer l’appel, l’objet de stockage retourne une nouvelle erreur E \_ en attente lorsque les données ne sont pas disponibles. Un client connaissant la liaison et le stockage asynchrones note cette erreur et attend d’autres notifications ([**ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) pour retenter l’opération. Un client peut choisir entre un stockage synchrone (blocage) et un stockage asynchrone (sans blocage) en choisissant de définir l' \_ indicateur BINDF ASYNCSTORAGE dans la valeur *grfBINDF* retournée à [**IBindStatusCallback :: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Monikers asynchrones](asynchronous-monikers.md)
</dt> </dl>

 

 