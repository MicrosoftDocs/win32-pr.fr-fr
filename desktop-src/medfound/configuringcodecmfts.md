---
description: Configuration du codec MFTs
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: Configuration du codec MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0065f05d10eae367b13ef6f7caf3fe2ab322163a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296327"
---
# <a name="configuring-codec-mfts"></a>Configuration du codec MFTs

Cette rubrique décrit le processus de configuration du codec MFTs. Chaque codec a des procédures spécifiques, mais les informations communes à toutes sont décrites ici.

## <a name="configuring-mft-inputs-and-outputs"></a>Configuration des entrées et des sorties MFT

Chaque MFT prend en charge des types d’entrée et de sortie spécifiques. Vous pouvez récupérer les types d’entrée pris en charge en appelant à plusieurs reprises [**IMFTransform :: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), en incrémentant l’index de type avec chaque appel. Lorsque vous trouvez un type approprié, définissez le type d’entrée en appelant [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype). Vous pouvez ensuite répéter le processus pour le type de sortie à l’aide des appels [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) et [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). Vous devez interroger ou définir les types de sortie disponibles uniquement après avoir défini le type d’entrée.

## <a name="configuring-the-codec-mfts-for-encoding"></a>Configuration du codec MFTs pour l’encodage

tous les codecs vidéo et Windows Media Audio prennent en charge un large éventail de fonctionnalités d’encodage. Ces fonctionnalités sont généralement configurées en définissant des propriétés sur la table MFT à l’aide des méthodes de l’interface **IPropertyStore** . Certaines propriétés sont configurées à l’aide d’interfaces de codec spécialisées. Ces interfaces sont répertoriées pour chaque codec dans la section [objets codec](codecobjects.md).

L’ordre général des opérations de configuration d’une table MFT d’encodage est le suivant :

1.  Configurez les fonctionnalités du codec comme vous le souhaitez à l’aide des méthodes de **IPropertyStore**.
2.  Utilisez les interfaces MFT du codec pour configurer des fonctionnalités supplémentaires, si nécessaire.
3.  Configurez les types d’entrée et de sortie. L’ordre dans lequel les types doivent être configurés varie en fonction des codecs individuels. Pour plus d’informations, consultez [utilisation de l’audio](workingwithaudio.md) et [utilisation de la vidéo](workingwithvideo.md).

## <a name="configuring-the-codec-mfts-for-decoding"></a>Configuration du codec MFTs pour le décodage

Le décodage est plus simple que l’encodage, car un nombre inférieur de fonctionnalités de décodeur est pris en charge.

L’ordre général des opérations de configuration d’une table MFT de décodage est le suivant :

1.  Configurez les fonctionnalités du décodeur comme vous le souhaitez à l’aide des méthodes de **IPropertyStore**.
2.  Définissez le type d’entrée sur le type utilisé pour la sortie de l’encodeur.
3.  Configurez le type de sortie. Les types de sortie pris en charge sont différents pour les différentes entrées.

> [!Note]  
> Il est important d’utiliser le même type de média pour l’entrée du décodeur que celui utilisé pour la sortie de l’encodeur. cela est dû au fait que les codecs Windows Media Audio et vidéo utilisent des formats multimédias avec des données supplémentaires. Sans les données de format étendu, vous ne pouvez pas décoder le contenu compressé.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



