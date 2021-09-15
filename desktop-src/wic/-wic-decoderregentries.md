---
description: Decoder-Specific les entrées de Registre
ms.assetid: 64ef260a-ed7f-4253-a644-bd3352b0ee41
title: Decoder-Specific les entrées de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17485e7adca62abd31643d84d371a0002724ea9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521164"
---
# <a name="decoder-specific-registry-entries"></a>Decoder-Specific les entrées de Registre


Outre les entrées de Registre requises pour tous les encodeurs et décodeurs, les entrées de Registre suivantes sont requises spécifiquement pour les décodeurs.

ces entrées inscrivent votre décodeur sous la catégorie des décodeurs WIC (Windows Imaging Component). Le premier GUID dans ces entrées est l’identificateur de catégorie (CATID) pour [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

comme indiqué dans la section [découverte et arbitrage](-wic-howwicworks.md) du fonctionnement du composant de création d’images Windows, le mécanisme qui permet à un décodeur approprié pour une image spécifique d’être découvert au moment de l’exécution est basé sur la mise en correspondance d’un modèle d’identification incorporé dans le fichier image avec un modèle spécifié dans l’entrée de registre du décodeur. Pour activer la découverte des décodeurs au moment de l’exécution, vous devez inscrire le modèle d’identification unique pour votre format d’image comme suit. Toutes ces entrées de Registre sont requises, à l’exception de l’entrée **EndOfStream** , qui est facultative, comme décrit dans le tableau suivant.

```
HKEY_CLASSES_ROOT
   CLSID
      {Decoder CLSID}
         Patterns
            {0}
               Position = Offset in block
               Length = Length of pattern
               Pattern = Pattern to match
               Mask = FF FF FF FF
               EndOfStream = 0|1
```



| Valeur       | Description                                                                                                                                                                                                                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Position    | Offset dans le fichier où se trouve le modèle.                                                                                                                                                                                                                                                                        |
| Longueur      | Longueur du modèle.                                                                                                                                                                                                                                                                                                      |
| Modèle     | Bits réels qui composent le modèle. Il s’agit des bits qui sont mis en correspondance avec le modèle d’identification dans un fichier image pendant la découverte.                                                                                                                                                                                |
| Mask        | Autorise les valeurs de caractères génériques dans les modèles. Le masque est appliqué en effectuant une opération AND logique sur le modèle et le masque. Tout bit du modèle qui correspond à un bit dans le masque avec une valeur de 0 est ignoré.                                                                                                       |
| EndOfStream | Le décalage du modèle d’identification doit être calculé à partir de la fin du flux, et non au début. Certains formats d’image placent le modèle d’identification à la fin ou près de la fin du fichier. Étant donné que la valeur par défaut consiste à effectuer une recherche à partir du début, à moins que votre modèle ne soit près de la fin du fichier, vous pouvez omettre cette entrée. |



 

Un codec peut prendre en charge plusieurs modèles d’identification. Dans ce cas, vous devez répéter toutes les clés sous les **\_ classes HKEY \_ \\ CLSID racine CLSID \\ {Decoder CLSID} \\** et utiliser la clé numérique (0 dans l’exemple) pour faire la distinction entre les différents modèles. Vous devez inclure chacune des quatre valeurs sous la clé pour chaque modèle.

## <a name="registering-a-container-format-with-metadata-readers"></a>Inscription d’un format de conteneur avec des lecteurs de métadonnées

Si vous créez un nouveau format de conteneur pour votre codec, vous devez également créer des entrées de Registre pour prendre en charge la découverte des lecteurs de métadonnées pour les blocs de métadonnées dans vos images, tout comme vous l’avez fait pour les enregistreurs de métadonnées. Les entrées suivantes doivent être créées sous l’identificateur de classe (CLSID) du lecteur de métadonnées pour chaque format de métadonnées que votre format de conteneur prend en charge. (Notez que, si votre codec utilise un conteneur TIFF (Tagged Image File Format), ces informations se trouvent déjà dans le registre.)

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Reader CLSID}
         Containers
            {Container Format GUID}
               
                  Position = Offset relative to its container
                  Pattern = Pattern used for metadata header
                  Mask = FF FF FF FF
                  DataOffset = Offset from beginning of header
```

Étant donné que les entrées pour les lecteurs de métadonnées sont également utilisées pour la découverte, elles sont très similaires aux entrées pour les décodeurs. Ces entrées sont utilisées par la fabrique de composants pour rechercher les lecteurs de métadonnées pris en charge par votre conteneur et pour sélectionner l’application appropriée, lorsque votre implémentation de [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) demande un lecteur de métadonnées.



| Valeur      | Description                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Position   | Offset dans le conteneur du bloc de métadonnées dans lequel l’en-tête de métadonnées est trouvé. Pour les blocs de métadonnées de niveau supérieur, il s’agit du décalage dans le flux de fichier. Pour les blocs de métadonnées imbriqués dans d’autres blocs de métadonnées, il s’agit du décalage par rapport au bloc de métadonnées conteneur. |
| Modèle    | Bits réels qui composent le modèle. Il s’agit des bits qui sont mis en correspondance avec le modèle d’identification dans un fichier image pendant la découverte.                                                                                                                            |
| Mask       | L’en-tête de métadonnées est généralement défini par le gestionnaire de métadonnées. Vous devez utiliser l’en-tête de métadonnées standard pour chaque lecteur, sauf si, pour une raison quelconque, le modèle doit avoir un format différent dans votre conteneur.                                                          |
| DataOffset | Offset à partir du début de l’en-tête de métadonnées au niveau duquel les données réelles commencent. Dans les cas où les métadonnées ne sont pas situées à un décalage spécifique par rapport à l’en-tête, cette entrée peut être omise.                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Entrées de Registre spécifiques à l’encodeur](-wic-encoderregentries.md)
</dt> <dt>

[intégration avec Windows galerie de photos et l’explorateur de Windows](-wic-integrationregentries.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



