---
description: utilisation de Flux multimédias dans les Applications
ms.assetid: 73cfe89b-df46-445a-92c7-2f7323672441
title: utilisation de Flux multimédias dans les Applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30dab204bc7b0bddbdc293708daecbe0558e8f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094642"
---
# <a name="using-multimedia-streams-in-applications"></a>utilisation de Flux multimédias dans les Applications

> [!Note]  
> Ces API sont déconseillées. les Applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.

 

Les interfaces de diffusion multimédia en continu simplifient radicalement le processus de manipulation des données multimédias en supprimant la dépendance sur des caractéristiques spécifiques de la source matérielle ou logicielle et en fournissant la prise en charge de tous les formats Microsoft DirectX® Media. Flux abstrait les données à un niveau très élevé ; les applications peuvent même déplacer des données d’un flux à un autre sans connaître le format des données.

Pour créer un flux multimédia, procédez comme suit.

1.  Créez le flux multimédia. La méthode de création et d’initialisation du flux est spécifique à l’architecture. DirectShow prend en charge l’interface [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) , qui est utilisée pour initialiser le flux. D’autres implémentations de serveur in-process de [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) seront créées et initialisées à l’aide de différents mécanismes.
2.  Après l’initialisation de l’objet de flux multimédia, l’application utilise **QueryInterface** pour récupérer l’interface **IMultiMediaStream** pour l’objet. Utilisez cette interface pour déterminer les propriétés du flux et énumérer les flux eux-mêmes. Vous pouvez récupérer un flux spécifique en appelant la méthode [**IMultiMediaStream :: GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) avec un ID d’objet spécifique. MSPID \_ PrimaryVideo et MSPID \_ PrimaryAudio, qui représentent les flux vidéo et audio principaux, sont les ID d’objet les plus couramment utilisés.
3.  Appelez **IUnknown :: QueryInterface** pour une interface spécifique au type de média du flux. Si vous souhaitez afficher un flux vidéo, par exemple, récupérez son interface [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) . Les interfaces spécifiques aux médias définissent des méthodes supplémentaires nécessaires pour tirer pleinement parti des fonctionnalités d’un format.
4.  Créez un ou plusieurs exemples à partir des données de flux. Chaque flux multimédia prend en charge la méthode [**IMediaStream :: CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) pour l’exemple de création. L’exemple qui en résulte prend en charge l’interface [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) , qui permet de contrôler l’échantillon et ses caractéristiques. En règle générale, le flux multimédia prend en charge une méthode spécifique au format d’exemple de création, qui est plus puissante que les méthodes **IStreamSample** mentionnées ci-dessus. **IDirectDrawMediaStream**, par exemple, peut créer des échantillons attachés à une surface DirectDraw souhaitée et un rectangle de découpage. Toutefois, dans certaines situations, vous devez gérer les données sans connaître leur format de données. Si vous souhaitez diffuser en continu des données indépendantes de leur format, utilisez la méthode **IMediaStream :: CreateSharedSample** pour créer les exemples de données.
5.  Après avoir créé tous les exemples de flux souhaités, démarrez le flux en appelant la méthode [**IMultiMediaStream :: SetState**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-setstate) et transmettez l' \_ indicateur d’exécution STREAMSTATE en tant que paramètre.
6.  Appelez [**IStreamSample :: Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) pour mettre à jour l’exemple de flux. Quand la méthode **IStreamSample :: Update** se termine, vous pouvez accéder aux données de l’exemple. Si vous souhaitez déclencher un événement ou un appel de fonction spécifique lorsque la mise à jour est retournée, transmettez les pointeurs appropriés à la méthode **IStreamSample :: Update** .

Pour plus d’informations sur les interfaces de diffusion multimédia en continu, consultez [diffusion multimédia en continu](multimedia-streaming.md).

 

 



