---
description: Interfaces de base de diffusion multimédia
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Interfaces de base de diffusion multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953470"
---
# <a name="base-multimedia-streaming-interfaces"></a>Interfaces de base de diffusion multimédia

> [!Note]  
> Ces API sont déconseillées. Les applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.

 

Les interfaces de base de diffusion multimédia en continu offrent un moyen d’accéder par programmation aux flux multimédias. Toutefois, l’utilisation d’une interface de base pour accéder à un type de données spécifique peut limiter la quantité de contrôle dont vous disposez sur les données, de sorte que les développeurs de médias doivent créer des versions dérivées de ces interfaces qui offrent un contrôle plus puissant sur les fonctionnalités uniques de leur type de média.



| Interface                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | Définit comment accéder à l’objet de flux multimédia de plus haut niveau ; cet objet contient et permet d’accéder à d’autres objets de flux. [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) possède des méthodes qui énumèrent ou récupèrent des flux spécifiques, ainsi que la vérification de la durée totale du flux et la recherche dans le flux.                                                                                                       |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | Définit un objet de flux générique. Utilisez ses méthodes pour récupérer un pointeur vers le flux, obtenir des informations sur le flux et créer des exemples à partir des données de flux. Vous pouvez également créer des exemples de flux partagés, auxquels plusieurs flux peuvent accéder sans dupliquer les données de l’exemple.                                                                                                                                                  |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | Contrôle le comportement d’un exemple de flux spécifique. Vous pouvez récupérer le flux qui a créé l’exemple, vérifier l’heure de début et de fin et l’état d’achèvement de l’exemple, et exécuter une fonction définie par l’utilisateur sur l’exemple lui-même (à l’aide de la méthode [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) ). En règle générale, la méthode de mise à jour traite les exemples de données de manière appropriée, comme le rendu des données vidéo ou la lecture de données audio. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liste des interfaces de diffusion multimédia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



